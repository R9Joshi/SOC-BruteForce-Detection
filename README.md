# SOC-BruteForce-Detection
Detection &amp; Incident Response of Brute Force Attacks using SIEM (CSA Project)

# 🚨 SOC L1 Project – Detecting Brute Force Attack on SSH

## 📌 Objective
Simulate and detect a brute force attack on an SSH service using Linux logs.  
This project demonstrates how a SOC Level-1 Analyst identifies suspicious login attempts from system logs.

---

## ⚙️ Environment Setup
- **OS:** Kali Linux
- **Service:** OpenSSH
- **User:** `testuser`
- **Tools Used:** Hydra, journalctl, grep

---

## 🔹 Steps Performed

### 1️⃣ Enable SSH Service
```bash
systemctl enable ssh
systemctl start ssh
systemctl status ssh

