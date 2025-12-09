# HomeLab Infrastructure

*Foundation for virtualization, networking, and secure access in my enterprise-style HomeLab.*

---

## 🧭 Table of Contents
- [Overview](#overview)
- [Hardware Overview](#hardware-overview)
- [Virtualization Layout](#virtualization-layout)
- [Network Architecture](#network-architecture)
- [OPNsense as Core Gateway](#opnsense-as-core-gateway)
- [Remote and Secure Access](#remote-and-secure-access)
- [Monitoring Integration](#monitoring-integration)
- [Key Skills Demonstrated](#key-skills-demonstrated)
- [Related Projects](#related-projects)

---

## Overview
This project provides the **physical and virtual foundation** for my entire HomeLab environment.  
It includes real server hardware, VLAN-based segmentation, virtualization platforms, and a dedicated firewall.
All other projects in this portfolio run on top of this infrastructure.

---

## Hardware Overview
The following hardware stack powers the full lab environment.  
Each system is assigned a dedicated role in networking, virtualization, or AI workloads.

<p align="center">
<img src="./screenshots/Home_Lab_01.png" width="600">
</p>
<p align="center"><i>Figure: Physical HomeLab rack with numbered components</i></p>

| No. | Hardware | Specs | Host OS | Primary Role |
|----:|----------|-------|---------|--------------|
| 1 | Patch Panel | CAT6 | — | Structured cabling |
| 2 | Cisco 3750G | 24 Ports Gigabit + SFP | Cisco IOS | Managed core switch |
| 3 | Thinkcentre M710q | i3-6100T, 8GB RAM, 256GB SSD | OPNsense | Firewall / Routing / DHCP |
| 4 | Thinkcentre M710q | i3-6100T, 8GB RAM, 256GB SSD | Proxmox 01 | Test host / VMs |
| 5 | Supermicro X11 | Xeon E3-1270, 48GB RAM, 2×1TB SSD | VMware ESXi | AD, DNS, File Services, Monitoring |
| 6 | Asus Prime Z-590 + GTX 1060 | i5-11600KF, 32GB RAM, 500GB SSD | Ubuntu Server | AI Inference / GPU workloads |

---

## Virtualization Layout
The infrastructure combines both **Proxmox VE** and **VMware ESXi** to simulate mixed technology environments:

- **Proxmox** — lightweight lab testing environment
- **ESXi** — enterprise-grade virtualization for Windows Server roles

Out-of-band management provided via:
- **IPMI** on the Supermicro host
- **Dedicated Management VLAN** for secure remote access

---

## Network Architecture

> Segmented multi-VLAN network ensuring security, performance and traffic isolation

<p align="center">
<img src="./screenshots/architecture_01.png" width="950">
</p>
<p align="center"><i>Figure: Logical network topology with VLAN and firewall enforcement</i></p>

### VLAN Overview

| VLAN | Subnet | Zone / Purpose | Example Systems |
|-----:|--------|----------------|----------------|
| 10 | 10.0.10.0/24 | Services | AD, DNS, Nextcloud, AI  |
| 20 | 10.0.20.0/24 | IT Clients | Win 11 IT workstations |
| 21 | 10.0.21.0/24 | HR Clients | Win 11 HR workstations |
| 30 | 10.0.30.0/24 | Management | Monitoring, SSH, Admin tools, ESXi MGMT |
| 40 | 10.0.40.0/24 | Testing | Proxmox testing |

### Traffic Principles
- Strict segmentation ensures **least privilege network access**
- Inter-VLAN routing controlled exclusively by OPNsense
- No direct communication between IT & HR networks

---

## OPNsense as Core Gateway
OPNsense runs on Server 01 and acts as:

- **Firewall**
- **Router**
- **DHCP server for client VLANs**
- Security enforcement point

Features enabled:
- Stateful firewalling between departments
- Uplink to home router for controlled WAN access
- DNS forwarding for AD integration
- Dedicated admin-only VLAN

---

## Remote and Secure Access

> Full management access from anywhere — without exposing services publicly

To reach HomeLab networks from external devices:

- **VPN** for secure encrypted access
- **Static Routes** configured on FritzBox home router  
  → Directs VLAN traffic to OPNsense gateway

This ensures:
✔ No port forwarding / public exposure required  
✔ Admin access limited to authorized devices only

---

## Monitoring Integration

This infrastructure is fully monitored by **Icinga**.

Monitoring coverage:
- Firewall, virtualization hosts, AD services
- Network reachability per VLAN
- CPU/RAM/Disk for core services

(Full details in the dedicated **Monitoring** project)

---

## Key Skills Demonstrated

- Enterprise networking with VLANs, routing & segmentation  
- Windows + Linux based infrastructure mix  
- Virtualization administration (Proxmox + ESXi)  
- Infrastructure Security & Zero-Trust principles  
- Remote access & IP addressing strategies  
- Rack building, hardware configuration & cabling  

---

## Related Projects

- [02-enterprise-infrastructure](https://github.com/Hikko218/homelab-portfolio/tree/main/02-enterprise-infrastructure) 
- [03-monitoring](https://github.com/Hikko218/homelab-portfolio/tree/main/03-monitoring) 
- [04-ai-inference-server](https://github.com/Hikko218/homelab-portfolio/tree/main/04-ai-inference-server)  
- [05-nextcloud-server](https://github.com/Hikko218/homelab-portfolio/tree/main/05-nextcloud-server) 

---

📌 *This foundation enables all current and future service deployments in my HomeLab.*
