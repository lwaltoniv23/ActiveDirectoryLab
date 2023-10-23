<h1>Active Directory Home Lab</h1>

 <!-- ### [YouTube Demonstration](https://youtu.be/7eJexJVCqJo) -->

<h2>Description</h2>
This repository contains steps on how i set up a basic home lab running Active Directory
<br />

<h2>Languages and Utilities Used</h2>

- <b>PowerShell</b> 
- <b>Active Directory</b>
- <b>Windows Server</b>
- <b>Virtualization (Oracle VirtualBox)</b> 

<h2>Diagram:</h2>

<p align="center">
<br/>
<img src="https://imgur.com/5mHWNV0.png" height="80%" width="80%"/>
<br/>

<!-- links to Windows websites for ISO files -->
<h2>Download and install Oracle VirtualBox from the official website.</h2>

<br>[Oracle VirtualBox](https://www.virtualbox.org)</br>

<h2>Download the Windows 10 and Windows Server 2019 ISO files</h2>

<br>[Windows 10 ISO](https://www.microsoft.com/en-us/software-download/windows10ISO)</br>
<br>[Windows Server 2019](https://www.microsoft.com/en-us/evalcenter/download-windows-server-2019)</br>


<h2>Create a new virtual machine by clicking on "NEW" in VirtualBox, name it "DC," and select the "Windows Server 2019" ISO file as the boot media.</h2>

<p align="center">
<br/>
<!-- new virtual machine image -->
<img src="https://imgur.com/zrVnxKy.png" height="80%" width="80%"/>
<br/>
<!-- hardware RAM image -->
<img src="https://imgur.com/aTGi9LM.png" height="80%" width="80%"/>
<br/>
<!-- virtual hard disk image -->
<img src="https://imgur.com/6wNygZf.png" height="80%" width="80%"/>
<br/>


<h2>Configure the virtual machine settings by giving it two netwoek adapters: one for connecting to the internet and the other for the internal private network.</h2>

<p align="center">
<br/>
<!-- newtwork adapter images -->
 <br>Network Adapter 1</br>
<img src="https://imgur.com/iKbPBli.png" height="80%" width="80%"/>
<br/>
 <br>Network Adapter 2 <br/>
<img src= "https://imgur.com/jtncQPr.png" height="80%" width="80%"/>
<br/>

<h2>Install Server 2019 on the virtual machine and set IP address for internal network.</h2>
<br>
<img src="https://imgur.com/X9asRqj.png" height="80%" width="80%"/>
<br/>
<img src="https://imgur.com/HUXrZWW.png" height="80%" width="80%"/>
<br/>

<h2>Name the Server and install Active Directory to create the domain.</h2>
<br>Name the Server<br/>
<img src="https://imgur.com/c4XbLHa.png" height="80%" width="80%"/>
<br/>
<br>Setup Server role<br/>
<img src="https://imgur.com/sqDXssy.png" height="80%" width="80%"/>
<br/>
<br>Add new forest and give domain name<br/>
<img src="https://imgur.com/iTTBTmj.png" height="80%" width="80%"/>
<br/>
<br>Give Domain Controller a password<br/>
<img src="https://imgur.com/dWPKA1k.png" height="80%" width="80%"/>
<br/>

<!-- setup internal private network -->
<h2>Form routing for private network internet access through the main domain controller</h2>
<br/>
<br>install routing</br/>
<img src="https://imgur.com/vazQREZ.png" height="80%" width="80%"/>
<br/>
<br>Select tools and Routing and Remote Access<br/>
<img src="https://imgur.com/KJQQheb.png" height="80%" width="80%"/>
<br/>
<br>Configure NAT<br/>
<img src="https://imgur.com/FzpmDgA.png" height="80%" width="80%"/>
<img src="https://imgur.com/xh7NN2K.png" height="80%" width="80%"/>
<br/>

<h2>Setup DHCP on the domain controller.</h2>
<br/>
<br>diagram of settings</br/>
<img src="https://imgur.com/JxuzbBt.png" height="40%" width="40%"/>
<br/>
<br>install DHCP server role<br/>
<img src="https://imgur.com/fnAjIAA.png" height="80%" width="80%"/>
<br/>
<br>Select tools and DHCP<br/>
<img src="https://imgur.com/9wh1KYs.png" height="80%" width="80%"/>
<br/>
<br>Add new scope<br/>
<img src="https://imgur.com/ZjTcFYM.png" height="80%" width="80%"/>
<br/>
<br>Enter IP range</br/>
<img src="https://imgur.com/Sdtfsga.png" height="80%" width="80%"/>
<img src="https://imgur.com/90aBpf7.png" height="80%" width="80%"/>
<br/>

<h2>Run Powershell to create users in Active Directory</h2>
<br><br/>
<h2>Create and install Windows 10 on a new virtual machine named "Client1"</h2>
<br><br/>

</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
