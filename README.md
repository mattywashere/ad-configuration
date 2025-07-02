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
<h3 align="center">Setup Resources in Azure</h3>
Create the Domain Controller VM (Windows Server 2022) named “RG-AD”
<p>
1.  <img src="https://i.imgur.com/gaAzjvb.png" height="75%" width="100%" alt="Resource Group"/>
</p>

Create a Virtual Machine named "DC-1"
<p>
2.  <img src="https://imgur.com/hxGdX5m.png" height="75%" width="100%" alt="Virtual Machine Microsoft Server"/>
</p>

Now create the Client VM (Windows 10) named “Client-1”. Use the same Resource Group and Vnet that was created in previous step
<p>
3.  <img src="https://imgur.com/Qe7kTPg.png" height="75%" width="100%" alt="Client Virtual Machine Windows"/>
</p>

Set Domain Controller’s NIC Private IP address to be static
<p>
4.  <img src="https://imgur.com/fpjb7Mm.png" height="75%" width="100%" alt="Static IP"/>
</p>

Check that both Virtual Machines are in the same Vnet (You can check the topology with Network Watcher)
<p>
5.  <img src="https://imgur.com/afB5syr.png" height="75%" width="100%" alt="Topology"/>
</p>
<h3 align="center">Ensure Connectivity between the client and Domain Controller</h3>
Login to Client-1 with Remote Desktop and ping DC-1’s private IP address with ping -t <ip address> (perpetual ping):
<p>
  <img src="https://imgur.com/L2wHmKP.png" height="75%" width="100%" alt="perpetual ping"/>
</p>
