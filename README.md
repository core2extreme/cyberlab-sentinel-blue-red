# 🛡️ Cybersecurity Lab: Blue/Red Teaming with Microsoft Sentinel

## Overview

This repository documents the design and setup of a **virtual cybersecurity lab** focused on hands-on experience in **Blue Team monitoring** and **Red Team simulation** using **Microsoft Sentinel**.

The lab simulates a realistic enterprise environment with segmented networks, multiple operating systems, firewall appliances, and custom detection logic written in KQL (Kusto Query Language).

> ⚠️ **Disclaimer:** This lab is built for educational purposes only. All systems are isolated and not exposed to the public internet. No real-world services or data are used.

---

## 🧰 Lab Features

- **SIEM Platform**: Microsoft Sentinel (via Azure)
- **Multi-Zone Network**:
  - Internal Network (Windows Domain)
  - DMZ (Linux-based public-facing services)
  - Attacker Zones (internal and external)
- **Firewalls**: 3x OPNsense virtual firewalls for segmentation
- **OS Mix**:
  - Windows Server 2022, Windows 10/11 clients
  - Ubuntu Server LTS, RHEL Developer Edition
- **Use Cases**:
  - Log ingestion & normalization
  - KQL-based detection queries
  - Automation with Playbooks (planned)
  - Red Team simulation (Stage 2)

---

## 🔧 Technologies Used

| Category           | Stack / Tools                          |
|--------------------|-----------------------------------------|
| SIEM               | Microsoft Sentinel                      |
| Virtualization     | VMware Workstation                      |
| Firewalls          | OPNsense                                |
| Servers & Clients  | Windows Server 2022, Windows 10/11, Ubuntu, RHEL |
| Logging            | Event Forwarding, Sysmon, Custom KQL    |
| Security Framework | MITRE ATT&CK (for simulation planning) |

---

## 🗺️ Lab Architecture (Simplified)

```
[Attacker VM]   [Internet]
      |             |
    [OPNsense] ←→ [DMZ Zone]
      |             |
  [Internal OPNsense Firewall]
      |
 [Internal Network]
      ├─ DC (Win Server)
      ├─ Client (Win 10/11)
      └─ SIEM Forwarders
```

_A full diagram is available in the `/diagrams` folder._

---

## 📄 Project Structure

```
/
├─ README.md
├─ LICENSE (MIT)
├─ diagrams/
│   └─ network-topology.png
├─ docs/
│   ├─ setup-overview.md
│   ├─ sentinel-kql-detections.md
│   └─ red-team-plans.md
├─ screenshots/
│   └─ sentinel-dashboard.png
└─ roadmap.md
```

---

## 🚀 Roadmap

- [x] Deploy Sentinel and connect log sources
- [x] Build Windows domain environment
- [x] Implement multi-zone firewall setup
- [ ] Create detection rules with KQL
- [ ] Develop Playbooks for automated response
- [ ] Simulate Red Team TTPs (MITRE-based)
- [ ] Add honeypots and deception techniques

---

## 🧠 Why This Lab?

> This lab is designed to develop and demonstrate practical skills in:
> - Detection engineering
> - Security monitoring
> - Adversary emulation
> - Incident response automation

---

## 📜 License

This project is licensed under the [MIT License](./LICENSE) – feel free to explore, adapt, and build upon it.

---

## 🙋‍♂️ Author

**core2extreme** – Cybersecurity enthusiast & hands-on learner  
Connect with me on [LinkedIn](https://www.linkedin.com/in/YOUR-PROFILE) *(optional)*
