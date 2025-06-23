# Nmap-Port-Scanning-Wireshark-Analysis

## 🎯 Objective
To perform basic network reconnaissance by scanning the local network for open ports using **Nmap**, and optionally analyze traffic using **Wireshark** to observe packet-level interactions.

---
## 🛠 Tools Used
- **Nmap** (v7.97) – for scanning network devices and identifying open TCP ports
- **Wireshark** – for packet capture and analysis
- *Operating System*: Windows 11

## 📡 Nmap Scan Summary

### 🔹 Network Scanned:
Command: nmap -sS 192.168.1.0/24

## 🔐 Security Observations

- **FTP (21)** and **HTTP (80)** are open on the router — may expose services if not secured properly.
- **SMB ports (135, 139, 445)** are open on the local machine — commonly targeted by ransomware; should be firewalled.
- One device (192.168.1.3) has all ports filtered — likely a hardened or firewalled host.

---

## 🧪 Wireshark Analysis

- Captured live packets while scanning.
- Observed **IGMPv3 Membership Query packets** from `192.168.1.1` to `224.0.0.1` (normal multicast activity).
- Applied IP filter: `ip.addr == 192.168.1.1`
- Verified that the router actively sends multicast queries.

---

## 📎 Files Included

- `report.xml` – Nmap output
- `Screenshot_Nmap.png` – Nmap capture result
- `Screenshot_Wireshark.png` – Wireshark capture result
- `Nmap_Wireshark_Task_Report.pdf` - Complete Analysis Report
- `README.md` – Explanation of task steps and findings

  



