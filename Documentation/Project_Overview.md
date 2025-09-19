# Project Overview – Hybrid Active Directory Infrastructure

## 📌 Project Description
This project demonstrates the design and deployment of a **Hybrid Active Directory environment** with complete integration of on-premises and cloud resources.  
It covers:
- Active Directory Domain Services (AD DS) setup
- OU and user management
- File Services with FSRM
- Group Policy configurations
- WDS deployment with captured images
- VPN integration with Microsoft Azure
- Child domain configuration

---

## 🌐 Domain Structure
- **Parent Domain:** `iti.local`
- **Child Domain:** `zag.iti.local`

---

## 🖥️ Environment Setup
- **DC1:** Windows Server 2019 – Parent Domain Controller (`iti.local`)
- **DC2:** Windows Server 2019 – Child Domain Controller (`zag.iti.local`)
- **Client Machines:** Windows 10/11 – joined to the domain
- **Azure VM:** Joined to the same network via site-to-site VPN

---

## 🗂️ Active Directory & User Management
- Created **Organizational Units (OU):**
  - IT
  - HR
  - Marketing
  - Sales
- Added users inside each OU
- Configured **Home Folders** for all users
- Enabled **Roaming Profiles** for IT OU

---

## 📂 File Services
- Created **File Shares** for each department:
  - `\\DC1\IT`
  - `\\DC1\HR`
  - `\\DC1\Marketing`
  - `\\DC1\Sales`
- Installed **FSRM (File Server Resource Manager)**
- Configured:
  - **File Screening** to block unwanted files
  - **Quotas** for each share

---

## 🛠️ Group Policies (GPOs)
- **Drive Mapping:** Automatic mapping of department shares  
- **Restrictions:**  
  - Block Control Panel for Sales & Marketing  
  - Block USB for HR, Marketing, Sales  
- **Desktop Background:** Enforced same wallpaper across all users  

---

## 💾 Windows Deployment Services (WDS)
- Installed and configured **WDS**
- Created a **Capture Image** from a reference Windows client
- Deployed captured image to new clients via PXE boot
- Pre-installed applications included in the image for user productivity

---

## 🔗 Azure Site-to-Site VPN
- Configured **VPN tunnel** between on-premises environment and Azure
- Deployed a **VM in Azure** within the same network
- Joined Azure VM to `iti.local`
- Promoted it as a **Child Domain Controller** (`zag.iti.local`)

---

## 📊 Key Outcomes
- Centralized user and resource management
- Secure file access and controlled storage
- Automated OS deployment with pre-configured apps
- Enforced security policies via GPOs
- Hybrid integration with Azure for scalability

---


