# 🚨 Brute Force Attack Detection

---

# 📌 Description

This detection identifies multiple failed login attempts within a short period, which may indicate a brute force attack attempting to gain unauthorized access.

---

# 🧠 Detection Logic

If a high number of failed login attempts (Event ID 4625) are observed from a single source within a defined time window, trigger an alert.

---

# 📊 Log Source

* Windows Security Event Logs
* Event ID: 4625 (Failed Login)

---

# ⚙️ Query Logic

Counts failed login attempts grouped by source IP and flags when threshold is exceeded.

---

# 🎯 MITRE ATT&CK Mapping

* **Technique ID:** T1110
* **Technique Name:** Brute Force

---

# ⚠️ Severity

High

---

# 🔍 Investigation Steps

* Identify source IP generating failed attempts
* Check frequency and time pattern
* Verify if attempts target multiple accounts

---

# 🛡️ Recommended Actions

* Enable account lockout policies
* Implement multi-factor authentication (MFA)
* Block suspicious IP addresses

---
