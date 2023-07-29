## SMB Using NMap
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
<img width="463" alt="image" src="https://github.com/kwafula/eJPTExamPrep/assets/95890992/327f72a5-3417-4d87-918e-002f3a581ccf">

# SMB Shares Enumeration Without Authentication 
nmap -p 445 -script smb-enum-shares 10.10.10.10

# SMB Shares Enumeration With Authentication 
nmap -p 445 -script smb-enum-shares --script-args smbusername=<usernamehere>,smbpasword=<passwordhere> 10.10.10.10

# SMB Shares Enumeration With Authentication & List Directories
nmap -p 445 -script smb-enum-shares,smb-ls --script-args smbusername=<usernamehere>,smbpasword=<passwordhere> 10.10.10.10

# SMB Users Enumeration Without Authentication 
nmap -p 445 -script smb-enum-users 10.10.10.10

# SMB Users Enumeration With Authentication
nmap -p 445 -script smb-enum-users --script-args smbusername=<usernamehere>,smbpasword=<passwordhere> 10.10.10.10
<img width="891" alt="image" src="https://github.com/kwafula/eJPTExamPrep/assets/95890992/2b79a8c8-f9c0-428c-b622-87ef165f9c68">

# SMB Statistics Enumeration With Authentication
nmap -p 445 -script smb-server-stats --script-args smbusername=<usernamehere>,smbpasword=<passwordhere> 10.10.10.10
<img width="917" alt="image" src="https://github.com/kwafula/eJPTExamPrep/assets/95890992/d58e1a50-5b84-4e26-b71d-54a0ca4d560f">

# SMB Domains Enumeration With Authentication
nmap -p 445 -script smb-enum-domains --script-args smbusername=<usernamehere>,smbpasword=<passwordhere> 10.10.10.10
<img width="1634" alt="image" src="https://github.com/kwafula/eJPTExamPrep/assets/95890992/4dd804b1-19c9-486a-a3b6-c9bd31af9294">

# SMB Groups Enumeration With Authentication
nmap -p 445 -script smb-enum-groups --script-args smbusername=<usernamehere>,smbpasword=<passwordhere> 10.10.10.10
<img width="720" alt="image" src="https://github.com/kwafula/eJPTExamPrep/assets/95890992/e2bda7e3-8149-4194-9a5a-e811d755a223">

# SMB Services Enumeration With Authentication
nmap -p 445 -script smb-enum-services --script-args smbusername=<usernamehere>,smbpasword=<passwordhere> 10.10.10.10
<img width="720" alt="image" src="https://github.com/kwafula/eJPTExamPrep/assets/95890992/fa60d371-cadf-43ed-949c-05bd91a685e0">

