<h1>Oracle VM VirtualBox - Creating and Maintaining Windows Active Directory</h1>

 ### [YouTube Demonstration](https://youtu.be/IyVqMel7Tew)
 ### [Server 2019 Download](https://www.microsoft.com/en-us/evalcenter/download-windows-server-2019)
 ### [Windows 10 ISO Download](https://www.microsoft.com/en-us/software-download/windows10)

<h2>Description</h2>
This project uses Oracle VirtualBox to create two Virtual Machine instances that will serve as a Domain Controller and a Client. The DC has two adapters, NAT (DC to the Internet) and Internal Network (DC to Client). This way, the Client can access the Internet through the DC. Using Server Manager, I install and configure Active Directory Domain Services, DHCP Server, and Remote Access onto the DC. I also run a custom script in PowerShell that will generate 1000+ users into the User Organizational Unit using a file with first and last names. Next, I boot up the Client VM and connect it to the domain. The Client only has one adapter, Internal Network (Client to DC). Finally, I implemented a few generic groups and assigned users to them. Now any of the 1000+ users can log in to the machine and work. 



<h2>Languages and Utilities Used</h2>

- <b>PowerShell</b>
- <b>Server Manager</b>

<h2>Environments Used </h2>

- <b>Oracle VirtualBox</b> 
- <b>Windows Server 2019</b>
- <b>Windows 10</b>

<h2>Project walk-through:</h2>

<p align="center">
Project Diagram: <br/><br />
<img src="https://i.imgur.com/LrJG1qq.png" height="80%" width="80%" alt="AD Steps"/>
<br />
<br />
<br />
Create the Domain Controller VM: <br/><br />
<img src="https://i.imgur.com/f2k07RZ.png" height="80%" width="80%" alt="AD Steps"/>
<br />
<br />
<br />
Edit the DC VM by adding two adapters: <br/><br />
<img src="https://i.imgur.com/ZNGtU7X.png" height="80%" width="80%" alt="AD Steps"/>
<img src="https://i.imgur.com/ZqjHeSg.png" height="80%" width="80%" alt="AD Steps"/>
<br />
<br />
<br />
Install Server 2019 onto the DC VM: <br/><br />
<img src="https://i.imgur.com/uhAPFI1.png" height="80%" width="80%" alt="AD Steps"/>
<br />
<br />
<br />
Rename the two networks to make setup easier later: <br/><br />
<img src="https://i.imgur.com/Xd6Guia.png" height="80%" width="80%" alt="AD Steps"/>
<br />
<br />
<br />
Set up an IP Address within the Internal Network: <br/><br />
<img src="https://i.imgur.com/Rl5iMCh.png" height="80%" width="80%" alt="AD Steps"/>
<br />
<br />
<br />
Install Active Directory Domain Services, DHCP Server, and Remote Access: <br/><br />
<img src="https://i.imgur.com/q7EhAgo.png" height="80%" width="80%" alt="AD Steps"/>
<br />
<br />
<br />
Add Routing Services when installing Remote Access: <br/><br />
<img src="https://i.imgur.com/sXAKEyY.png" height="80%" width="80%" alt="AD Steps"/>
<br />
<br />
<br />
Configure AD DS: <br/><br />
<img src="https://i.imgur.com/SoSomvy.png" height="80%" width="80%" alt="AD Steps"/>
<img src="https://i.imgur.com/ON2RaL2.png" height="80%" width="80%" alt="AD Steps"/>
<br />
<br />
<br />
Add a personal admin account: <br/><br />
<img src="https://i.imgur.com/eQaHy6K.png" height="80%" width="80%" alt="AD Steps"/>
<img src="https://i.imgur.com/3YkwgoV.png" height="80%" width="80%" alt="AD Steps"/>
<br />
<br />
<br />
Configure Remote Access: <br/><br />
<img src="https://i.imgur.com/KuVHlGb.png" height="80%" width="80%" alt="AD Steps"/>
<img src="https://i.imgur.com/I5Y8HHE.png" height="80%" width="80%" alt="AD Steps"/>
<br />
<br />
<br />
Configure DHCP by creating a new scope: <br/><br />
<img src="https://i.imgur.com/fZAeEJv.png" height="80%" width="80%" alt="AD Steps"/>
<img src="https://i.imgur.com/eCIyvY5.png" height="80%" width="80%" alt="AD Steps"/>
<img src="https://i.imgur.com/xny1MNX.png" height="80%" width="80%" alt="AD Steps"/>
<br />
<br />
<br />
Create 1000+ users by using a custom PowerShell script: <br/><br />
<img src="https://i.imgur.com/lB7RmMz.png" height="80%" width="80%" alt="AD Steps"/>
<br />
<br />
<br />
Create the Client VM: <br/><br />
<img src="https://i.imgur.com/N8Ft7pn.png" height="80%" width="80%" alt="AD Steps"/>
<br />
<br />
<br />
Edit the Client VM by adding the Internal Network Adapter: <br/><br />
<img src="https://i.imgur.com/0YgMoyt.png" height="80%" width="80%" alt="AD Steps"/>
<br />
<br />
<br />
Install Windows 10 Pro onto the Client VM: <br/><br />
<img src="https://i.imgur.com/TBRKje2.png" height="80%" width="80%" alt="AD Steps"/>
<br />
<br />
<br />
Add the Client VM to our Domain: <br/><br />
<img src="https://i.imgur.com/BMDoqBL.png" height="80%" width="80%" alt="AD Steps"/>
<br />
<br />
<br />
Observe that the Client is now listed with our computers: <br/><br />
<img src="https://i.imgur.com/Xdy5hUC.png" height="80%" width="80%" alt="AD Steps"/>
<br />
<br />
<br />
Create a few generic groups: <br/><br />
<img src="https://i.imgur.com/ThIyIc0.png" height="80%" width="80%" alt="AD Steps"/>
<img src="https://i.imgur.com/3nEGvpm.png" height="80%" width="80%" alt="AD Steps"/>
<br />
<br />
<br />
Add a few users to our new groups: <br/><br />
<img src="https://i.imgur.com/IoO3RmE.png" height="80%" width="80%" alt="AD Steps"/>
<img src="https://i.imgur.com/OFvXdLW.png" height="80%" width="80%" alt="AD Steps"/>
<br />
<br />
<br />
And we're done <br/><br />
