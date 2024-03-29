<p align="center">
<img src="https://imgur.com/RTZL0Ru.png alt="Traffic Examination"/>  
</p>

<h1>Azure Virtual Machines Traffic Inspection (March 2023)</h1>
In this tutorial I analyze and observe various network traffic protocols between Azure Virtual Machines with Wireshark. This is a great excercise for anyone who seeks to learn about and observe network traffic in a controlled environment.  
<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines) abbreviated VM. VMs are used to install the software that is used to analyze the traffic being sent.

- Remote Desktop Protocol (RDP) is used to connect to the virtual machines and it is one type of traffic observed in wireshark. 

- Various Command-Line Tools are used such as Command Prompt for ping commands and Powershell to ssh into the second virtual machine.

- Network Protocols (SSH, RDH, DNS, ICMP, DHCP) are observed in wireshark as both VMs communicate with each other under various commands.

- Wireshark is the network traffic analyzer used to observe the different types of traffic being sent between both VMs.

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Ubuntu Server 20.04

<h2>Pre-Requisites</h2>
<h2>Creating the virtual machines<h2/>                                                             

- Step 1.a - After signing in to your Azure account, go into Resource Groups and create a Resource Group.

<p>
<img src="https://imgur.com/RR14RE3.png alt"Resource Group"/?
</p>
<br />
<br />

1.b Give it a name (click review and create).

<p>
<img src="https://imgur.com/gYES8J8.png alt"Resource Group"/?
</p>
<br />
<br />

1.c Then click create and wait a few moments....

<p>
<img src="https://imgur.com/CwSfMjG.png alt"Resource Group"/?
</p>
<br />
<br />

1.d The Resource Group is Created

<p>
<img src="https://imgur.com/gfKydDa.png alt"Rescource Group"/?
</p>
<br />
<br />

Step 2.a - Create two Virtual Machines. One Windows and one Linux (as displayed below).

<p>
<img src="https://imgur.com/q4UtpZY.png alt"Rescource Group"/?
</p>
<br />
<br />  
  
2b. Choose the resource group, name, region and operating system for the VM. Then click review and create.
<p>
<img src="https://imgur.com/CWIg88Z.png alt"Rescource Group"/?
</p>
<br />
<br />                                                            
                                                            
2c. Choose the size, create a username and password, click the confirm box then click review and create. 
<p>
<img src="https://imgur.com/pRi6kbD.png alt"Rescource Group"/?
</p>
<br />
<br />
  
2d. Also create a VM using Ubuntu as the operating system
<p>
<img src="https://imgur.com/Gcv021M.png alt"Rescource Group"/?
</p>
<br />                                                            
<br />
                                                            
2e. The virtual machine has been created                                                            
<p>
<img src="https://imgur.com/C1z2KlR.png alt"Rescource Group"/?
</p>
<br />                                                            
<br />

Step 3 - Log in to VM1 using it's ip address

<p>
<img src="https://imgur.com/pzsx4Xn.png alt"Rescource Group"/?
</p>

<p>
<img src="https://imgur.com/Hz2NxI2.png alt"Rescource Group"/?
</p>
<br />
<br />  

Step 4 - After logging in to the VM, navigate to Microsoft Edge and install Wireshark 

<p>
<img src="https://imgur.com/clrmTgG.png alt"Rescource Group"/?
</p>

<p>
<img src="https://imgur.com/plnj4UI.png alt"Rescource Group"/?
</p>
<br />
<br />
Now that you have logged in you can continue on to the traffic observation steps detailed below.
<br />
<br />
<br />  


<h2>Actions and Observations</h2>
These observations are made by inputting commands that corresond to the type of traffic one wishes to observe and then filtering Wireshark by the corresponding traffic type.
<br />
<br />

Below is RDP (Remote Desktop Protocol) traffic observation after filtering for RDP traffic in Wireshark 

<p>
<img src="https://imgur.com/CHAA6zi.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />


Below is DHCP (Dynamic Host Control Protocol) traffic observation using Wireshark

<p>
<img src="https://imgur.com/Gi74JxZ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />


Below is DNS (Domain Name System) traffic observation using Wireshark

<p>
<img src="https://imgur.com/NQQTI7C.png " height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />


Below is SSH (Secure Shell) traffic observation using Wireshark

<p>
<img src="https://imgur.com/2lxIu4v.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />


Below are the steps for ICMP (nternet Control Message Protocol) traffic observation from a perpetual ping and ICMP traffic stop after the inbound firewall rule is set 
<br />
1. Set the perpetual ping comand to ping VM2 and observe the ICMP traffic
<p>
<img src="https://imgur.com/cgRnPPG.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />
<br />

2. Change the Inbound firewall rule to deny ICMP traffic

<p>
<img src="https://imgur.com/gKmvkuS.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />
<br />


3. Observe the ping request times out after the firewall rule was put in place
(*note - The ping request timed out due to the ICMP traffic being denied as the firewall rule blocked the traffic)
<p>
<img src="https://imgur.com/dMWGgWi.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<h1>Thank Your for looking! For more content like this, visit <a href="https://exemplarysecurity.com">my website</a>☺</h1>

