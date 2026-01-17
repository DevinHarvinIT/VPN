# Virtual Private Network Lab

![image alt](PLACEHOLDER_HEADER_IMAGE)

## Overview

This lab demonstrates how a Virtual Private Network (VPN) functions as a secure tunnel by masking a device’s public IP address and changing its apparent geographic location. The workflow compares a local host IP address, a cloud virtual machine IP address in a different region, and a VPN assigned IP address. The lab concludes by validating the location change through region based content access.

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
- Geolocation validation using real world services

---

## Step 1: Verify Baseline IPv4 Address and Location

![image alt](PLACEHOLDER_SH1)

The baseline public IPv4 address and geographic location are verified from the host machine using an IP lookup service. This establishes the original location before introducing any cloud or VPN based changes.

---

## Step 2: Create Virtual Machine in a Different Geographic Region

![image alt](PLACEHOLDER_SH2)

![image alt](PLACEHOLDER_SH4)

A new Azure virtual machine is deployed in a different geographic region. For this lab, the region is set to East Asia to intentionally assign a public IP address outside of the host machine’s original location.

---

## Step 3: Connect to the Virtual Machine Using Remote Desktop

![image alt](PLACEHOLDER_SH5)

![image alt](PLACEHOLDER_SH6)

The virtual machine is accessed using Windows Remote Desktop using the VM’s public IP address. This confirms successful deployment and establishes the VM as the environment for further testing.

---

## Step 4: Verify Virtual Machine Public IP and Location

![image alt](PLACEHOLDER_SH7)

From within the virtual machine, the public IPv4 address and location are checked again. Because the VM was deployed in East Asia, the IP geolocation reflects Hong Kong, confirming the regional placement of the VM.

---

## Step 5: Download and Sign In to VPN Client

![image alt](PLACEHOLDER_SH10)

![image alt](PLACEHOLDER_SH11)

The Proton VPN client is downloaded and installed on the virtual machine. After installation, the client is launched and authenticated in preparation for establishing a VPN connection.

---

## Step 6: Connect to VPN and Confirm Updated IP Address

![image alt](PLACEHOLDER_SH12)

Once connected to Proton VPN, the public IP address and geolocation are checked again. The VPN assigns a new public facing IP address, shifting the apparent location to the Netherlands.

---

## Step 7: Validate Geolocation Change Using Netflix

![image alt](PLACEHOLDER_SH13)

Netflix is accessed to validate the geolocation change. The site loads with Netherlands regional indicators, confirming that location based content reflects the VPN assigned IP address.

---

## Results Summary

![image alt](PLACEHOLDER_SH14)

The final comparison highlights three distinct IP addresses and locations:

- Host machine public IP and local geolocation
- Azure virtual machine public IP and East Asia geolocation
- VPN assigned public IP and Netherlands geolocation

This confirms how VPNs function as secure tunnels by masking original IP addresses and routing traffic through alternate geographic locations.
