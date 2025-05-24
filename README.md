🏗️ SCADA and OT Security Lab Setup – Full Lab Series

This repository documents a full virtual lab environment designed for industrial network security testing and monitoring. The labs simulate a segmented network infrastructure protected and monitored with open-source tools like Security Onion, pfSense, Snort, Wazuh, and Sysmon, and visualize activity using Kibana.

---

## 📁 Repository Structure

| File Name                                         | Description |
|--------------------------------------------------|-------------|
| `Lab0 - Virtual Box Network Setup.docx`          | NAT network segmentation with VirtualBox for internal/external/DMZ zones |
| `Lab 1 - Security Onion Setup.docx`              | Security Onion installation, Suricata setup, Wazuh deployment |
| `Lab 2 - pfSense Firewall Configuration.docx`    | pfSense installation and log forwarding to Security Onion |
| `Exercise4Scada(1).docx`                         | Adding Snort IDS to pfSense (intrusion prevention mode) |
| `Lab 5 - Using Wazuh to add PowerShell logging.docx` | Monitoring PowerShell script execution (Event ID 4104) |
| `Lab 6 - Using Wazuh to add Sysmon logging.docx` | Sysmon integration for deep endpoint visibility |
| `Lab 7 - Creating pfSense Firewall Dashboard in Kibana.docx` | Visualizing firewall logs with custom dashboards |

---

## 🧱 Lab Architecture Overview

### 🔹 Virtual Network Segments
- Internal Zone: `192.168.10.0/24`
- External Zone: `192.168.20.0/24`
- DMZ: `10.10.10.0/24`

### 🔹 Key VMs
- `SecurityOnion`: IDS, SIEM, ELK stack
- `pfSense`: Firewall with Snort integration
- `Windows VM`: For endpoint logging, PowerShell, and Sysmon

---

## 🔍 Lab Highlights

### ✅ Lab 0: Network Setup
- Created NAT networks in VirtualBox for segmented traffic simulation

### ✅ Lab 1: Security Onion
- Installed and configured ELK stack with Suricata
- Created users and updated rulesets
- Integrated Wazuh agent for host monitoring

### ✅ Lab 2: pfSense
- Deployed pfSense firewall
- Configured syslog forwarding to Security Onion
- Synchronized logs for unified event visibility

### ✅ Lab 4 (Exercise 4): Snort IDS
- Installed Snort on pfSense
- Switched from IDS to IPS (blocking mode)
- Tested detection using `http://testmyids.ca`

### ✅ Lab 5: PowerShell Script Block Logging
- Enabled GPO logging for PowerShell (Event ID 4104)
- Forwarded logs via Wazuh to Elasticsearch
- Verified script execution visibility in Kibana

### ✅ Lab 6: Sysmon Logging
- Installed Sysmon on endpoint
- Used SwiftOnSecurity config for rich telemetry
- Sent process and file activity logs to ELK

### ✅ Lab 7: Kibana Firewall Dashboard
- Created custom visualizations:
  - Source/Destination IPs
  - Ports
  - Network protocols
  - Action summary pie charts
- All widgets integrated into a custom dashboard

---

## 🛠️ Tools Used

- 🧱 VirtualBox – Virtualization & network segmentation
- 🧠 Security Onion – Threat detection, log analysis (Suricata, Wazuh)
- 🔥 pfSense – Firewall/NAT/Snort IDS/IPS
- 🐍 Wazuh – HIDS for log forwarding
- 🪟 Sysmon – Deep endpoint monitoring (processes, hashes, parent-child)
- 📊 Kibana – Log visualization and correlation dashboards

---

## 👨‍💻 Author

Sriram 
Master’s in Digital Forensics & Cybersecurity  
University at Albany, SUNY – Spring 2025

---

## 📄 License

This project is licensed under the  
Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International (CC BY-NC-ND 4.0)

📌 You may view and share this work with proper credit, but you may not modify or use it commercially.

🔗 [View License Terms](https://creativecommons.org/licenses/by-nc-nd/4.0/)
