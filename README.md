# IT-Infrastructure-Monitoring-Active-Directory-Lab-Endpoint-Management
Designed and implemented an enterprise-style lab demonstrating Windows Server, Active Directory, RBAC, endpoint management, and infrastructure monitoring to improve visibility into endpoint health, network performance, device management, and issues such as latency spikes, packet loss, network congestion, and limited visibility of connected systems.
# Enterprise Infrastructure Monitoring & Active Directory Lab

## Project Overview

This project is a virtualized **enterprise infrastructure lab** designed to simulate core **systems administration**, **endpoint management**, and **infrastructure monitoring** workflows used in real IT environments. The lab combines **Windows Server 2022**, **Active Directory Domain Services (AD DS)**, **DNS**, **domain-joined Windows endpoints**, and a **Linux-based Zabbix monitoring server** to create a centralized environment for identity management, host monitoring, service visibility, and network-focused monitoring.

The main goal of the project is to improve visibility into **endpoint health**, **host availability**, **service status**, and **network performance** in a controlled enterprise-style lab. It also demonstrates how centralized monitoring can help identify and respond to issues such as **latency spikes**, **packet loss**, **network congestion**, **offline endpoints**, and limited visibility of connected systems.

This lab was built to strengthen practical skills in:

- **Windows Server administration**
- **Active Directory (AD DS)**
- **DNS**
- **Role-Based Access Control (RBAC)**
- **Linux server administration**
- **Zabbix monitoring**
- **Host and service monitoring**
- **Infrastructure observability**
- **Network-focused monitoring**
- **Alerting and dashboarding**

  
<img width="2527" height="1276" alt="image" src="https://github.com/user-attachments/assets/64871445-ae88-472e-b066-74f9933a639a" />

 
<img width="2555" height="1279" alt="image" src="https://github.com/user-attachments/assets/c01b774d-cc31-45f9-96b7-5e0fb2d64198" />

<img width="2511" height="1271" alt="image" src="https://github.com/user-attachments/assets/835f4330-5d45-4e25-b3d2-c97af1c6f923" />

<img width="2560" height="1315" alt="image" src="https://github.com/user-attachments/assets/40324bfc-9aa0-4c1e-9f4c-1ca61a02cc75" />



---

## Objectives

- Build a **Windows Server 2022** lab with **Active Directory Domain Services (AD DS)** and **DNS**
- Configure **Organizational Units (OUs)** and basic **Role-Based Access Control (RBAC)**
- Join Windows client systems to the domain
- Deploy a **Linux-based Zabbix Server**
- Configure agent-based monitoring on Windows and Linux hosts
- Monitor host availability, services, and performance metrics
- Build the foundation for **alerts**, **dashboards**, **discovery**, and **asset visibility**
- Simulate a centralized enterprise monitoring workflow

---

## Lab Architecture

The lab currently includes the following systems:

- **DC01** — Windows Server 2022 virtual machine hosting **Active Directory** and **DNS**
- **LABPC** — Domain-joined Windows client virtual machine simulating an enterprise endpoint
- **MONITOR01** — Ubuntu Server virtual machine hosting the **Zabbix monitoring platform**
- **Zabbix Server** — Centralized monitoring platform used for host visibility, service tracking, and alerting

### High-Level Architecture

```text
+----------------------+
|      MONITOR01       |
| Ubuntu + Zabbix      |
| 192.168.56.20        |
+----------+-----------+
           |
           |
     192.168.56.0/24
           |
  +--------+---------+
  |                  |
  |                  |
+------+         +--------+
| DC01 |         | LABPC  |
| AD   |         | Client |
| DNS  |         | Domain |
+------+         +--------+
