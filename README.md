<h1>Oracle VM Virtual Box - Creating and Maintaining Windows Active Directory</h1>

 ### [YouTube Demonstration]()

<h2>Description</h2>
This project uses Oracle Virtual Box to create two Virtual Machine instances that will serve as a Domain Controller and a Client. The DC has two adapters, NAT (DC to the Internet) and Internal Network (DC to Client). This way the Client can access the internet through the DC. Using Server Manager I install and configure Active Directory Domain Services, DHCP Server, and Remote Access onto the DC. I also run a custom script in Powershell that will generate 1000+ users into the User Organizational Unit using a file with first and last names. Finally I boot up the Client VM and connect it to the domain. The Client only has one adapter, Internal Network (Client to DC). Now any of the 1000+ users can login to the machine and work. 



<h2>Languages and Utilities Used</h2>

- <b>PowerShell</b>
- <b>Server Manager</b>

<h2>Environments Used </h2>

- <b>Oracle Virtual Box</b> 
- <b>Windows Server 2019</b>
- <b>Windows 10</b>

<h2>Program walk-through:</h2>

<p align="center">
Create the Domain Controller VM: <br/><br />
<img src="https://i.imgur.com/f2k07RZ.png" height="80%" width="80%" alt="SIEM Steps"/>
<br />
<br />
<br />
Edit the DC VM by adding two adapters: <br/><br />
<img src="https://i.imgur.com/ZNGtU7X.png" height="80%" width="80%" alt="SIEM Steps"/>
<img src="https://i.imgur.com/ZqjHeSg.png" height="80%" width="80%" alt="SIEM Steps"/>
<br />
<br />
<br />
Install Server 2019 onto the DC VM: <br/><br />
<img src="https://i.imgur.com/uhAPFI1.png" height="80%" width="80%" alt="SIEM Steps"/>
<br />
<br />
<br />
Rename our networks to make setup easier later: <br/><br />
<img src="https://i.imgur.com/Xd6Guia.png" height="80%" width="80%" alt="SIEM Steps"/>
<br />
<br />
<br />
Setup a IP Address within the Internal Network: <br/><br />
<img src="https://i.imgur.com/Rl5iMCh.png" height="80%" width="80%" alt="SIEM Steps"/>
<br />
<br />
<br />
Install Active Directory Domain Services, DHCP Server, and Remote Access: <br/><br />
<img src="https://i.imgur.com/q7EhAgo.png" height="80%" width="80%" alt="SIEM Steps"/>
<br />
<br />
<br />
Add Routing Services when installing Remote Accesss: <br/><br />
<img src="https://i.imgur.com/sXAKEyY.png" height="80%" width="80%" alt="SIEM Steps"/>
<br />
<br />
<br />
Configure AD DS: <br/><br />
<img src="https://i.imgur.com/SoSomvy.png" height="80%" width="80%" alt="SIEM Steps"/>
<img src="https://i.imgur.com/ON2RaL2.png" height="80%" width="80%" alt="SIEM Steps"/>
<br />
<br />
<br />
Add a personal admin account: <br/><br />
<img src="https://i.imgur.com/eQaHy6K.png" height="80%" width="80%" alt="SIEM Steps"/>
<img src="https://i.imgur.com/3YkwgoV.png" height="80%" width="80%" alt="SIEM Steps"/>
<br />
<br />
<br />
Configure Remote Access: <br/><br />
<img src="https://i.imgur.com/KuVHlGb.png" height="80%" width="80%" alt="SIEM Steps"/>
<img src="https://i.imgur.com/I5Y8HHE.png" height="80%" width="80%" alt="SIEM Steps"/>
<br />
<br />
<br />
Configure DHCP by creating a new scope: <br/><br />
<img src="https://i.imgur.com/fZAeEJv.png" height="80%" width="80%" alt="SIEM Steps"/>
<img src="https://i.imgur.com/eCIyvY5.png" height="80%" width="80%" alt="SIEM Steps"/>
<img src="https://i.imgur.com/xny1MNX.png" height="80%" width="80%" alt="SIEM Steps"/>
<br />
<br />
<br />
Create 1000+ users using a custom PowerShell script: <br/><br />
<img src="https://i.imgur.com/lB7RmMz.png" height="80%" width="80%" alt="SIEM Steps"/>
<br />
<br />
<br />
Create the Client VM: <br/><br />
<img src="https://i.imgur.com/N8Ft7pn.png" height="80%" width="80%" alt="SIEM Steps"/>
<br />
<br />
<br />
Edit the Client VM by adding the Internal Network Adapter: <br/><br />
<img src="https://i.imgur.com/0YgMoyt.png" height="80%" width="80%" alt="SIEM Steps"/>
<br />
<br />
<br />
