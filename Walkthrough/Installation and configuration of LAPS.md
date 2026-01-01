# Installation of LAPS 
- Installed LAPS from Micrsofts page with my host OS
- Placed the installation into a shared folder that is shared between the host OS and virtual machine
<img width="700" height="163" alt="image" src="https://github.com/user-attachments/assets/a82454c3-4b85-4f0b-9da7-d54c65c9ddce" />

- Installed entire features under 'Management Tools' during the wizard
<img width="370" height="205" alt="image" src="https://github.com/user-attachments/assets/4fe57249-f5f0-4613-a447-85c28b7c5194" />

- Restarted the DC after installtion to ensure services load cleanly such as Group Policy extensions and PowerShell modules

## PowerShell Commands 
Importing the module, this makes the module's commands available in the current PowerShell session 

<img width="470" height="56" alt="image" src="https://github.com/user-attachments/assets/083de10c-51e2-4fe7-8fe3-1aea7d64bb5f" />

---
Updating the schema

<img width="750" height="184" alt="image" src="https://github.com/user-attachments/assets/44b61efb-da0a-4dc9-8d2f-cbebe8962d63" />

---
Setting permissions that allow the computer using LAPS to update its own attributes
- The Orgainisational Unit 'Workstations' is the target in which the test client is in
  

<img width="750" height="138" alt="image" src="https://github.com/user-attachments/assets/0bc9c2fa-0c58-4724-8d6b-d92e467ebeb6" />

---
For the next command, a security group called 'LAPSAdmins' was created with Domain Admins added to it 
- This command sets the permissions to view the updated Administrator passwords


<img width="750" height="135" alt="image" src="https://github.com/user-attachments/assets/abd52d15-f985-472b-89d0-08e624d3caa7" />

## Creating a Group Policy to install the LAPS installer on the target machoine 
- A GPO was created and configured by navigating Computer Configuration > Software Settings > Software installation
<img width="800" height="148" alt="image" src="https://github.com/user-attachments/assets/a125b2d1-9401-4a35-a2c2-41dad91a102d" />

- LAPS installation file was added

## Configuring LAPS Policies 
- Navigated to LAPS through Computer Configuation > Policies > Administrative Templates > LAPS
- Enabled 'Enable local admin password management'
- Enabled 'Password Settings'
- Enabled 'Do not allow password expiration time longer than required'
<img width="750" height="148" alt="image" src="https://github.com/user-attachments/assets/390e3579-e5aa-4312-9971-a52888f696d3" />

- GPO was linked to the OU the target machine is in










