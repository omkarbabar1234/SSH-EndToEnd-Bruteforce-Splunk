# SSH End-to-End Brute-force Simulation, Detection & Prevention (Splunk)

**Author:** Babar Omkar Sukhdev  
**Institution:** Modern College, Nanded  
**Project Type:** SOC Lab / Academic Project  
**Year:** 2025

---

## 🎯 Project Overview

This project simulates SSH credential brute-force attacks (Hydra) against an Ubuntu target and demonstrates an end-to-end SOC workflow:

1. Generate SSH failed/successful auth events (Hydra).  
2. Ingest Linux `auth.log`into Splunk.  
3. Create correlation searches and alerts for brute-force and password-spray patterns.  
4. Visualize attacker IPs/timelines in Splunk dashboards.  
5. Block attacker IP(s) using UFW/iptables and verify prevention.

---

## 🧩 Lab Topology & Requirements

- **SIEM Server:** Ubuntu 22.04 + Splunk Enterprise (indexes: `auth`, `suricata`)  
- **Target Server:** Ubuntu 22.04 running `sshd` (test target)  
- **Attacker:** Kali Linux (Hydra; Metasploit optional)  
- **Network:** VirtualBox/VMware NAT or internal network  
- **Note:** Perform this lab only in an isolated, authorized environment.

---

## ⚙️ Preparation & Setup

1. **Enable password auth on target (lab only)**  
   Edit `/etc/ssh/sshd_config`:

