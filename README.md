<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in the Cloud (Azure)</h1>
This tutorial outlines the implementation of on-premises Active Directory within Azure Virtual Machines.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Various Command-Line Tools
- Various Network Protocols (SSH, RDH, DNS, HTTP/S, ICMP)
- Wireshark (Protocol Analyzer)

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>Deployment and Configuration Steps</h2>

Start by setting up two Virtual Machines (VMs) in Microsoft Azure. Configure the first VM to run Windows 10 and the second to use Linux (Ubuntu) as their respective operating systems. Assign each VM two CPUs and ensure they are connected to the same Virtual Network (VNet). 

Once the setup is complete, use Remote Desktop to access the Windows 10 VM. Open a web browser and download Wireshark from [http://www.wireshark.org/download.html](http://www.wireshark.org/download.html). After installing and launching Wireshark, apply a filter to capture ICMP (Internet Control Message Protocol) traffic. ICMP is a protocol used for communication between devices, enabling one device to send messages when issues are detected. 

With the ICMP filter active in Wireshark, use the `ping` command to test connectivity by pinging the private IP address of the Linux VM. This process will generate ICMP traffic, which Wireshark can monitor and analyze to confirm network connectivity between the two hosts.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
