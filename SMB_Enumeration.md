## Using NMap
# Service Enumeration
nmap -Pn -p 1-10000 -sV 10.10.10.10
<img width="1001" alt="image" src="https://github.com/kwafula/eJPTExamPrep/assets/95890992/b9ebd1cf-6cc3-419c-a5a7-9f03575d9067">

# SMB Dialects Enumeration
nmap -p 445 --script smb-protocols 10.10.10.10
<img width="1028" alt="image" src="https://github.com/kwafula/eJPTExamPrep/assets/95890992/500cdc41-728b-4d80-9caf-273ec412c964">

# SMB Security Mode Enumeration
nmap -p 445 -script smb-security-mode 10.10.10.10
<img width="1028" alt="image" src="https://github.com/kwafula/eJPTExamPrep/assets/95890992/afadeaa8-c4b8-4739-ad44-dafe33cc27e9">

# SMB Sessions Enumeration
nmap -p 445 -script smb-enum-sessons 10.10.10.10
<img width="1028" alt="image" src="https://github.com/kwafula/eJPTExamPrep/assets/95890992/8a569e75-47ab-45ca-97ed-49a6b651b82d">

# SMB Sessions Enumeration With Default Configuration (Guest User Account Enabled)
nmap -p 445 -script smb-enum-sessons 10.10.10.10
<img width="1028" alt="image" src="https://github.com/kwafula/eJPTExamPrep/assets/95890992/19971b68-0084-4c28-99b6-3b71d578467d">


