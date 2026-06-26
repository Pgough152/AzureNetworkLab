# AzureNetworkLab

<h1>Azure Network</h1>


<h2>Description</h2>
Project consists using Azure to gain familiarity with the cloud service. I started by creating a Resource Group. After that a Storage Account was added to it. Once that is done, I created a simple text file and uploaded it to the Storage Account. From Azure, I edited the text file and saved it locally under a new file name. Afterwards I delete the entire Resource group from Azure and check on Cost Analysis.
<br />


<h2>Utilities Used</h2>

- <b>Microsoft Azure</b> 
- <b>Notepad</b>
- <b>Remote Desktop Connection</b>

<h2>Environments Used </h2>

- <b>Windows 11</b> 

<h2>Lab walk-through:</h2>

<p align="center">
Lab Checklist: <br/>
<img width="818" height="1055" alt="image" src="https://github.com/user-attachments/assets/60bb879c-a93b-4a3f-bcdd-441fc92fb537" />
<img width="814" height="744" alt="image" src="https://github.com/user-attachments/assets/e0a01344-5429-4702-83e3-35937081cc6b" />
<br />
<br />
Create Resource Group: <br/>
<img width="941" height="472" alt="image" src="https://github.com/user-attachments/assets/c47833a4-84af-4a00-b93f-3364758ea45a" />
<br />
<br />
Create Windows 10 Virtual Machine:
  
  I ran into a few roadblocks when creating the VM. I kept getting errors when selecting the size of the VM in US East. I found a workaround by selcting Central US as the region. Another issue I had was I could not pass validation when I would try to create the VM. I had to upgrade my Azure account from the free trial version to Pay-As-You Go for it to pass validation.<br/><br/><br/>
<img width="1112" height="945" alt="image" src="https://github.com/user-attachments/assets/4611970a-b7f4-4910-9cd2-cc4f683e188a" />
<img width="1040" height="945" alt="image" src="https://github.com/user-attachments/assets/7a5b09fa-ac94-4fe3-9bf9-cae0ea9ef248" />
<img width="1066" height="945" alt="image" src="https://github.com/user-attachments/assets/709c3bb3-6af5-43fb-9988-0281191bb8a8" />
<img width="1167" height="945" alt="image" src="https://github.com/user-attachments/assets/86b9fdda-95de-4fe7-b132-ea0224cccd98" />
<br />
<br />
Create Virtual Network:  <br/>
<img width="1495" height="945" alt="image" src="https://github.com/user-attachments/assets/58a2078c-dd9e-4abe-98bc-f63682655643" />
<br />
<br />
Create Linux VM on same network as Windows VM:  <br/>
<img width="912" height="471" alt="image" src="https://github.com/user-attachments/assets/048c22b9-a59f-4ca0-89ad-d399a882c4dc" />
<br />
<br />
Use Remote Desktop Connection to connect to Windows VM  <br/>
<img width="906" height="442" alt="image" src="https://github.com/user-attachments/assets/cc8ee7e2-80cb-4fe9-a09a-00496c0e7b8c" />
<br />
<br />
Install Wireshark onto Windows VM and open it:  <br/>
<img width="1352" height="948" alt="image" src="https://github.com/user-attachments/assets/3a4bd83a-1410-4199-be69-6e1d2ca1f078" />
  <br />
<br />
Filter for ICMP Traffic and ping Linux VM from within Windows VM and view traffic fom Wireshark:  <br/>

I tried to ping the public IP of the Linux VM and it Failed. I pinged the private IP of the VM and it connected.

<img width="1233" height="913" alt="image" src="https://github.com/user-attachments/assets/b6d63ad5-157c-451d-ae65-915f1b22bc46" />
<br />
<br />
Ping Google from Windows VM  <br/>
<img width="1281" height="870" alt="image" src="https://github.com/user-attachments/assets/93d4067b-e154-4662-9c9a-41849c2653b5" />
Set up a perpetual ping from Windows VM to Linux VM:  <br/>
<img width="1412" height="818" alt="image" src="https://github.com/user-attachments/assets/01358e82-bcc2-423f-8498-b4c5a88e4c7c" />

<br />
<br />
Configure Linux VM Firwall to block incoming pings:  <br/>

Azure>Virtual Machines>Linux VM>Networking>Network Settings>LinuxVM-nsg>Settings>Inbound security rules>Add  <br/>
<img width="323" height="577" alt="image" src="https://github.com/user-attachments/assets/7b8d1bed-7edb-4a60-b375-3ed80b655704" />
<img width="1362" height="532" alt="image" src="https://github.com/user-attachments/assets/aacdf9d7-4533-4d5e-b156-31135d4c506d" />
<img width="542" height="530" alt="image" src="https://github.com/user-attachments/assets/fd19ff21-ab82-4c61-9c1e-b9aa62859867" />
<img width="667" height="738" alt="image" src="https://github.com/user-attachments/assets/5fccc63f-fe0e-49d2-b125-477e96869fba" />
<img width="1236" height="392" alt="image" src="https://github.com/user-attachments/assets/21e39d01-a7a1-47dd-ac66-d83792a20246" />
<img width="990" height="453" alt="image" src="https://github.com/user-attachments/assets/f94f63f4-5544-4c36-b443-5713661273ba" />
<br />
<br />
Reenable ICMP Traffic to Linux VM <br/>
<img width="1247" height="68" alt="image" src="https://github.com/user-attachments/assets/ae986a51-1c98-4f55-924e-9979a88ec9fd" />
<img width="453" height="322" alt="image" src="https://github.com/user-attachments/assets/3063204b-c85d-40f8-aa45-dcc89ad87a17" />
<br />
<br />
Observe SSH traffic  <br/>

Powershell> ssh labuser@10.0.0.5
<img width="1412" height="877" alt="image" src="https://github.com/user-attachments/assets/1745c231-dcd9-4540-a76a-969c42c6ce48" />
<img width="1571" height="1023" alt="image" src="https://github.com/user-attachments/assets/3fa11604-b377-441e-aa55-1b9772627bcc" />
  <br />
<br />



Observing DHCP Traffic <br/>
<img width="1746" height="916" alt="image" src="https://github.com/user-attachments/assets/ac3d5541-f955-450a-bb67-5e38c652b987" />



<br />
<br />
Observe SSH traffic  <br/>
<img width="1412" height="877" alt="image" src="https://github.com/user-attachments/assets/1745c231-dcd9-4540-a76a-969c42c6ce48" />
<img width="1571" height="1023" alt="image" src="https://github.com/user-attachments/assets/3fa11604-b377-441e-aa55-1b9772627bcc" />
  <br />
<br />
Observe DNS Traffic<br/>
<img width="1691" height="681" alt="image" src="https://github.com/user-attachments/assets/3485a513-ca84-45fe-964a-2f26f60709e8" />
  <br />
<br />
Observe RDP Traffic <br/>
<img width="1337" height="827" alt="image" src="https://github.com/user-attachments/assets/c0f75f80-1c9b-42ee-9d0e-349d1ef6b95c" />
