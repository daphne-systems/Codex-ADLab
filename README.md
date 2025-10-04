
<p align="center">
<img width="415" height="439" alt="image" src="https://github.com/user-attachments/assets/df96bc33-cab8-46bb-abb9-735396d228e2" />
</p>
<p align="center">
A custom-built AD lab project simulating a mid-sized company, designed for IT learning and experimentation.
</p>

---

## 📖 Company Background – Codex Systems
Codex Systems was founded by technologists who loved literature. Their vision is to **preserve, analyze, and share human knowledge** using modern technology.  

This fictional company serves as the foundation for our Active Directory lab environment. By blending story with technology, we create a more engaging and realistic enterprise IT simulation.  

---

## 🏢 Organizational Units (Departments)
For Phase 1, Codex Systems has been mapped into OUs representing real-world departments:

- **IT Infrastructure** – Systems, networking, helpdesk.  
- **Knowledge Engineering** – Developers and data scientists.  
- **Publishing & Media** – Editors, creative specialists.  
- **Operations** – HR, Finance, Legal, Admin.  

Each department is represented as its own **Organizational Unit (OU)** under the root **Codex Systems OU**.  

---

## 🛠️ Lab Configuration (Phase 1 Setup)
### Domain Controller
- **Server Name:** `DC-1`  
- **Role:** Domain Controller for `codex.local`  
- **Networking:** Static IP configured

  <img width="1718" height="920" alt="image" src="https://github.com/user-attachments/assets/6135b104-0477-46db-a567-63f822bd48f1" />
<img width="1718" height="920" alt="image" src="https://github.com/user-attachments/assets/8c216e7e-bfca-4143-90fc-6b394ee7e4f2" />



### Client Machine
- **Machine Name:** `Client-1`  
- **Role:** Domain-joined workstation  
- **Networking:** Configured on same subnet as DC-1
  
<img width="1024" height="768" alt="image" src="https://github.com/user-attachments/assets/dd44accf-9585-43a3-9abd-3ac21031f8af" />

 <img width="1024" height="768" alt="image" src="https://github.com/user-attachments/assets/3b54f7c3-f8f8-4e36-a6e7-6273b07f8836" />


✅ Client-1 was able to **register with the domain** successfully.  

---

## ✅ Completed in Phase 1
- Domain installed and configured (`codex.local`).  
- Root OU created: **Codex Systems**.  
- Department-level OUs established (IT, Knowledge Engineering, Publishing, Operations).  
- Client-1 joined to the domain.  

---

## 🔮 Next Steps (Phase 2 Preview)
- Populate users in each department (Executive, IT, Research, Publishing, Operations, Sales).  
- Establish baseline Group Policy Objects (password complexity, lockout policies).  
- Begin testing with domain logins from Client-1.  
---

## 📂 Repository Notes
- This file (`01_AD_Setup.md`) is part of the **Codex Systems Lab Series**.  
- Each phase will be documented in `/docs` as the environment grows:  
  - `01_AD_Setup.md` → Active Directory setup  
  - `02_GPOs.md` → Group Policy Objects  
  - `03_Networking.md` → Networking & Security Extensions  
