# 🔐 CyberArk Privileged Access Security (PAS) Lab – Full Enterprise Simulation

## 🎯 Objective
To simulate a real-world deployment of **CyberArk PAS v12.6** using a personal lab built with VMware Workstation. The lab includes configuration of:
- Digital Vault
- PVWA (Password Vault Web Access)
- CPM (Central Policy Manager)
- PSM (Privileged Session Manager)
- Active Directory Domain Controller (AD)

This setup mirrors enterprise environments and demonstrates hands-on proficiency in Privileged Access Management (PAM).

---

## 🛠️ Lab Overview

### 🧱 1. Virtual Environment with 3 VMs
Set up using **VMware Workstation Pro 17**:

- `VAULT` (10.0.0.1)
- `Active Directory` – Domain Controller (10.0.0.2)
- `COMPONENTS` – PVWA, CPM, and PSM combined (10.0.0.3)

📸 _VM structure and network settings
<table>
  <tr>
    <td align="center"><b>VMware Workstation View</b><br><img src="https://github.com/user-attachments/assets/49564de8-ddbb-4165-8363-39a20652a0c4" width="800"/></td>
    <td align="center"><b>Vault IP Configuration</b><br><img src="https://github.com/user-attachments/assets/ef41507d-fe8c-4c9e-9004-38fe14056104" width="800"/></td>
  </tr>
</table>

<table>
  <tr>
    <td align="center"><b>AD VM IP Settings</b><br><img src="https://github.com/user-attachments/assets/654541b9-9f5e-4e35-b75b-ac6af60c8a5e" width="800"/></td>
    <td align="center"><b>COMPONENTS VM IP Settings</b><br><img src="https://github.com/user-attachments/assets/c9d73e17-7ec3-470c-9ffc-afed8b52f87e" width="800"/></td>
  </tr>
</table>

![VAULT-2025-05-26-20-25-39](https://github.com/user-attachments/assets/ef41507d-fe8c-4c9e-9004-38fe14056104)
![Screenshot_2](https://github.com/user-attachments/assets/49564de8-ddbb-4165-8363-39a20652a0c4)
![Active Directory-2025-05-28-21-01-23](https://github.com/user-attachments/assets/654541b9-9f5e-4e35-b75b-ac6af60c8a5e)
![PVWA-CPM-PSM-2025-05-28-20-26-34](https://github.com/user-attachments/assets/c9d73e17-7ec3-470c-9ffc-afed8b52f87e)



---

## 🧩 2. Vault Setup
- Created the `VAULT` VM and installed **VMware Tools**
- Installed .NET prerequisites and **CyberArk Vault**
- Vault successfully initialized and ready for connection

📸 _Screenshot of Vault installation success screen_
![VAULT-2025-05-26-20-42-57](https://github.com/user-attachments/assets/06e8002e-fcf6-4fab-b984-94c967c3af26)
![VAULT-2025-05-26-20-42-41](https://github.com/user-attachments/assets/fb00b66e-6ef6-4bac-945e-80db20e0cbe6)



---

## 🧩 3. Active Directory Domain Controller (AD)
- Created and renamed VM to `DC-01`
- Configured static IP: `10.0.0.2`, DNS: `127.0.0.1`
- Promoted to Domain Controller for `CYBERARK.COM`
- Enabled Remote Desktop

📸 _Screenshot of domain promotion or DC role install_

---

## 🧩 4. PVWA, CPM, and PSM on Shared VM
- Created a third VM named `COMPONENTS`
- Set static IP: `10.0.0.3`, DNS: `10.0.0.2`
- Joined domain `CYBERARK.COM`
- Enabled Remote Desktop, installed .NET & VMware Tools

---

### ✅ PVWA Installation
- Ran PowerShell pre-installation script
- Installed **PVWA**
- Accessed `https://10.0.0.3/PasswordVault` in browser and logged in

📸 _PVWA login page screenshot_  
📍 *Open browser in VM → go to `https://<PVWA-IP>/PasswordVault`*

---

### ✅ CPM Installation
- Executed `CPM_PreInstallation.ps1`
- Installed **CPM** and registered with Vault

📸 _PowerShell output or CPM install success screen_

---

### ✅ PSM Installation
- Completed PowerShell setup steps
- Installed **PSM**
- Verified connection to Vault and service status

📸 _PSM installation or service status screenshot_

---

## ✅ 5. Final Validation in PVWA
- Logged into PVWA and confirmed:
  - Vault: ✅ Connected
  - CPM: ✅ Connected
  - PSM: ✅ Connected

📸 _Screenshot of PVWA dashboard showing component connectivity_

---

## 📚 What I Learned
- How to deploy and configure the full **CyberArk PAS ecosystem**
- Setup of AD, DNS, static IPs, domain join, and service registration
- Executed and interpreted PowerShell install scripts
- Gained working knowledge of PAM workflows: credential vaulting, session control

---

## 💼 Why It Matters
This lab proves hands-on capability with:
- CyberArk infrastructure setup
- Active Directory integration
- Secure session & credential management

---

📌 _Built fully on VMware Workstation 17 Pro in a local lab using Windows Server 2016 VMs._
