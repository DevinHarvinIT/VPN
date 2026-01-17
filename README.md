# Virtual Private Network Lab

![image alt](PLACEHOLDER_HEADER_IMAGE)

## Overview

This lab demonstrates how a Virtual Private Network (VPN) functions as a secure tunnel by masking a device’s public IP address and changing its apparent geographic location. The workflow compares a local host IP address, a cloud virtual machine IP address in a different region, and a VPN-assigned IP address. The lab concludes by validating the location change through region-based content access.

## Environment and Tools Used

- Microsoft Azure Virtual Machine  
- Windows 10 Pro  
- Windows Remote Desktop (Windows App on macOS)  
- Proton VPN  
- WhatIsMyIPAddress.com  
- Netflix  

## Skills Demonstrated

- Public IP identification and geolocation verification  
- Cloud virtual machine deployment in a selected region  
- Remote desktop connectivity to a cloud VM  
- VPN client installation and authentication  
- VPN traffic routing and IP masking  
- Geolocation validation using real-world services  

---

## Step 1
<div align="center"><b>Verify Baseline IPv4 Address and Location</b></div>

<div align="center">
  
![image alt](PLACEHOLDER_SH1)

</div>

The baseline public IPv4 address and geographic location are verified from the host machine using an IP lookup service. This establishes the original location before introducing any cloud or VPN-based changes.

---

## Step 2
<div align="center"><b>Create Virtual Machine in a Different Geographic Region</b></div>

<div align="center">
  
![image alt](PLACEHOLDER_SH2)  
![image alt](PLACEHOLDER_SH4)

</div>

A new Azure virtual machine is deployed in a different geographic region. For this lab, the region is set to East Asia to intentionally assign a public IP address outside of the host machine’s original location.

---

## Step 3
<div align="center"><b>Connect to the Virtual Machine Using Remote Desktop</b></div>

<div align="center">
  
![image alt](PLACEHOLDER_SH5)  
![image alt](PLACEHOLDER_SH6)

</div>

The virtual machine is accessed using Windows Remote Desktop with the VM’s public IP address. This confirms successful deployment and establishes the VM as the testing environment.

---

## Step 4
<div align="center"><b>Verify Virtual Machine Public IP and Location</b></div>

<div align="center">
  
![image alt](PLACEHOLDER_SH7)

</div>

From within the virtual machine, the public IPv4 address and location are checked again. Because the VM was deployed in East Asia, the IP geolocation reflects Hong Kong, confirming correct regional placement.

---

## Step 5
<div align="center"><b>Download and Sign In to VPN Client</b></div>

<div align="center">
  
![image alt](PLACEHOLDER_SH10)  
![image alt](PLACEHOLDER_SH11)

</div>

The Proton VPN client is downloaded and installed on the virtual machine. After installation, the client is launched and authenticated in preparation for establishing a VPN connection.

---

## Step 6
<div align="center"><b>Connect to VPN and Confirm Updated IP Address</b></div>

<div align="center">
  
![image alt](PLACEHOLDER_SH12)

</div>

Once connected to Proton VPN, the public IP address and geolocation are checked again. The VPN assigns a new public-facing IP address, shifting the apparent location to the Netherlands.

---

## Step 7
<div align="center"><b>Validate Geolocation Change Using Netflix</b></div>

<div align="center">
  
![image alt](PLACEHOLDER_SH13)

</div>

Netflix is accessed to validate the geolocation change. The site loads with Netherlands regional indicators, confirming that location-based content reflects the VPN-assigned IP address.

---

## Results Summary

<div align="center">
  
![image alt](PLACEHOLDER_SH14)

</div>

The final comparison highlights three distinct IP addresses and locations:

- Host machine public IP and local geolocation  
- Azure virtual machine public IP and East Asia geolocation  
- VPN-assigned public IP and Netherlands geolocation  

This confirms how VPNs function as secure tunnels by masking original IP addresses and routing traffic through alternate geographic locations.


This confirms how VPNs function as secure tunnels by masking original IP addresses and routing traffic through alternate geographic locations.
