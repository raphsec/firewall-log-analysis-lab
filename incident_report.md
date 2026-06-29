# Firewall Log Analysis — Incident Report
Analyst: Raphael Akro  
Date: June 28, 2026  
Lab Environment: pfSense Firewall Logs | Splunk Enterprise 10.4.0 | Ubuntu Linux  

## Executive Summary
Analysed pfSense firewall logs using Splunk to identify 
malicious activity. Detected 3 confirmed threat patterns 
across 15 firewall events including a port scan, SSH brute 
force attack, and Metasploit C2 communication attempt.

## Findings

### Finding 1 — Internal Port Scan
- Source IP: 192.168.1.105
- Target IP: 10.0.0.1
- Ports Scanned: 22, 23, 80, 443, 3389, 445, 4444
- Time: 08:23:01 — 08:23:04
- Action: All blocked
- Conclusion: Automated port scan detected. 
7 ports probed in 3 seconds indicating reconnaissance activity.
  
- **Severity:** 🟡 MEDIUM

### Finding 2 — SSH Brute Force Attack
- Source IP: 185.220.101.45 (External)
- Target: 10.0.0.1 Port 22
- Attempts: 5 in 4 seconds
- Action: All blocked
- Conclusion: External brute force attack on SSH service.

- **Severity:** 🔴 HIGH

### Finding 3 — Metasploit C2 Traffic
- Source IP: 45.33.32.156 (External)
- Target: 10.0.0.1 Port 4444
- Action: Blocked
- Conclusion: Connection attempt on Metasploit default 
port — possible C2 communication attempt.

- **Severity:** 🔴 CRITICAL

## Recommendations
1. Block 192.168.1.105 immediately and investigate the device
2. Block 185.220.101.45 at perimeter — known brute force IP
3. Block 45.33.32.156 — suspicious C2 activity
4. Disable SSH port 22 or move to non-standard port
5. Set up automated alerts for port 4444 traffic

## Tools Used
- Splunk Enterprise 10.4.0
- pfSense Firewall Logs
- SPL Queries for threat detection
- Ubuntu Linux Lab Environment
