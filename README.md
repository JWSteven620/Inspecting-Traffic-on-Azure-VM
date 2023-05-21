# Inspecting-Traffic-on-Azure-VM
<p align="center">
<img src="https://www.eilegal.com.au/wp-content/uploads/2020/07/when-is-a-formal-workplace-investigation-required_BLOG.jpg" alt="Traffic Examination"/>
</p>

<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>
This tutorial entails the analysis of network traffic to and from Azure Virtual Machines utilizing Wireshark, alongside practical exploration of Network Security Groups for enhanced network security measures. <br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Various Command-Line Tools
- Various Network Protocols (DHCP, DNS, ICMP)
- Wireshark (Protocol Analyzer)

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Ubuntu Server 20.04

<h2>Steps</h2>
<p>
<img src="https://i.imgur.com/v64tCNc.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

- Create both VMs in Azure and make sure they are on the same network
- Login the Windows VM and Download wireshark

<br />

<p>
<img src="https://i.imgur.com/7pbezun.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

- Once logged in download Wireshark and Install wireshark

<br />

<p>
<img src="https://i.imgur.com/dXEEbxj.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

- Open wireshark and proceed to capture traffic by selecting Ethernet

<br />

<p>
<img src="https://i.imgur.com/3HM8ekU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

- Open Command Prompt and use the following commands
  -ping (private IP of unbuntu vm) 
  -nslookup disney.com
  -ipconfig /renew
- Once you entered all three commands stop wireshark from capturing packets 

<br />

<p>
<img src="https://i.imgur.com/dxuLUDm.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

- In the filter in wireshark type ICMP
- This is the traffic produced by the ping  

<br />

<p>
<img src="https://i.imgur.com/w8Wu7In.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

- In the filter in wireshark type DHCP
- This is the traffic produced by the nslookup 

<br />

<p>
<img src="https://i.imgur.com/uZizIwv.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

- In the filter in wireshark type DNS
- This is the traffic produced by the ipconfig /renew

<br />
