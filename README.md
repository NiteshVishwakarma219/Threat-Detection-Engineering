# 🚨 Threat Detection Engineering – SOC Analyst Project

![SOC](https://img.shields.io/badge/SOC-Detection-blue)
![SIEM](https://img.shields.io/badge/SIEM-Splunk-green)
![Status](https://img.shields.io/badge/Status-Completed-success)

---

# 📌 Overview

This project focuses on **Detection Engineering**, a critical function in a Security Operations Center (SOC).

It demonstrates how security analysts design and implement detection rules to identify malicious activities such as brute force attacks, PowerShell exploitation, and suspicious process execution using SIEM tools.

---

# 🎯 Objectives

* Develop real-world detection rules
* Identify malicious behavior from logs
* Create alerting mechanisms
* Map detections to MITRE ATT&CK framework

---

# 🧠 What is Detection Engineering?

Detection Engineering is the process of:

* Creating rules to detect threats
* Analyzing logs for suspicious patterns
* Improving security visibility

This project simulates how SOC analysts proactively detect cyber threats.

---

# 🧰 Tools & Technologies

* Splunk (SIEM Platform)
* Windows Event Logs
* Sysmon Logs

---

# 🏗️ Project Structure

```id="struc1"
Threat-Detection-Engineering/
│
├── detections/
├── queries/
├── reports/
├── screenshots/
└── README.md
```

---

# ⚙️ Implemented Detections

## 🚨 1. Brute Force Attack Detection

* Detects multiple failed login attempts
* Uses Windows Event ID 4625

📌 Logic:
Trigger alert if login failures exceed threshold

📂 Query:

```id="q1"
index=wineventlog EventCode=4625
| stats count by src_ip
| where count > 5
```

📌 MITRE ATT&CK:
T1110 – Brute Force

---

## ⚠️ 2. PowerShell Attack Detection

* Detects suspicious PowerShell execution
* Uses Sysmon logs

📂 Query:

```id="q2"
index=wineventlog EventCode=1
| search powershell
```

📌 MITRE ATT&CK:
T1059 – Command Execution

---

## 🧪 3. Suspicious Process Detection

* Identifies unusual processes

📂 Query:

```id="q3"
index=wineventlog EventCode=1
| stats count by Image
```

📌 MITRE ATT&CK:
T1204 – User Execution

---

# 🚨 Alerting Mechanism

Alerts are configured in Splunk to trigger when:

* Threshold conditions are met
* Suspicious patterns are detected

This ensures real-time threat detection.

---

# 📊 Screenshots

| Description          | File                       |
| -------------------- | -------------------------- |
| Detection Query      | screenshots/detection1.png |
| PowerShell Detection | screenshots/detection2.png |
| Alerts               | screenshots/alerts.png     |

---

# 📄 Detection Report

📂 Located in: `/reports/detection-report.md`

Includes:

* Detection summary
* Techniques used
* Observations

---

# 🧠 Skills Demonstrated

* Detection Engineering
* SIEM (Splunk)
* Log Analysis
* Threat Hunting
* MITRE ATT&CK Mapping

---

# 💼 Resume Highlight

✔ Developed custom detection rules in Splunk to identify brute force attacks, PowerShell-based threats, and suspicious processes, mapped to MITRE ATT&CK techniques.

---

# 🚀 Future Improvements

* Add more detection use cases
* Integrate threat intelligence feeds
* Automate detection rules

---

# ⭐ Conclusion

This project demonstrates practical experience in **Detection Engineering**, showcasing the ability to identify, analyze, and respond to cyber threats using SIEM tools.

---

# 🔗 Author

Nitesh Vishwakarma

---
