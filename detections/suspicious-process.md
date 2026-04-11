# 🧪 Suspicious Process Detection

---

# 📌 Description

This detection identifies unusual or potentially malicious processes running on the system.

---

# 🧠 Detection Logic

Monitor process creation events and identify anomalies based on uncommon process names or unexpected behavior.

---

# 📊 Log Source

* Sysmon Logs
* Event ID: 1 (Process Creation)

---

# ⚙️ Query Logic

Analyze process execution frequency and identify rare or suspicious processes.

---

# 🎯 MITRE ATT&CK Mapping

* **Technique ID:** T1204
* **Technique Name:** User Execution

---

# ⚠️ Severity

Medium

---

# 🔍 Investigation Steps

* Identify unusual process names
* Check execution path
* Analyze parent-child relationship

---

# 🛡️ Recommended Actions

* Restrict execution of unknown binaries
* Monitor system processes regularly
* Apply application whitelisting

---
