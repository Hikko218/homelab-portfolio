# HomeLab IT Infrastructure Portfolio
*Hands-on enterprise technologies in a virtualized learning environment*

---

## Table of Contents
- [About This Portfolio](#about-this-portfolio)
- [Skills & Focus Areas](#skills-focus-areas)
- [Core Architecture Overview](#core-architecture-overview)
- [Projects](#projects)
  - [01. HomeLab Infrastructure](#01-homelab-infrastructure)
  - [02. Enterprise Infrastructure Lab](#02-enterprise-infrastructure-lab)
  - [03. Network and System Monitoring](#03-network-and-system-monitoring)
  - [04. AI Inference Server](#04-ai-inference-server)
  - [05. Nextcloud Server](#05-nextcloud-server)
- [Remote and Secure Access](#remote-and-secure-access)
- [Purpose and Learning Goals](#purpose-and-learning-goals)
- [Contact](#contact)

---

## About This Portfolio

This repository serves as a **central entry point** to all of my HomeLab and IT-infrastructure projects.  
It replicates **real-world enterprise operations** using virtualization, network security, hybrid identity, monitoring, and self-hosted services.

> A hands-on enterprise lab — built for learning and gaining real IT operations experience.

Each project contains full documentation, diagrams, screenshots, and explanations of design decisions.

---

## Skills & Focus Areas

| Category | Topics | Experience Level |
|--------|--------|:--:|
| **Windows Infrastructure** | AD DS, GPO, WSUS, DNS, DHCP, Hybrid Identities | ⭐⭐⭐⭐ |
| **Networking & Security** | VLANs, Routing, Firewall Rules, VPN | ⭐⭐⭐⭐⭐ |
| **Virtualization** | Proxmox, VMware ESXi | ⭐⭐⭐⭐ |
| **Linux Server Administration** | Ubuntu Server, Apache, MariaDB | ⭐⭐⭐ |
| **Monitoring & IT Ops** | Icinga 2 + Web 2, Service Checks, Alerting | ⭐⭐⭐ |
| **Cloud Integration** | Microsoft Entra ID, SSO Concepts | ⭐⭐⭐ |

> Network architecture and segmentation are my strongest focus and passion areas.

---

## Core Architecture Overview

> *Virtualized multi-VLAN enterprise network with centralized identity and monitoring*

(Planned: architecture diagram in draw.io format.)

- Proxmox + ESXi virtualization hosts  
- Segmented VLAN design (IT / HR / Services / Management)  
- OPNsense as security gateway and routing core  
- Windows Servers + Linux services + GPU workloads  
- Central Icinga monitoring for visibility  

---

## Projects

---

## 01. HomeLab Infrastructure

Foundation for all services: hardware, virtualization, VLAN segmentation, routing, and out-of-band management.

**Key Skills**

- Network design and subnetting  
- Virtualization (Proxmox, ESXi)  
- NIC bonding, trunking, management networks  
- IPMI integration  

**Project Documentation:**  
[01-homelab-infrastructure](https://github.com/Hikko218/homelab-portfolio/tree/main/01-homelab-infrastructure)

---

## 02. Enterprise Infrastructure Lab

Realistic SMB/enterprise environment with identity, file services, update management, and security-driven segmentation.

**Features**

- Windows Server 2025 Domain Controller  
- GPO-based workstation management  
- Hybrid integration with Microsoft Entra ID  
- Firewall policies separating IT and HR clients  

**Project Documentation:**  
[02-enterprise-infrastructure](https://github.com/Hikko218/homelab-portfolio/tree/main/02-enterprise-infrastructure)

---

## 03. Network and System Monitoring

Icinga deployment for full infrastructure visibility across servers, clients, and networking equipment.

**Highlights**

- Service health checks  
- Alerting and status dashboards  
- Monitoring across VLANs  

**Project Documentation:**  
[03-monitoring](https://github.com/Hikko218/homelab-portfolio/tree/main/03-monitoring)

---

## 04. AI Inference Server

GPU-powered Ubuntu machine for LLM workloads and future automation projects.

**Capabilities**

- GPU acceleration (NVIDIA)  
- Container-ready design  
- Testing LLM inference locally  

**Project Documentation:**  
[04-ai-inference-server](https://github.com/Hikko218/homelab-portfolio/tree/main/04-ai-inference-server)

---

## 05. Nextcloud Server

Private cloud solution with local authentication and secure access inside the HomeLab.

**Stack**

- Ubuntu Server  
- Apache + PHP  
- MariaDB  
- File sync and collaboration  

**Project Documentation:**  
[05-nextcloud-server](https://github.com/Hikko218/homelab-portfolio/tree/main/05-nextcloud-server)

---

## Remote and Secure Access

To avoid exposing services to the public internet:

- VPN connections from trusted personal devices  
- Static routes configured on FritzBox,  
  routing all HomeLab subnets via **OPNsense** as the gateway  

> Secure and full access from anywhere — without compromising security.

---

## Purpose and Learning Goals

This HomeLab allows me to continuously improve my skills in:

- Enterprise identity and access management  
- Network segmentation and firewall security  
- Hybrid cloud operations  
- Linux service deployment  
- Monitoring and troubleshooting  

Built like a real environment — operated for learning.  
Always evolving with new technologies and projects.

---

## Contact

If you'd like to know more or collaborate, feel free to reach out.  
Happy to discuss IT infrastructure, networking, or HomeLab setups.
