# linux-soc-splunk-detection-lab
Linux SOC detection lab using Splunk SIEM to simulate and detect real-world attacks like brute-force logins, SQL injection, directory enumeration, and vulnerability scanning. Focused on log analysis, SPL queries, and attacker behavior using DVWA and Kali Linux tools.
# 🛡️ Linux SOC Detection Lab using Splunk

## 📌 Overview
This project simulates a real-world Security Operations Center (SOC) environment using Linux systems, DVWA web application, offensive security tools, and Splunk SIEM.

It focuses on detecting attacker behavior by generating malicious traffic and analyzing logs.

---

## 🎯 Real-Life Problems This Project Solves

This lab simulates common cyberattacks seen in real organizations:

- 🔐 Brute-force SSH login attempts
- 💉 SQL injection attacks against web applications
- 🌐 Directory enumeration (hidden path discovery)
- 🧪 Web vulnerability scanning
- 📊 Authentication anomalies and suspicious login behavior

These are real attack techniques observed in production environments.

---

## 🏗️ Architecture

Kali Linux (Attacker Machine)
        ↓
Ubuntu Server (DVWA + Apache logs)
        ↓
Splunk Forwarder
        ↓
Splunk Enterprise (SIEM Analysis Engine)

---

## ⚔️ Tools Used

### Attack Tools (Kali Linux)
- Hydra → SSH brute force attacks
- SQLmap → SQL injection testing
- Gobuster → directory enumeration
- Nikto → vulnerability scanning

---

## 📊 What This Project Demonstrates

- SIEM log ingestion using Splunk
- Detection engineering using SPL queries
- Web attack pattern recognition
- Security monitoring of Linux systems
- SOC-style investigation workflow

---

## 🚀 How to Run the Lab

1. Install DVWA on Ubuntu
2. Configure Apache logging
3. Install Splunk Enterprise
4. Install Splunk Forwarder on Ubuntu
5. Forward logs to Splunk
6. Run attack tools from Kali Linux
7. Analyze logs using SPL queries
