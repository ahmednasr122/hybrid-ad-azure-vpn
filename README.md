# Hybrid AD Infrastructure with Azure Site-to-Site VPN
Hybrid Active Directory infrastructure with Site-to-Site VPN integration using Azure.


## 📌 Project Overview
This project demonstrates a **Hybrid Active Directory infrastructure** that connects on-premises and cloud environments using **Azure Site-to-Site VPN**.

---

## 🛠️ Key Components
- **On-Premises Domain Controller (iti.local)**
  - OUs for IT, HR, Marketing, and Sales
  - Users with home folders & roaming profiles (for IT)
  - Group Policies: drive mapping, control panel restriction, USB blocking, unified wallpaper
  - File Services with FSRM (quota & file screening)
  - Windows Deployment Services (WDS) for automated OS + app deployment

- **Cloud Integration**
  - Site-to-Site VPN between on-premises and Azure
  - Azure VM joined to on-premises domain
  - Promoted as a **Child Domain Controller (zag.iti.local)**

---

## 🎯 Key Learning Points
- Enterprise AD design & management
- Secure file & resource management
- Hybrid cloud integration with Azure
- Real-world enterprise deployment simulation

---

## 📂 Resources
- [LinkedIn Post]((https://lnkd.in/p/d5AnGGfG))
