![Status](https://img.shields.io/badge/Status-Complete-brightgreen)
![Tools](https://img.shields.io/badge/SIEM-Splunk-orange)
![Platform](https://img.shields.io/badge/Platform-Ubuntu_Linux-purple)
![Type](https://img.shields.io/badge/Type-Blue_Team_Lab-blue)
![Threats](https://img.shields.io/badge/Threats_Detected-3-red)

# Firewall Log Analysis & Threat Detection Lab

## Project Overview
Blue Team SOC lab analysing pfSense firewall logs 
using Splunk Enterprise to detect real attack patterns.

## Threats Detected
- Port Scan — 192.168.1.105
- SSH Brute Force — 185.220.101.45  
- Metasploit C2 Traffic — Port 4444

## Tools Used
- Splunk Enterprise 10.4.0
- pfSense Firewall Logs
- SPL Queries
- Ubuntu Linux on VirtualBox

## Skills Demonstrated
- Firewall log ingestion into SIEM
- SPL query writing for threat detection
- Alert triage and incident documentation
- SOC Tier 1 analyst workflow

## Screenshots

### Splunk Dashboard
![Splunk Dashboard](screenshots/splunk-dashboard.png)

### Firewall Logs Ingested
![Firewall Logs](screenshots/firewall-logs-created.png)

### Port Scan Detected
![Port Scan](screenshots/splunk_port_scan_detected.png)

### Brute Force Attack Detected
![Brute Force](screenshots/splunk_brute_force_detected.png)

### Metasploit C2 Traffic Detected
![Metasploit](screenshots/splunk_metasploit_port_detected.png)

### Incident Report
![Incident Report](screenshots/incident_report.png)

## Analyst
Raphael Akro | raphsec.github.io
