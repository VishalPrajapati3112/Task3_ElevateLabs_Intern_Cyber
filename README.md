# Task3_ElevateLabs_Intern_Cyber
Perform a Basic Vulnerability Scan on Your PC.


# Task 3 – Vulnerability Assessment Using OpenVAS

This repository contains the setup and configuration steps for performing a vulnerability assessment using **OpenVAS (GVM)** on a Kali Linux system. The objective was to scan the local machine (`127.0.0.1`) for known vulnerabilities using updated feeds and standard scan configurations.

---

## 🔧 Tool & Environment

- **Tool**: OpenVAS (Greenbone Vulnerability Manager)
- **OS**: Kali Linux (Dual Boot)
- **GVM Version**: 25.x
- **Scanner**: OpenVAS 23.20.1
- **Database**: PostgreSQL 17.5

---

## ✅ Setup Summary

- Installed OpenVAS using `gvm-setup`
- Fixed PostgreSQL collation version mismatch
- Successfully synced:
  - GVMD_DATA
  - SCAP
  - CERT feeds
- Verified scanner using `gvmd --verify-scanner`
- Created:
  - Target: `127.0.0.1`
  - Scan Task using “Full and Fast” / “Base” config

---

## ⚠️ Issue Faced

Although the entire setup was successful, the **"Start Scan" (▶️)** button remained **disabled**, even after:
- Rebuilding gvmd cache
- Manually importing scan configs
- Restarting scanner and manager services

This appears to be a **known UI-desync bug in GVM 25.x** on Kali Linux, where scan execution is blocked despite valid config.

---

## 📁 Folder Structure
task-3-vulnerability-scan/
├── screenshots/
│ ├── target_created.png
│ ├── task_created.png
│ ├── scanner_verified.png
│ └── so on....
├── Task_3_OpenVAS_Report.pdf
└── README.md (this)



## 🧠 Learning Outcome

This task involved hands-on experience with:
- Vulnerability scanning tools
- Feed management and sync troubleshooting
- Scanner/daemon configuration
- Real-world debugging of database + UI level issues

---

📌 Even though the scan could not be executed, all configuration steps were completed, demonstrating readiness for vulnerability assessments in real-world environments.



