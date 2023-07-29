## Using NMap
# Service Enumeration
nmap -Pn -p 1-10000 -sV 10.10.10.10
<img width="1028" alt="image" src="https://github.com/kwafula/eJPTExamPrep/assets/95890992/41240871-a970-4147-b82b-0177f9ce0fac">

# SMB Dialects Enumeration
nmap -p 445 --script smb-protocols 10.10.10.10
<img width="1028" alt="image" src="https://github.com/kwafula/eJPTExamPrep/assets/95890992/212b5dfa-f001-434e-b8f1-97cf5979e07c">

# SMB Security Mode Enumeration
nmap -p 445 -script smb-security-mode 10.10.10.10
<img width="1028" alt="image" src="https://github.com/kwafula/eJPTExamPrep/assets/95890992/9ab3383b-2b4a-48a2-99f6-b851fe63da49">

# SMB Sessions Enumeration Without Authentication & Default Configuration (Guest User Account Enabled)
nmap -p 445 -script smb-enum-sessons 10.10.10.10
<img width="1028" alt="image" src="https://github.com/kwafula/eJPTExamPrep/assets/95890992/19971b68-0084-4c28-99b6-3b71d578467d">

# SMB Sessions Enumeration With Authentication
nmap -p 445 -script smb-enum-sessons --script-args smbusername=<usernamehere>,smbpasword=<passwordhere> 10.10.10.10
<img width="1105" alt="image" src="https://github.com/kwafula/eJPTExamPrep/assets/95890992/8cca114a-6c92-4192-946a-dc7dd32a5838">

# SMB Shares Enumeration Without Authentication 
nmap -p 445 -script smb-enum-shares 10.10.10.10





