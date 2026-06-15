# Active Directory Simulation – CyberTech Solutions

This project demonstrates the deployment of a **Windows Server Domain Controller (Active Directory)** for a simulated organization, **CyberTech Solutions**. It covers domain setup, client integration, OU structuring, Group Policy implementation, and access control in an enterprise-like environment.

---

## 🏢 Company Structure

**CyberTech Solutions** is modeled as a small IT services firm with the following setup:

- 1 × Windows Server (Domain Controller)
- 1 × Windows 8 Client PC (Accounts Department)
- 1 × Windows XP Client PC (Legacy System)

---

## 🎯 Project Objectives

- Configure an Active Directory Domain Controller
- Join client machines to the domain
- Design Organizational Units (OUs)
- Implement Group Policies (GPOs)
- Simulate centralized identity and access management

---

## 🌐 Network Design

```
Internet
   ↓
Router (Gateway: 10.0.5.1)
   ↓
Switch
 ┌──────┬─────────────┬──────────────┐
 │      │             │              │
Server  PC1 (Win 8)   PC2 (Win XP)
```

| Device           | IP Address | Role                          |
|------------------|------------|-------------------------------|
| Windows Server   | 10.0.5.5   | Domain Controller (AD DS)     |
| Windows 8 PC     | DHCP       | Client (Accounts Department)  |
| Windows XP PC    | DHCP       | Legacy Client                 |

---

## 🖥️ Domain Configuration

- **Domain Name:** `cybertech.local`
- **Server Name:** `CYBERTECH`
- **IP Address:** `10.0.5.5` (Static)
- **Roles Installed:**
  - Active Directory Domain Services (AD DS)
  - DNS
  - DHCP

---

## 🗂️ Organizational Units (OUs)

Structured using **Active Directory Users and Computers (ADUC):**

```
CyberTech.local
├── OU: IT Department
│   ├── Alex.IT
│   └── Charles.IT
│
├── OU: Sales
│   └── Users
```

---

## 🔐 Group Policy (GPO)

Configured via **Group Policy Management Console (gpmc.msc):**

- **GPO Name:** `DisableRemovableDrives`
- **Linked To:** IT Department OU
- **Policy Path:**
  ```
  Computer Configuration → Administrative Templates → System → Removable Storage Access
  ```
- **Setting:**
  - **All Removable Storage Classes: Deny All Access → Enabled**

**Outcome:**  
USB and external storage devices are blocked for users within the targeted OU.

---

## 📸 Screenshots

- [Active Directory Domain Structure](https://github.com/your-username/your-repo/blob/main/screenshots/ad-structure.png)
- [GPO Configuration Screenshot](https://github.com/your-username/your-repo/blob/main/screenshots/gpo-config.png)
- [Client Joined to Domain](https://github.com/your-username/your-repo/blob/main/screenshots/domain-join.png)
- [USB Access Denied Result](https://github.com/your-username/your-repo/blob/main/screenshots/usb-denied.png)

> Replace the links above with your actual GitHub screenshot URLs.

---

## 🧠 Key Takeaways

- Hands-on experience deploying and managing Active Directory
- Implementation of centralized access control using GPOs
- Practical OU design aligned with organizational structure
- Real-world application of Identity and Access Management (IAM)

---

## 👤 Author

**Aliu B. Sanusi**  
Cybersecurity Analyst
