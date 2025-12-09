# Self-Hosted Nextcloud Server

A private cloud storage and collaboration service hosted in the HomeLab network.  
Designed for secure file access without relying on external cloud providers.

---

## Table of Contents
- [Purpose & Overview](#purpose--overview)
- [Tech Stack](#tech-stack)
- [Dashboard](#dashboard)
- [Setup & Configuration Summary](#setup--configuration-summary)
- [Security Measures](#security-measures)
- [Skills Demonstrated](#skills-demonstrated)
- [Related Projects](#related-projects)

---

## Purpose & Overview

This project provides **secure, local-first file synchronization** using Nextcloud.

It enables:

- Multi-device access to private files
- Group and user permissions using AD accounts *(planned future integration)*
- Extendability through apps (Calendar, Contacts, Tasks, Notes, etc.)
- Web access inside the HomeLab

> Fully self-hosted and not exposed to the public internet.

---

## Tech Stack

| Component | Details |
|----------|---------|
| OS | Ubuntu Server |
| Application | Nextcloud (Classic installation) |
| Web Server | Apache2 |
| Database | MariaDB |
| Language Runtime | PHP 8.x + required modules |
| Network Zone | Service VLAN (VLAN 10) |
| Firewall | OPNsense (no inbound WAN access) |

---

## Dashboard

<p align="center">
<img src="./screenshots/NextCloud_Dashboard.png" width="1050">
</p>

---

## Setup & Configuration Summary

1. **Ubuntu Server setup**
   - Static IP configuration
   - SSH enabled
   - UFW rules applied

2. **MariaDB database**
   - Database & user created for Nextcloud
   - Basic SQL permission hardening

3. **Nextcloud deployment**
   - Apache + PHP configuration
   - Nextcloud initialized via web installer
   - Data directory placed on local storage

4. **Initial Apps & Users**
   - Storage & sharing enabled
   - Admin account created
   - Local network access verified

---

## Security Measures

- Hosted internally only (**no WAN exposure**)
- Firewall rules limit access to HomeLab admin devices
- Database user limited to required permissions
- Systemd services automatically monitored
- HTTPS planned via local reverse proxy (future improvement)

> The focus is secure private usage — **not public cloud exposure**.

---

## Skills Demonstrated

- Linux server administration
- Web server configuration (Apache + PHP)
- Database provisioning & access control
- File-based cloud service deployment
- Firewall access management
- Secure HomeLab service hosting

---

## Related Projects

- [01-homelab-infrastructure](https://github.com/Hikko218/homelab-portfolio/tree/main/01-homelab-infrastructure)
- [02-enterprise-infrastructure](https://github.com/Hikko218/homelab-portfolio/tree/main/02-enterprise-infrastructure) 
- [03-monitoring](https://github.com/Hikko218/homelab-portfolio/tree/main/03-monitoring) 
- [04-ai-inference-server](https://github.com/Hikko218/homelab-portfolio/tree/main/04-ai-inference-server)  

---

📌 This service adds a practical, privacy-focused file collaboration option to the HomeLab.
