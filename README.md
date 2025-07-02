<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" height="40%" width="40%"alt="Microsoft Active Directory"/>
</p>

# Configuring Active Directory Within Azure
This tutorial teaches the implementation of Active Directory within Azure Virtual Machines

# Environments & Technologies Used

- Microsoft Azure (Virtual Machines | Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

# Operating Systems Used 

- Windows Server 2022
- Windows 10

# High-Level Deployment and Configuration Steps #

- Create Resources
- Ensure Connectivity between the client and Domain Controller
- Install Active Directory
- Create an Admin and Normal User Account in AD
- Join Client-1 to your domain (myadproject.com)
- Setup Remote Desktop for non-administrative users on Client-1
- Create additional users and attempt to log into client-1 with one of the users

# Deployment and Configuration Steps

Create the Domain Controller VM (Windows Server 2022) named “RG-AD”:
<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" height="40%" width="40%"alt="Resource Group"/>
</p>
