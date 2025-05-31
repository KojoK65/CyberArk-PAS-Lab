# 🔐 CyberArk Privileged Access Security (PAS) Lab – Full Enterprise Simulation

## 🎯 Objective
To simulate a real-world deployment of **CyberArk PAS v12.6** using a personal lab built with VMware Workstation. The lab includes configuration of:
- Digital Vault
- PVWA (Password Vault Web Access)
- CPM (Central Policy Manager)
- PSM (Privileged Session Manager)
- Active Directory Domain Controller (AD)

This mirrors enterprise environments and demonstrates hands-on proficiency in Privileged Access Management (PAM).

---

## 🧱 1. Virtual Environment Setup

Created 3 virtual machines in **VMware Workstation Pro 17**:

- `VAULT` – CyberArk Vault Server (`10.0.0.1`)
- `Active Directory (DC-01)` – Domain Controller (`10.0.0.2`)
- `COMPONENTS` – Combined PVWA, CPM, PSM (`10.0.0.3`)

**Vault IP Configuration:**

<p align="center">
  <img src="https://github.com/user-attachments/assets/ef41507d-fe8c-4c9e-9004-38fe14056104" width="75%"/>
</p>

---

## 🧩 2. Vault Setup

- Installed **VMware Tools** and required **.NET Framework**
- Performed the full installation of **CyberArk Digital Vault**
- Verified Vault initialization via PrivateArk Server

**Vault Installation Confirmation:**

<p align="center">
  <img src="https://github.com/user-attachments/assets/06e8002e-fcf6-4fab-b984-94c967c3af26" width="75%"/>
  <br><br>
  <img src="https://github.com/user-attachments/assets/fb00b66e-6ef6-4bac-945e-80db20e0cbe6" width="75%"/>
</p>

---

## 🧩 3. Active Directory (AD) Setup

- Renamed VM to `DC-01`
- Set static IP: `10.0.0.2`, DNS: `127.0.0.1`
- Promoted to Domain Controller for the domain `CYBERARK.COM`

<p align="center">
  <img src="https://github.com/user-attachments/assets/0d12ae23-7abe-44eb-93f6-151aa7d9d21e" width="75%"/>
</p>

---

## 🧩 4. PVWA, CPM, and PSM on Shared VM

- Created third VM: `COMPONENTS`
- Set static IP: `10.0.0.3`, DNS: `10.0.0.2`
- Joined domain `CYBERARK.COM`
- Installed **VMware Tools** and required .NET framework

<p align="center">
  <img src="https://github.com/user-attachments/assets/a7058cfb-626f-428a-b34e-5840a62a4d94" width="75%"/>
  <br><br>
  <img src="https://github.com/user-attachments/assets/eae5c60e-a3de-4840-bb9d-8d65be8d7756" width="75%"/>
</p>

---

### ✅ PVWA Installation
- Ran PowerShell pre-install script
- Installed **Password Vault Web Access**
- Verified access via browser

<p align="center">
  <img src="https://github.com/user-attachments/assets/4cd88a91-5b4d-4540-928d-8bea7bc8b77f" width="75%"/>
  <br><br>
  <img src="https://github.com/user-attachments/assets/fd5398f6-9648-47f5-b923-1832ef19307b" width="75%"/>
</p>

📍 Navigated to: `https://10.0.0.3/PasswordVault`

<p align="center">
  <img src="https://github.com/user-attachments/assets/ee7d191c-659c-41dc-81e2-8b0490438cd4" width="75%"/>
</p>

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
