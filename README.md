# Virtual Private Network (VPN) Lab

<div align="center">
  <img src[>![image alt](https://github.com/DevinHarvinIT/VPN/blob/89e3a2348f796ba634caca7abce2945f37515510/Images/VPN%20Header.webp)
</div>

## Overview
This lab demonstrates the use of a Virtual Private Network to mask geographic location and alter IP-based access by routing traffic through encrypted tunnels. The lab validates VPN behavior by comparing IP addresses and geolocation data before VM creation, after VM deployment, and after VPN activation.

## Environment and Tools Used
- Azure Cloud Virtual Machine  
- Proton VPN  
- Windows 10  
- Microsoft Remote Desktop  
- WhatIsMyIPAddress.com  

## Skills Demonstrated
- VPN configuration and validation  
- IP address and geolocation analysis  
- Virtual machine deployment and access  
- Secure remote connectivity concepts  
- Network privacy awareness  

<br>

## **Step 1** <div align="center"><b>Baseline IP Address and Geolocation Check</b></div>

![image alt](images/SH1.png)

The public IPv4 address and geographic location of the local machine are identified using an IP lookup service. This establishes a baseline before any virtual infrastructure or VPN usage.

<br>

## **Step 2** <div align="center"><b>Create Virtual Machine in Alternate Geographic Region</b></div>

![image alt](images/SH2.png)
![image alt](images/SH4.png)

A virtual machine is deployed in the East Asia region using Azure. This selection determines the initial geolocation associated with the VM’s public IP address.

<br>

## **Step 3** <div align="center"><b>Access Virtual Machine via Remote Desktop</b></div>

![image alt](images/SH5.png)
![image alt](images/SH6.png)

The virtual machine is accessed using Microsoft Remote Desktop by connecting to the VM’s public IP address with administrator credentials.

<br>

## **Step 4** <div align="center"><b>Verify VM IP Address and Location</b></div>

![image alt](images/SH7.png)

The VM’s public IP address is checked using an IP lookup service, confirming the geolocation corresponds to Hong Kong based on the selected Azure region.

<br>

## **Step 5** <div align="center"><b>Install and Connect to VPN Client</b></div>

![image alt](images/SH10.png)
![image alt](images/SH11.png)

Proton VPN is downloaded and installed on the virtual machine. A VPN server located in a different country is selected and the VPN tunnel is established.

<br>

## **Step 6** <div align="center"><b>Validate VPN IP Address and Geolocation Change</b></div>

![image alt](images/SH12.png)

After VPN activation, the public IP address is checked again. The geolocation now reflects the VPN server location in the Netherlands, confirming successful traffic tunneling.

<br>

## **Step 7** <div align="center"><b>Validate Geolocation Impact Using Streaming Services</b></div>

![image alt](images/SH13.png)

Netflix is accessed to demonstrate how content availability and regional access are influenced by IP-based geolocation changes introduced by the VPN.

<br>

## **Step 8** <div align="center"><b>Summary of IP Address and Geolocation Transitions</b></div>

![image alt](images/SH14.png)

**A summary comparison documents the three observed states:**
- Local machine IP and location  
- Azure VM IP and location  
- VPN-protected IP and location  

This confirms how VPNs abstract physical location and enhance privacy by routing traffic through alternate geographic endpoints.


This confirms how VPNs function as secure tunnels by masking original IP addresses and routing traffic through alternate geographic locations.


This confirms how VPNs function as secure tunnels by masking original IP addresses and routing traffic through alternate geographic locations.
