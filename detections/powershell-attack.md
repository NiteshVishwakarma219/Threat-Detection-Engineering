# ⚠️ PowerShell Attack Detection

---

# 📌 Description

This detection monitors suspicious PowerShell execution, which is commonly used by attackers for fileless malware and lateral movement.

---

# 🧠 Detection Logic

Detect execution of PowerShell processes using Sysmon logs (Event ID 1).

---

# 📊 Log Source

* Sysmon Logs
* Event ID: 1 (Process Creation)

---

# ⚙️ Query Logic

Search for processes containing "powershell" in command line or image name.

---

# 🎯 MITRE ATT&CK Mapping

* **Technique ID:** T1059
* **Technique Name:** Command and Scripting Interpreter

---

# ⚠️ Severity

Medium

---

# 🔍 Investigation Steps

* Analyze command-line arguments
* Identify parent process
* Check for encoded or obfuscated commands

---

# 🛡️ Recommended Actions

* Restrict PowerShell usage
* Enable PowerShell logging
* Monitor suspicious scripts

---
