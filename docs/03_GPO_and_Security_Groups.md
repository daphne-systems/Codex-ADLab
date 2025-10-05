# Active Directory: GPOs, Security Groups, and Testing

<img width="804" height="404" alt="image" src="https://github.com/user-attachments/assets/0c4f8439-4f87-4b58-90d9-58357384acf8" />


Now that the domain is set up and we have OUs with users, the next step is to create **security groups**, apply **Group Policy Objects (GPOs)**, and test them to make sure everything works.

---

## 1. Creating Security Groups

1. Open **Active Directory Users and Computers (ADUC)**.  
2. Navigate to the OU where the group should live (e.g., IT, HR, Sales).  
3. Right-click → **New → Group**.  
4. You wanna give the group a descriptive name (e.g., `HR_Users`, `IT_Admins`).  
5. Choose:
   - **Group Scope**: Domain  
   - **Group Type**: Security  
6. Add users to the group and by right-clicking the group → **Properties → Members → Add**.  

<img width="1718" height="920" alt="DC-1-2025-10-04-21-39-03" src="https://github.com/user-attachments/assets/8632826e-268e-48bb-a305-fac8aa23aa7d" />
<img width="1718" height="920" alt="DC-1-2025-10-04-21-41-33" src="https://github.com/user-attachments/assets/ddb11641-726e-48de-a57a-6fe29b7b9be8" />

---

## 2. An easy way to create a default policy

1. Open **Group Policy Management** (type `gpmc.msc` in Run).  
2. click your domain and  → **Default Domain Policy...**  
3. Right click it and press → **Edit** .   
4. Configure the settings under:
   - **Computer Configuration** or **User Configuration** → Policies.  

<img width="1718" height="920" alt="DC-1-2025-10-04-23-01-55" src="https://github.com/user-attachments/assets/dc4e580d-52c9-4e04-9bfc-aeead93afb4c" />


## 3. Creating Group Policy Objects (GPO)-Intermediate Way

1. Open **Group Policy Management** (type `gpmc.msc` in Run).  
2. Right-click your domain or an OU → **Create a GPO in this domain, and Link it here...**  
3. Name it something descriptive (e.g., `PasswordPolicy`, `ControlPanelPolicy, `WallpaperPolicy`).  
4. Right-click the GPO → **Edit**.  
5. Configure the settings under:
   - **Computer Configuration** or **User Configuration** → Policies.  

<img width="1718" height="920" alt="image" src="https://github.com/user-attachments/assets/426dd486-47a8-4caa-b057-79e43db2cc38" />

- This was me setting up the 'PasswordPolicy' that would lockout a user after typing in the wrong password 4 times.
  
---


## 4. Testing the GPOs

1. Log in as a test user from the target OU.  
2. Run the command:  
   gpupdate /force
   

<img width="1024" height="768" alt="image" src="https://github.com/user-attachments/assets/4666d9e6-e4c7-4d17-a11b-66e67592c4bf" />

- Example of the Account Lockout Policy that I set up above.
