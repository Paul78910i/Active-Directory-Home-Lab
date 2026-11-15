# Enterprise Active Directory & Group Policy Home Lab

## 🚀 Project Overview
A fully functional, isolated enterprise IT environment built using Oracle VirtualBox. This project demonstrates core System Administration competencies including Active Directory Domain Services (AD DS) deployment, DNS configuration, client machine domain joining, Organizational Unit (OU) structuring, and Group Policy Object (GPO) security enforcement.

---

## 🛠️ Lab Architecture & Environment
* **Domain Controller (`DC01`):** Windows Server 2022
* **Client Workstation (`Client01`):** Windows 10 Pro
* **Virtualization Platform:** Oracle VirtualBox
* **Networking:** Internal Network (Isolated virtual switch configuration ensuring secure domain communication)

---

## 📋 Implementation Steps

### 1. Domain Controller Setup (`DC01`)
* Deployed Windows Server 2022 and configured a static IP address.
* Installed the **Active Directory Domain Services (AD DS)** and **DNS Server** roles.
* Promoted the server to a new forest domain (`corp.local`).

### 2. Virtual Networking & Client Join (`Client01`)
* Configured an internal virtual network adapter on both VMs to isolate lab traffic.
* Configured `Client01` to point its primary DNS to `DC01`.
* Joined `Client01` to the `corp.local` domain and established secure machine authentication.

### 3. Identity & Access Management (IAM)
* Created a custom Organizational Unit (OU) named **`IT team`**.
* Created and populated domain user accounts and security groups within the OU.
* Moved the `Client01` computer object into the `IT team` OU for centralized targeting.

### 4. Group Policy Object (GPO) Configuration & Enforcement
* Created a custom GPO (`User_Restrictions`) in the **Group Policy Management Console (`gpmc.msc`)**.
* Linked the GPO directly to the **`IT team`** OU.
* Configured **User Configuration** policies to lock down the environment (e.g., *Prohibit access to Control Panel and PC settings*).
* Verified policy synchronization and enforcement on `Client01` using `gpupdate /force` and runtime validation.

---

## 🔍 Key Skills Demonstrated
* Windows Server 2022 & Active Directory Administration
* DNS and Internal Network Configuration
* User & Computer Object Provisioning within OUs
* Group Policy Object (GPO) Creation, Linking, and Security Enforcement
* Troubleshooting and Policy Propagation Verification (`gpupdate`, Event Viewer)


<img width="1916" height="1046" alt="Screenshot 2026-11-15 235836" src="https://github.com/user-attachments/assets/52e4c6dc-52d9-4e77-a4a2-53b8a5d41c71" />

<img width="1913" height="1050" alt="Screenshot 2026-11-16 002322" src="https://github.com/user-attachments/assets/a2be2940-f2d3-4d93-bc4c-cd91e686c25f" />

<img width="1910" height="1078" alt="Screenshot 2026-11-16 002645" src="https://github.com/user-attachments/assets/617cc67f-b7bd-410b-bf31-1f10183d9299" />





