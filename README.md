
<p align="center">
<img width="557" height="154" alt="image" src="https://github.com/user-attachments/assets/21d7af99-860c-47f4-9644-c4b50524dc33" />
</p>

---

This project documents the deployment of an **Active Directory (AD) environment** for the fictional company **Codex Systems**.  
The goal was to simulate how a real organization would structure, secure, and manage its domain through OUs, users, security groups, and Group Policy Objects (GPOs).  


## 📂 Repository Notes 
- This series will be documented in `/docs` as the environment grows:  
  - `01_AD_Setup.md` → Active Directory setup  
  - `02_OUs_and_Users.md` → Creating OUs and Users  
  - `03_GPO_and_Security_Groups.md` → Group Policy Objects & Security Extensions  

---

## Active Directory Setup

- Installed and configured **Windows Server 2025** as a Domain Controller.  
- Deployed **Active Directory Domain Services (AD DS)** and established the domain `codex.local`.  
- Verified that domain and DNS services were operating correctly.  

---

## Organizational Units and Users

- Created Organizational Units (OUs) to represent departments at Codex Systems (e.g., IT, HR, Finance, Sales).  
- Added fictional user accounts and assigned them to the appropriate OUs.  
- Configured passwords and logon details to reflect standard onboarding practices.  

---

## Security Groups

- Built **security groups** to streamline access management.  
- Groups were aligned with departments (e.g., “HR_Group”, “IT_Group”) and users were added to their respective groups.  
- This allowed centralized management of access rights without needing to adjust each user individually.  

---

## Group Policy Objects (GPOs)

Configured several GPOs to enforce company standards across the domain:

- **Password Policy** → Enforced complexity requirements and expiration rules.  
- **Desktop Wallpaper Policy** → Standardized the desktop background for all users.  
- **Disable Control Panel/Settings** → Restricted access for non-administrative accounts.  

---

## Results and Testing

- Verified that the **password policy** was enforced by attempting to set a weak password, which was blocked as expected.  
- This confirmed that Group Policies were applying correctly within the Codex Systems domain.  
- Other policies were configured and could be expanded upon for future testing.  

---

## Conclusion

Through this lab project, I successfully simulated the deployment of an enterprise-level **Active Directory environment** for Codex Systems.  

Key achievements included:  
- Standing up a domain controller and domain services  
- Structuring the domain with OUs to reflect company organization  
- Creating users and assigning them to their correct OUs  
- Managing access with security groups  
- Enforcing organizational standards using Group Policy  

By the end of this project, Codex Systems had a functioning Active Directory environment that demonstrates core identity and access management practices.  

---

## Future Enhancements

Additional improvements could include:  
- Implementing a logon banner for compliance  
- Redirecting user folders to network shares  
- Deploying printers automatically through GPO  
- Configuring auditing to track logon/logoff and security events  

---

## 📂 Repository Notes
- This file (`01_AD_Setup.md`) is part of the **Codex Systems Lab Series**.  
- This series will be documented in `/docs` as the environment grows:  
  - `01_AD_Setup.md` → Active Directory setup  
  - `02_OUs_and_Users.md` → Creating OUs and Users  
  - `03_GPO_and_Security_Groups.md` → Group Policy Objects & Security Extensions  
