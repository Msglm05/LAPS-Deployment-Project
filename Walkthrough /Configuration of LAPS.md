# Configuration of LAPS
- To check whether the Laps module was installed, the command below was ran
<img width="500" height="467" alt="image" src="https://github.com/user-attachments/assets/2ed7eefd-e753-4444-841f-50d171b18e60" />

- If this command produces no output, updates may need to be carried on the Windows Server
---
### Updating the schema
- This enables the LAPS password to be stored in Active Directory along with others, in the attributes section of the target machines

<img width="650" height="108" alt="image" src="https://github.com/user-attachments/assets/8f6fad5f-0f29-4818-9556-3a79b0b94a7f" />

---
### Permission for the target machine
- This is required to enable the target machines to update their passwords in Active Directory
<img width="700" height="90" alt="image" src="https://github.com/user-attachments/assets/6f7bbd6b-efe9-4f25-85ad-bf13df1405e3" />

- In my case, the target OU 'Workstations' is nested another another OU 'Company'
---
### Permission to read the LAPS password 
- This is required to give permission for a security group to read the LAPS password in Active Directory
<img width="700" height="113" alt="image" src="https://github.com/user-attachments/assets/9c7eacee-0cc9-45d7-a0e2-0a6d4a5b7bd0" />

## Group Policy Enabled Settings:
- A GPO called 'LAPS' was created and edited by navigating to Computer Configuration > Policies > Administrative Templates > System > LAPS
- 'Configure password backup directory', selected the backup directory to Active Directory
<img width="370" height="632" alt="image" src="https://github.com/user-attachments/assets/18dea797-b44f-4a28-b02e-0abb989c7b04" />

- 'Password Settings'
<img width="370" height="625" alt="image" src="https://github.com/user-attachments/assets/65bd0d65-9a38-4840-b2c6-719cbaf322fd" />

- 'do not allow password expiration time longer than required by policy'
- Password encryption
- 'Configure authroised password decryptors', set the authenticated group 'LAPSAdmins' in my case
<img width="370" height="626" alt="image" src="https://github.com/user-attachments/assets/cbe014b1-4d4a-4efd-a9ff-4573befa8245" />


- GPO was linked to the target OU in which the test client is in






 
