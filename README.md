# 🔐 CyberArk Privileged Access Security (PAS) Lab – Full Enterprise Simulation

## 🎯 Objective
To simulate a full deployment of **CyberArk PAS v12.6** using a personal lab environment. This included:
- CyberArk Digital Vault
- PVWA (Password Vault Web Access)
- CPM (Central Policy Manager)
- PSM (Privileged Session Manager)
- Active Directory (Domain Controller)

This mirrors real-world enterprise infrastructure and demonstrates core skills in Privileged Access Management (PAM).

---

## 🧱 1. Virtual Environment Overview

Lab built using **VMware Workstation Pro 17** with the following VMs:

- `VAULT` – CyberArk Vault Server (`10.0.0.1`)
- `DC-01` – Domain Controller (`10.0.0.2`)
- `PVWA-CPM-PSM` – Shared VM for remaining components (`10.0.0.3`)

<p align="center">
  <img src="https://github.com/user-attachments/assets/ef41507d-fe8c-4c9e-9004-38fe14056104" width="75%"/>
</p>

---

## 🧩 2. Vault Setup

- Created and configured the `VAULT` VM
- Installed .NET prerequisites and **CyberArk Vault**
- Confirmed Vault was initialized using **PrivateArk Server**

<p align="center">
  <img src="https://github.com/user-attachments/assets/06e8002e-fcf6-4fab-b984-94c967c3af26" width="75%"/>
  <br><br>
  <img src="https://github.com/user-attachments/assets/fb00b66e-6ef6-4bac-945e-80db20e0cbe6" width="75%"/>
</p>

---

## 🧩 3. Active Directory Setup

- Set static IP: `10.0.0.2`, DNS: `127.0.0.1`
- Renamed machine to `DC-01` and promoted it to Domain Controller for `CYBERARK.COM`

<p align="center">
  <img src="https://github.com/user-attachments/assets/0d12ae23-7abe-44eb-93f6-151aa7d9d21e" width="75%"/>
</p>

---

## 🧩 4. PVWA, CPM, and PSM Setup on Shared VM

- Created new VM `PVWA-CPM-PSM`
- Set static IP: `10.0.0.3`, DNS: `10.0.0.2`
- Joined to domain `CYBERARK.COM`

<p align="center">
  <img src="https://github.com/user-attachments/assets/a7058cfb-626f-428a-b34e-5840a62a4d94" width="75%"/>
  <br><br>
  <img src="https://github.com/user-attachments/assets/eae5c60e-a3de-4840-bb9d-8d65be8d7756" width="75%"/>
</p>

---

## ✅ PVWA Installation

- Ran pre-installation PowerShell script
- Installed **PVWA**
- Verified access via browser

<p align="center">
  <img src="https://github.com/user-attachments/assets/4cd88a91-5b4d-4540-928d-8bea7bc8b77f" width="75%"/>
  <br><br>
  <img src="https://github.com/user-attachments/assets/fd5398f6-9648-47f5-b923-1832ef19307b" width="75%"/>
  <br><br>
  <img src="https://github.com/user-attachments/assets/ee7d191c-659c-41dc-81e2-8b0490438cd4" width="75%"/>
</p>

---

## ✅ CPM Installation

- Executed `CPM_PreInstallation.ps1`
- Installed and registered **Central Policy Manager**

<p align="center">
  <img src="https://github.com/user-attachments/assets/e58cfb79-00d4-4d5f-a980-3fc869b1e3f4" width="75%"/>
  <br><br>
  <img src="https://github.com/user-attachments/assets/2b4bd284-647f-4448-8bba-c9903a37f567" width="75%"/>
</p>

---

## ✅ PSM Installation

- Installed **Privileged Session Manager**
- Validated successful installation and service connection

<p align="center">
  <img src="https://github.com/user-attachments/assets/95a3a523-070d-4373-a707-3bcbe88bc3e2" width="75%"/>
  <br><br>
  <img src="https://github.com/user-attachments/assets/e04c5b7c-98de-4718-822b-740d23f94e62" width="75%"/>
</p>

---

## ✅ Final Validation in PVWA

Logged into PVWA and confirmed all components were connected and operational:

<p align="center">
  <img src="https://github.com/user-attachments/assets/109bcac9-e916-4447-8cfd-f506c876dad7" width="75%"/>
</p>

---

## 📚 Key Skills Gained

- Full **CyberArk PAS** deployment and configuration
- Domain Controller setup and integration
- PowerShell scripting for CyberArk installations
- Component interconnectivity and troubleshooting
- Web-based administration of PAM operations

---

## 💼 Why This Matters

This project demonstrates real-world capability to:

- Deploy and manage CyberArk security infrastructure
- Work across networked systems and AD environments
- Secure privileged credentials and manage user sessions

---

📌 _Lab built entirely using VMware Workstation 17 Pro with Windows Server 2016._

