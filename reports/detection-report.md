# 📊 Detection Engineering Report

---

# 📌 Executive Summary

This project focuses on the development and implementation of detection rules to identify malicious activities within a simulated SOC environment using SIEM tools.

Multiple detection use cases were created to identify common attack techniques such as brute force attempts, PowerShell-based execution, and suspicious process behavior. These detections were mapped to the MITRE ATT&CK framework to align with industry standards.

---

# 🎯 Objectives

* Design and implement detection rules
* Identify suspicious activities from system logs
* Improve visibility into endpoint behavior
* Simulate real-world SOC detection workflows

---

# 🧰 Environment Details

* SIEM Tool: Splunk
* Log Sources:

  * Windows Security Logs
  * Sysmon Logs
* Data Source:

  * Simulated attack activity from Kali Linux

---

# 🏗️ Detection Use Cases Implemented

---

## 🚨 1. Brute Force Attack Detection

### Description

Detects repeated failed login attempts that may indicate password guessing attacks.

### Log Source

* Windows Event ID: 4625

### Detection Logic

Triggers when multiple failed login attempts occur from a single source within a defined threshold.

### Risk Level

High

### MITRE ATT&CK Mapping

* T1110 – Brute Force

---

## ⚠️ 2. PowerShell Activity Detection

### Description

Monitors execution of PowerShell processes which may indicate malicious or unauthorized script execution.

### Log Source

* Sysmon Event ID: 1

### Detection Logic

Identifies PowerShell execution based on process creation logs and command-line arguments.

### Risk Level

Medium

### MITRE ATT&CK Mapping

* T1059 – Command and Scripting Interpreter

---

## 🧪 3. Suspicious Process Detection

### Description

Identifies unusual or unexpected processes that may indicate malicious activity.

### Log Source

* Sysmon Event ID: 1

### Detection Logic

Analyzes process execution patterns and flags uncommon or suspicious processes.

### Risk Level

Medium

### MITRE ATT&CK Mapping

* T1204 – User Execution

---

## 🔍 4. Suspicious Parent-Child Process Detection

### Description

Detects abnormal process relationships such as command prompt spawning PowerShell, often used in attacks.

### Log Source

* Sysmon Event ID: 1

### Detection Logic

Flags unusual parent-child relationships in process execution.

### Risk Level

High

### MITRE ATT&CK Mapping

* T1059 – Command Execution

---

# 🔎 Analysis & Findings

* Multiple failed login attempts were successfully detected using threshold-based logic
* PowerShell execution was observed and analyzed through command-line monitoring
* Process activity logs provided insights into system behavior
* Parent-child relationships helped identify potentially malicious execution chains

---

# ⚠️ Challenges Faced

* Filtering noisy logs
* Identifying meaningful patterns
* Setting appropriate thresholds to avoid false positives

---

# 🛡️ Recommendations

* Implement multi-factor authentication (MFA)
* Apply account lockout policies
* Monitor PowerShell usage closely
* Use allowlisting for trusted applications
* Continuously update detection rules

---

# 🚀 Future Improvements

* Integrate threat intelligence feeds
* Automate detection rules
* Expand use cases (lateral movement, persistence, exfiltration)
* Add MITRE ATT&CK coverage mapping dashboard

---

# 🧠 Skills Demonstrated

* Detection Engineering
* SIEM (Splunk)
* Log Analysis
* Threat Hunting
* MITRE ATT&CK Mapping

---

# 📊 Conclusion

This project demonstrates the practical implementation of detection engineering techniques in a SOC environment. It highlights the ability to design detection logic, analyze logs, and identify potential threats using industry-standard frameworks and tools.

---
