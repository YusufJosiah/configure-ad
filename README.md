<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>Active Directory Deployed in the Cloud (Azure)</h1>
This tutorial outlines the implementation of on-premises Active Directory within Azure Virtual Machines.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (22H2)

<h2>High-Level Deployment and Configuration Steps</h2>
Organizations utilize Microsoft Active Directory (AD) to manage computers, users, and applications on their network. AD enables efficient administration through features like single sign-on, group policy management, and facilitates secure access control to resources within the network environment. AD is deployed and configured in Azure following the steps:

1. Create a Domain Controller (DC) Windows Server and configure a static NIC Private IP a.ddress. Create a client virtual machine (VM) (Windows 10) set it on the same virtual network (VNET) as the DC.
2. Verify Connectivity between the DC and the client VM within the VNET using the ping protocol.
3. Install and configure Active Directory Domain Serivices (AD DS) on the DC to create a domain. Then create and provision administrative users.
3. Join the client VM to the domain; create and configure non-administrative users


<h2>Deployment and Configuration Steps</h2>

<p>
<img src="https://i.imgur.com/932xy1H.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
To set the Domain Controller's NIC’s private IP address to be static, Navigate to the Domain Controller's network settings, access the IP configuration, and change the IP configuration from dynamic (DHCP) to static. Save the change.
</p>
<br />

<p>
<img src="https://i.imgur.com/CGLg2M2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Long into (DC-1) using the RDP. Access the server manager and install Active Directory Services. The click on promote to domain controller to finish installing the active directory. Then log back in using domain-name\user and the password.
</p>
<br />

<p>
<img src="https://i.imgur.com/4H9d8wC.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
As can be seen in the picture above, using AD, administrators can create, manage, and organize users, groups, and computers, simplifying the process of assigning permissions and access rights. AD provides a centralized database to authenticate and authorize users and computers in a Windows domain network. AD allows administrators to enforce security settings and policies across the network using Group Policy Objects (GPOs). These policies can define access controls, password policies, software installation rules, and more.
</p>
<br />
