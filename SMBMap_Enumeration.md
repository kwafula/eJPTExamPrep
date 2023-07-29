### SMB Enumeration Using SMBMap
# Service Enumaration
nmap 10.10.10.10
nmap -Pn 10.10.10
nmap -Pn -sV 10.10.10.10
<img width="720" alt="image" src="https://github.com/kwafula/eJPTExamPrep/assets/95890992/12c52d47-81e1-4a80-9a68-10b362f3470e">


# Enumerate SMB Dialects
nmap --script smb-protocols 10.10.10.10 -p 445
<img width="720" alt="image" src="https://github.com/kwafula/eJPTExamPrep/assets/95890992/30c50f31-f4e2-4fc6-976e-316c15ff4c34">

# Enumerate Shares Folder Using Guest Account
smbmap -u guest -p "" -d . -H 10.10.10.10 -p 445
<img width="983" alt="image" src="https://github.com/kwafula/eJPTExamPrep/assets/95890992/eed41952-e433-43c7-be6d-942996f72eb7">

# Enumerate Shares Using Standard User
smbmap -u <standardusernamehere> -p <userpasswordhere> -d . -H 10.10.10.10
<img width="983" alt="image" src="https://github.com/kwafula/eJPTExamPrep/assets/95890992/e376b228-857d-43ca-b963-4291ed8be14c">
 
# Command Output Using Standard User 
smbmap -u <standardusernamehere> -p <userpasswordhere> -d . -H 10.10.10.10 -x 'ipconfig'

# List Drives Using Standard User 
smbmap -u <standardusernamehere> -p <userpasswordhere> -d . -H 10.10.10.10 -L

# List Contents of C:\ Using Standard User 
smbmap -u <standardusernamehere> -p <userpasswordhere> -d . -H 10.10.10.10 -r 'C$'

# Upload To C:\ Using Standard User 
smbmap -u <standardusernamehere> -p <userpasswordhere> -d . -H 10.10.10.10 --upload '/home/bob/test.txt' 'C$\text.txt'

# Download To C:\ Using Standard User 
smbmap -u <standardusernamehere> -p <userpasswordhere> -d . -H 10.10.10.10 --download 'C$\text.txt'


