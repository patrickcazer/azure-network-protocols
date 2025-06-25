<p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" alt="Traffic Examination"/>
</p>

<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>
In this tutorial, we observe various network traffic to and from Azure Virtual Machines with Wireshark as well as experiment with Network Security Groups. <br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Various Command-Line Tools
- Various Network Protocols (SSH, RDH, DNS, HTTP/S, ICMP)
- Wireshark (Protocol Analyzer)

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Ubuntu Server 20.04

<h2>High-Level Steps</h2>

- Set up Azure Virtual Machines and configure intital network settings
- Set up remote connections to each virtual machine (RDP/SSH)
- Configure and apply network security groups (NSGs) with various inbound/outbound rules
- Use Wireshark and command-line tools to inspect and analyze traffic based on NSG configurations

<h2>Actions and Observations</h2>

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="NSG Rule Creation"/>
</p>
<p>
I created a Network Security group (NSG) and defined inbound rules allowing using RDP and SSH. RDP is on port 3389 and SSH is on port 22. Observed that connections succeeded after applying these rules.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Traffic Capture with Wireshark"/>
</p>
<p>
Captured network packets using Wireshark during an RDP session. Identified the protocol (TCP), source/destinations IPs, and confirmed encrypted traffic flow.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="NSG rule blocking ICMP"/>
</p>
<p>

Modified NSG rules to block ICM (ping). Attempted to ping the VM and verified packet loss in Wireshark, confirming the NSG rule was effective.
</p>
<br />
