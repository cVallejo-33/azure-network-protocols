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

- Step 1 Environment Setup

Provisioned virtual machines in Microsoft Azure
Configured networking settings, including virtual networks and firewall rules
Established remote access using RDP (Windows) and SSH (Linux)
- Step 2 System Configuration & Connectivity Testing

Installed and configured necessary tools on both Windows and Ubuntu systems
Verified connectivity between machines using protocols such as ICMP (ping) and SSH
Tested web traffic using HTTP/HTTPS to ensure proper network communication
- Step 3 Network Traffic Analysis

Captured live network traffic using Wireshark
Analyzed different protocol behaviors (DNS queries, HTTP requests, ICMP packets, etc.)
Identified packet structures and troubleshooting insights from captured data 


<h2>Actions and Observations</h2>

<p>
<img width="600" height="323" alt="image" src="https://github.com/user-attachments/assets/4059a6cf-a03c-44e6-ae3e-59d42ff86101" />

</p>
<p>
Step 1: View the Network Security Group rules in the Azure Portal. Inbound rules are shown here, listing rules that allow and deny specific traffic to the Virtual Machine 
</p>
<br />

<p>
<img width="562" height="251" alt="image" src="https://github.com/user-attachments/assets/27098ac7-41d6-4457-bf71-7bdd77e3a6b6" />


</p>
<p>

Step 2: Capturing SSH traffic using Wireshark. This screenshot shows Wireshark capturing and analyzing SSH traffic between two Azure VM's. The traffic is displayed in Wireshark.
</p>
<br />

<p>
<img width="565" height="184" alt="image" src="https://github.com/user-attachments/assets/80358805-142d-4791-9d14-c6eac2b9ccc4" />

</p>
<p>

Step 3: Blocking SSH traffic by adjusting NSG rules. Here, the NSG rule for port 22 is changed from "Allow" to Deny, blocking SSH traffic to the VM. On the right, Wireshark captures a failed SSH connection attempt after adjusting the firewall rule. 
</p>
<br />
