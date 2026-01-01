# LAPS Confirmation 
- As LAPS has been configured and set up, the client machine was logged in to, to initiate the Local Administrator password to be enforced
-  gpupdate /force was ran on the client to pull in the LAPS GPO
-  After client restart, the LAPS password can be viewed in the DC via the LAPS UI
<img width="400" height="293" alt="image" src="https://github.com/user-attachments/assets/8770e466-818e-4558-b3f7-ccce30af8fe6" />

- The password can also be viewed through Active Directory > the target OU > go into attribute editor on the machine object. Scroll down till you see the attribute shown in the screenshot
<img width="400" height="379" alt="image" src="https://github.com/user-attachments/assets/2f2b4d2e-bff5-45b8-87a7-a4227e72f72b" />

## Verifying login using the LAPS password

