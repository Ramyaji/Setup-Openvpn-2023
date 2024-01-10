[openvpn-setup.txt](https://github.com/Ramyaji/Setup-Openvpn-2023/files/13890976/openvpn-setup.txt)
# Setup-Openvpn-2023
Setup-Openvpn-2023

**Create Security Group  openvpn**
Edit Inbound Rules
HTTPS 443
ALL ICMP-IPv4
SSH  22
ALL UDP 1194
ALL TCP 943

**Create EC2 Instance**
*Application and OS Images (Amazon Machine Image)
Choose AMI 
Click on Browse more AMIs
Search openvpn

{{OpenVPN Access Server (5 Connected Devices)
OpenVPN Inc. 

 2 AWS reviews  | 31 external reviews 
Free Tier|Free Trial}}

*Key pair (login)

*Network settings

Select SG openvpn

Auto-assign public IP
Disable 

Launch Instance

**Stop the Open vpn Instance**

**Create Elastic IP**
Associate to Openvpn Instance

**Start the instance**

**Open Linux terminal in .Pem directory**
chmod 777 PK.pem
ping Public IP (EIP)
ssh -i PK.pem openvpnas@EIP

**yes yes next all the way to create admin credentials**

8.sudo -i
passwd admin
save passwd 

9.https://EIP/
https://43.204.208.123:943/admin

Go to usermanagement
create users

provide url to access public IP:943


https://www.youtube.com/watch?v=XO4WQ3VdYDE  (video for set up this)
