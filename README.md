# Windows LAPS Deployment in Active Directory
## Overview 🔍
This project demonstrates the deployment of Windows Local Administrator Password Solution (LAPS) in an Active Directory envrionment. It highlights how to secure manage and rotate local administrator passwords, reduce lateral movement risk, and enforce least-privellege access for IT support Staff.
## Technologies Used 💻
- Windows Server 2022 (Domain Controller)
- Windows 11 Client (Domain-joined)
- Active DIrectory Domain Services
- Windows LAPS
- Group Policy Management
- PowerShell
## Architecture Summary 
This project uses a single Active Directory Domain with one Domain Controller and a domain-joined Windows client. Group Policy is used to configure LAPS, and PowerShell is used to assign permissions to an authorised party to view the passwords.
## Security Objectives 🔒
- Prevent reuse of local administrator passwords
- Enforce least-privellege access
- Reduce lateral movement risk
- Provdide audability for admin access
