# Virtual Private Network Lab

<div align="center">
  <img src="PLACEHOLDER_HEADER_IMAGE" alt="VPN Lab Header">
</div>

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

<div style="display: flex; align-items: center;">
  <div style="font-weight: bold;">Step 1</div>
  <div style="flex: 1; text-align: center; font-weight: bold;">
    Verify Baseline IPv4 Address and Location
  </div>
</div>

![image alt](PLACEHOLDER_SH1)

The baseline public IPv4 address and geographic location are verified from the host machine using an IP lookup service. This establishes the original location before introducing any cloud or VPN-based changes.

---

<div style="display: flex; align-items: center;">
  <div style="font-weight: bold;">Step 2</div>
  <div style="flex: 1; text-align: center; font-weight: bold;">
    Create Virtual Machine in a Different Geographic Region
  </div>
</div>

![image alt](PLACEHOLDER_SH2)
![image alt](PLACEHOLDER_SH4)

A new Azure virtual machine is deployed in a different geographic region. For this lab, the region is set to East Asia to intentionally assign a public IP address outside of the host machine’s original location.

---

<div style="display: flex; align-items: center;">
  <div style="font-weight: bold;">Step 3</div>
  <div style="flex: 1; text-align: center; font-weight: bold;">
    Connect to the Virtual Machine Using Remote Desktop
  </div>
</div>

![image alt](PLACEHOLDER_SH5)
![image alt](PLACEHOLDER_SH6)

The virtual machine is accessed using Windows Remote Desktop with the VM’s public IP address. This confirms successful deployment and establishes the VM as the testing environment.

---

<div style="display: flex; align-items: center;">
  <div style="font-weight: bold;">Step 4</div>
  <div style="flex: 1; text-align: center; font-weight: bold;">
    Verify Virtual Machine Public IP and Location
  </div>
</div>

![image alt](PLACEHOLDER_SH7)

From within the virtual machine, the public IPv4 address and location are checked again. Because the VM was deployed in East Asia, the IP geolocation reflects Hong Kong, confirming correct regional placement.

---

<div style="display: flex; align-items: center;">
  <div style="font-weight: bold;">Step 5</div>
  <div style="flex: 1; text-align: center; font-weight: bold;">
    Download and Sign In to VPN Client
  </div>
</div>

![image alt](PLACEHOLDER_SH10)
![image alt](PLACEHOLDER_SH11)

The Proton VPN client is downloaded and installed on the virtual machine. After installation, the client is launched and authenticated in preparation for establishing a VPN connection.

---

<div style="display: flex; align-items: center;">
  <div style="font-weight: bold;">Step 6</div>
  <div style="flex: 1; text-align: center; font-weight: bold;">
    Connect to VPN and Confirm Updated IP Address
  </div>
</div>

![image alt](PLACEHOLDER_SH12)

Once connected to Proton VPN, the public IP address and geolocation are checked again. The VPN assigns a new public-facing IP address, shifting the apparent location to the Netherlands.

---

<div style="display: flex; align-items: center;">
  <div style="font-weight: bold;">Step 7</div>
  <div style="flex: 1; text-align: center; font-weight: bold;">
    Validate Geolocation Change Using Netflix
  </div>
</div>

![image alt](PLACEHOLDER_SH13)

Netflix is accessed to validate the geolocation change. The site loads with Netherlands regional indicators, confirming that location-based content reflects the VPN-assigned IP address.

---

## Results Summary

![image alt](PLACEHOLDER_SH14)

The final comparison highlights three distinct IP addresses and locations:

- Host machine public IP and local geolocation
- Azure virtual machine public IP and East Asia geolocation
- VPN-assigned public IP and Netherlands geolocation

This confirms how VPNs mask an original public IP and route traffic through a different geographic exit point.


This confirms how VPNs function as secure tunnels by masking original IP addresses and routing traffic through alternate geographic locations.


This confirms how VPNs function as secure tunnels by masking original IP addresses and routing traffic through alternate geographic locations.
