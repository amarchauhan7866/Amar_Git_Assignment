# 	Q.1   In this section we will try to understand why we need a VCS and what would be our life without that  

   ### Benefits of version control systems. Developing software without using version control is risky, like not having backups. Version       control can also enable developers to move faster and it allows software teams to preserve efficiency and agility as the team scales to     include more developers and below are the keys.
### A.	Collaboration
### B.	Storing Versions
### C.	Restoring Previous Versions
### D.	Understanding What Happened
### E.	Backup  


# Create a shell script to install vsftpd

```
#/bin/bash

yum install vsftpd

#Start the vsftpd servic

systemctl start vsftpd
systemctl enable vsftpd

# allow port in firewall

firewall-cmd --zone=public --permanent --add-port=21/tcp
firewall-cmd --zone=public --permanent --add-service=ftp
firewall-cmd --reload

```

![vsftp](https://github.com/amarchauhan7866/Amar_Git_Assignment/blob/Amar/Git_Media_Day1/vsftpd.jpg)

## Setup a FTP server and use that FTP server to share the code among yourself

![vsftclint](https://github.com/amarchauhan7866/Amar_Git_Assignment/blob/Amar/Git_Media_Day1/vsftpdclint.jpg)

![filecreateion](https://github.com/amarchauhan7866/Amar_Git_Assignment/blob/Amar/Git_Media_Day1/createfile.jpg.png)

![crosscheckUI](https://github.com/amarchauhan7866/Amar_Git_Assignment/blob/Amar/Git_Media_Day1/CrosscheckfromUI.jpg)


![crosscheckUI](https://github.com/amarchauhan7866/Amar_Git_Assignment/blob/Amar/Git_Media_Day1/Access%20ftp%20from%20fileZilla.png)



