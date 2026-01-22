# splunkhomelab using virtualbox

This repository documents the deployment of a **Cybersecurity Home Lab** designed to simulate attacks and practice threat detection. Built on **VirtualBox** (Kali Linux & Windows 10), it leverages **Sysmon** for advanced telemetry and **Splunk Enterprise** for centralized log analysis

🛠️ Phase 0: Lab Prerequisites
Before configuring the network, the following environments were deployed on VirtualBox.

**Attacker:** [Kali Linux 2024.x (VirtualBox Image)](https://www.kali.org/get-kali/#kali-virtual-machines)
**Victim:** [Windows 10 (Official ISO Tool)](https://www.microsoft.com/en-us/software-download/windows10)
**Hypervisor:** [Oracle VirtualBox 7.0](https://www.virtualbox.org/wiki/Downloads)


## 🌐 Phase 1: Network Architecture
To simulate a realistic corporate LAN isolated from my home Wi-Fi, I created a custom **NAT Network**. This ensures the Attacker and Victim can communicate directly while remaining protected behind a virtual gateway.
### ⚙️ Configuration Steps
1.  Open VirtualBox **Network Manager** (`File` > `Tools` > `Network Manager`).
2.  Create a new NAT Network named `HackingLab`.
3.  **CIDR:** Set to `10.0.2.0/24` to define the subnet.
4.  **DHCP:** Enabled (to handle automatic IP assignment).

<img width="944" height="189" alt="v4ilkq5asL" src="https://github.com/user-attachments/assets/d755a8cb-031a-4678-ad0e-2412cdc96786" />

<img width="959" height="585" alt="cdW1vsMS8G" src="https://github.com/user-attachments/assets/7b2a4f61-a879-48f8-8a05-915ad613e001" />



