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
