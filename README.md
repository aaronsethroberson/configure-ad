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

- Ubuntu Server 22.04
- Windows (Windows 10 Pro)

<h2>Deployment and Configuration Steps</h2>

Start by setting up two Virtual Machines (VMs) in Microsoft Azure. Configure the first VM to run Windows 10 and the second to use Linux (Ubuntu) as their respective operating systems. Assign each VM two CPUs and ensure they are connected to the same Virtual Network (VNet). 

Once the setup is complete, use Remote Desktop to access the Windows 10 VM. Open a web browser and download Wireshark from [http://www.wireshark.org/download.html](http://www.wireshark.org/download.html). After installing and launching Wireshark, apply a filter to capture ICMP (Internet Control Message Protocol) traffic. ICMP is a protocol used for communication between devices, enabling one device to send messages when issues are detected. 

With the ICMP filter active in Wireshark, use the `ping` command to test connectivity by pinging the private IP address of the Linux VM. This process will generate ICMP traffic, which Wireshark can monitor and analyze to confirm network connectivity between the two hosts. See image below.
</p>
<br />

<p>
<img src="https://i.ibb.co/YQfbRzR/1.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
In the next phase of the lab, we will use the `ping` command with the `-t` option and the private IP address of the Linux Virtual Machine. This will initiate a continuous ping that will run indefinitely until it is manually stopped or a response is received. While the Windows 10 VM is actively pinging the Linux VM, we will switch to the Linux VM and block all ICMP traffic using its firewall. This will involve creating a new Network Security Group for the Linux VM, configured to deny ICMP traffic. Consequently, the Linux VM will stop sending echo replies.
</p>
<br />

<p>
<img src="https://i.ibb.co/GCY0QM9/2.jpg" height="80%" width="80%" alt="Ping Commmand"/>
<img src="https://i.ibb.co/Tc8BHGb/3.jpg" height="80%" width="80%" alt="icmp deny"/>

</p>
<p>
As demonstrated below, disabling incoming ICMP traffic results in the message "Request Timed Out." To re-enable ICMP traffic, adjust the settings in the Linux Network Security Group to allow it. To stop the continuous pings, press `Ctrl+C`.
</p>
<br />
<p>
<img src="https://i.ibb.co/Q8nvKP3/4.jpg" height="80%" width="80%" alt="control c"/>
</p>

<p>
Next, we will configure Wireshark on the Windows 10 VM to filter for SSH (Secure Shell) traffic as we prepare to establish an SSH connection to the Linux VM. Since SSH operates without a graphical interface, it provides direct access to the command line. In the Command Prompt, we will execute the command `ssh username@10.0.0.5`, and Wireshark will begin capturing SSH packets as the connection is established.
</p>
<br />
<p>
<img src="https://i.ibb.co/RBy8sB2/5.jpg" height="80%" width="80%" alt="ssh"/>
</p>

<p>
While monitoring SSH traffic, we will run several Linux commands and examine the corresponding traffic captured in Wireshark.

* Linux Commands
  * id
  * hostname
  * pwd
  * touch 
  * ls
</p>
<br />
<p>
<img src="https://i.ibb.co/X7GwJBV/6.jpg" height="80%" width="80%" alt="commands"/>
</p>

<p>
In Wireshark, we’ll apply a filter for DHCP (Dynamic Host Configuration Protocol), which manages the assignment of network configurations and IP addresses to devices, enabling proper communication. DHCP operates on ports 67 and 68. After applying the DHCP filter, open the command prompt and execute the command `ipconfig /renew`. This command refreshes the device’s network settings by requesting a new IP address.
</p>
<br />
<p>
<img src="https://i.ibb.co/nb2ydmH/7.jpg" height="80%" width="80%" alt="ssh"/>
</p>

<p>
The Domain Name System (DNS) translates human-readable domain names into IP addresses, allowing computers to identify each other on a network. In Wireshark, apply a DNS filter, then open the command line and type `nslookup www.google.com`. This command queries the DNS to obtain the IP address associated with Google.
</p>
<br />
<p>
<img src="https://i.ibb.co/sqskLGt/8.jpg" height="80%" width="80%" alt="dns"/>
</p>

<p>
Finally, we’ll filter for RDP (Remote Desktop Protocol) traffic by using the filter `tcp.port==3389`. This will reveal continuous traffic, as RDP streams real-time data between computers, leading to ongoing network activity as live updates are transmitted.
</p>
<br />
<p>
<img src="https://i.ibb.co/MS5txBN/9.jpg" height="80%" width="80%" alt="ssh"/>
</p>
