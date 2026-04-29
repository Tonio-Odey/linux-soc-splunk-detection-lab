# 🏗️ System Architecture

## 📌 Overview
This lab simulates a basic Security Operations Center (SOC) workflow where attacks are generated, logged, and detected using Splunk.

---

## 🔄 Data Flow

Kali Linux (Attacker)
        ↓
DVWA Web Server (Target - Ubuntu)
        ↓
System Logs (Apache & Auth Logs)
        ↓
Splunk Forwarder
        ↓
Splunk Enterprise (Detection & Analysis)

---

## 🧩 Components

### ⚔️ Attacker Machine (Kali Linux)
Used to simulate real-world attacks:
- Gobuster → directory enumeration
- Nikto → vulnerability scanning
- SQLmap → SQL injection
- Hydra → brute-force login attempts

---

### 🖥️ Target Machine (DVWA on Ubuntu)
A vulnerable web application used to receive attacks.

- Runs DVWA
- Uses Apache web server
- Generates:
  - Web logs (HTTP requests)
  - Authentication logs (login attempts)

---

### 📄 Log Sources
Logs generated on the target system include:

- `/var/log/apache2/access.log` → web traffic
- `/var/log/auth.log` → authentication activity

These logs capture attacker behavior.

---

### 🔄 Splunk Forwarder
Installed on the target machine to send logs to Splunk.

- Monitors log files
- Uses `inputs.conf`
- Sends data to Splunk via `outputs.conf`

---

### 📊 Splunk Enterprise (SIEM)
Central system used for detection and analysis.

- Ingests logs from forwarder
- Runs SPL queries
- Identifies malicious activity:
  - Brute force attacks
  - SQL injection attempts
  - Directory enumeration
  - Vulnerability scans

---

## 🧠 Detection Flow

1. Attack is launched from Kali Linux  
2. DVWA server receives the request  
3. Logs are generated on the server  
4. Splunk Forwarder sends logs to Splunk  
5. SPL queries analyze the logs  
6. Suspicious activity is detected  

---

## 🎯 Purpose

This architecture demonstrates how a SOC detects real-world attacks by:

- Simulating attacker behavior  
- Collecting logs from systems  
- Analyzing logs using SIEM  
- Identifying malicious patterns  

---

## 📌 Summary

This lab represents a simplified SOC pipeline:

**Attack → Logs → Forwarding → Detection → Evidence**
