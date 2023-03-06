<p align="center">
<img src="https://imgur.com/RTZL0Ru.png alt="Traffic Examination"/>
</p>

<h1>Azure Network Security Groups (NSGs) and Inspecting Traffic among Azure Virtual Machines</h1>
In this tutorial I demonstrate the various network traffic to and from Azure Virtual Machines with Wireshark as well as exploring Network Security Groups. <br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines)
- Remote Desktop Protocol
- Various Command-Line Tools 
- Network Protocols (SSH, RDH, DNS, ICMP, DHCP)
- Wireshark (network Traffic Analyzer)

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Ubuntu Server 20.04

<h2>Pre-Requisites</h2>

- Step 1.a - After signing in to your Azure account, go into Resource Groups and create a Resource Group.

<p>
<img src="https://imgur.com/RR14RE3.png alt"Resource Group"/?
</p>


1.b Give it a name (click review and create)

<p>
<img src="https://imgur.com/gYES8J8.png alt"Resource Group"/?
</p>


1.c Then click create and wait a few moments....

<p>
<img src="https://imgur.com/CwSfMjG.png alt"Resource Group"/?
</p>

1.d The Resource Group is Created

<p>
<img src="https://imgur.com/gfKydDa.png alt"Rescource Group"/?
</p>

- Step 2 - Create two Virtual Machines. One Windows and one Linux (as displayed below)

<p>
<img src="https://imgur.com/q4UtpZY.png alt"Rescource Group"/?
</p>

<p>
<img src="https://imgur.com/CWIg88Z.png alt"Rescource Group"/?
</p>

<p>
<img src="https://imgur.com/pRi6kbD.png alt"Rescource Group"/?
</p>

<p>
<img src="https://imgur.com/Gcv021M.png alt"Rescource Group"/?
</p>

<p>
<img src="https://imgur.com/C1z2KlR.png alt"Rescource Group"/?
</p>


- Step 3 - Log in to VM1 using it's ip address

<p>
<img src="https://imgur.com/pzsx4Xn.png alt"Rescource Group"/?
</p>

<p>
<img src="https://imgur.com/Hz2NxI2.png alt"Rescource Group"/?
</p>


- Step 4 - Afterlogging in to the VM, navigate to Microsoft Edge and install Wireshark 

<p>
<img src="https://imgur.com/clrmTgG.png alt"Rescource Group"/?
</p>

<p>
<img src="https://imgur.com/plnj4UI.png alt"Rescource Group"/?
</p>



<h2>Actions and Observations</h2>

RDP Traffic Observation after filtering for RDP traffic in Wireshark 

<p>
<img src="https://imgur.com/CHAA6zi.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />


DHCP traffic observation using Wireshark

<p>
<img src="https://imgur.com/Gi74JxZ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />


DNS traffic observation using Wireshark

<p>
<img src="https://imgur.com/NQQTI7C.png " height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />


SSH traffic observation using Wireshark

<p>
<img src="https://imgur.com/2lxIu4v.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />


ICMP traffic observation from perpetual ping and ICMP traffic stop after inbound firewall rule set  

<p>
<img src="https://imgur.com/cgRnPPG.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
<img src="https://imgur.com/gKmvkuS.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
<img src="https://imgur.com/dMWGgWi.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

Thank You for looking! For more, visit my [blog](https://exemplarysecurity.com/0

