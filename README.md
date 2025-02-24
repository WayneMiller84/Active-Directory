<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in the Cloud (Azure)</h1>
This tutorial outlines the implementation of on-premises Active Directory within Azure Virtual Machines.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How to Deploy on-premises Active Directory within Azure Compute](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Setup Domain Controller VM (dc-1) & Disable Firewall
- Setup Client-1 & Change Settings to dc-1's Private IP Adrress
- Attempt to Ping DC-1 Private IP address using PowerShell
- Run ipconfig /all for DNS setting 10.0.0.4
- Create a Domain Admin User
- Setup Remote Desktop for Non-admin users on Client-1

<h2>Deployment and Configuration Steps</h2>

![DC-1](https://github.com/user-attachments/assets/9aa66cf3-85d2-44eb-a302-6f5f040fdf2b)
![image](https://github.com/user-attachments/assets/ab85786e-ba2e-4412-9d1f-af8078a89635)

</p>
<p>
Create a Resource Group, Create a Virtual Network and Subnet, Create the Domain Controller VM (dc-1), once VM is created set dc-1 NIC Private IP address (10.0.0.4) to static. Log into the VM and disable the Windows Firewall (for testing connectivity)

</p>
<br />

![Clent-1](https://github.com/user-attachments/assets/d3167533-28db-4dde-ab2f-fd81e9338400)
![image](https://github.com/user-attachments/assets/f7ba1fad-5a59-41d9-94dd-57c47848e790)
  
</p>
<p>
Create Client VM (Client-1) in Azure, Change Inherit from Virtual Network to Custom then set DNS settings to DC-1's private IP address (10.0.0.4) 
</p>
<br />

![image](https://github.com/user-attachments/assets/ddfe17b4-929a-464b-9770-c7587c26b3a2)

</p>
<p>
On Client-1 VM click on Start button the type Powershell, type ping and dc-1 private IP address 10.0.0.4 and enter 
</p>
<br />

![image](https://github.com/user-attachments/assets/899ca796-020d-4324-8c46-f269339f02d0)

</p>
<p>
From Client-1 VM open PowerShell and run ipconfig /all, the DNS settings should show dc-1 private IP address (10.0.0.4)
</p>
<br />

![image]

</p>
<p>
TYPE HERE
</p>
<br />

![image]

</p>
<p>
TYPE HERE
</p>
<br />
