<h1>Sentinel SIEM</h1>

<h2>Description</h2>
This project consists of building a simple Microsoft Sentinel SIEM following muptiple tutorials. 


<h2>Languages and Utilities Used</h2>

- <b>Virtual Box</b>
- <b>PFSense</b> 
- <b>Windows 10 AD</b>
- <b>Windows 2022 Server</b>
- <b>BadBlood</b>
- <b>Sysmon</b>
- <b>Crowdsec</b>

<h2>Environments Used </h2>

- <b>Windows 10</b> 
- <b>Linux</b>

<h2>Virtual Machines Created </h2>

- <b>SOC_PFSENSE</b>: This machine was made for the software pfSense which is used as a Firewall/Router. 
- <b>SOC_AD</b>: This machine is used as an Active Directory Domain Controller.
- <b>SOC_Win10</b>: This machine is used as a simple workstation instance.

<h2>Errors Occured </h2>

- <b>The specified domain either does not exist or could not be contacted:</b> This poped-up when I tried to join the domain SOC with the workstation VM. This happened because when I assigned the IP for the workstation, I put a wrong IP as a prefered DNS server. The correct way is to set as the DNS the AD server, so in my case the "SOC_AD" VM. On the image below the IP of the DNS is 192.168.10.10 which is not a system in my environment. The right way is the AD's IP 192.168.1.2. 
<p align="center">
<img src="https://i.imgur.com/XHSmegt.png" height="80%" width="80%" alt="SOC Lab"/>
<br />
<br />
</p> 
The AD server needs to be the DNS server of the workstation because firstly there is no DNS server in the environment and secondly because Active Directory relies heavily on name resolution, so the workstation can properly resolve domain names, locate AD resources such as domain controllers, and authenticate users.

<h2>Sources Used </h2>

- <b>Let's Defend SOC Lab at Home lesson: </b> https://app.letsdefend.io/training/lessons/building-a-soc-lab-at-home
- <b>Sysmon Configuration XML: </b> https://github.com/olafhartong/sysmon-modular/blob/master/sysmonconfig.xml
- <b>Active Directory Video: </b> https://www.youtube.com/watch?v=SsN8pwIE1_Y
- <b>Various posts in Stackoverflow: </b> https://stackoverflow.com/
- <b>For image attachemnts: </b> https://imgur.com/
- <b>CrowdSec .msi installation </b> https://github.com/crowdsecurity/crowdsec/releases/tag/v1.6.1

<h2>Creation walk-through:</h2>

<h3>PfSense Virtual Machine:</h3>
<p align="center">
Cofiguring Network Adapters <br/>
<img src="https://i.imgur.com/STvaVTR.png" height="80%" width="80%" alt="SOC Lab"/>
<br />
<br />
pfSense Installer <br/>
<img src="https://i.imgur.com/9NOfSGO.png" height="80%" width="80%" alt="SOC Lab"/>
<br />
<br />
Configuring Network Interfaces:  <br/>
<img src="https://i.imgur.com/Q7870zq.png" height="80%" width="80%" alt="SOC Lab"/>
<br />
<br />
</p>

<h3>Active Directory Virtual Machine:</h3>
<p align="center">
Seting Up the VM and Windows 2022 Server OS <br/>
<img src="https://i.imgur.com/ZGaMNfh.png" height="80%" width="80%" alt="SOC Lab"/>
<br />
<br />
Network Adapter Configuration <br/>
<img src="https://i.imgur.com/HLDVosz.png" height="80%" width="80%" alt="SOC Lab"/>
<br />
<br />
Active Directory Installation  <br/>
<img src="https://i.imgur.com/IId9kTS.png" height="80%" width="80%" alt="SOC Lab"/>
<br />
<br />
Making the server a domain controller  <br/>
<img src="https://i.imgur.com/t5LdACo.png" height="80%" width="80%" alt="SOC Lab"/>
<br />
<br />
Adding a new AD forest  <br />
<img src="https://i.imgur.com/Bpk3jql.png" height="80%" width="80%" alt="SOC Lab"/>
<br />
<br />
Initiating BadBlood to populate Active Directory <br />
<img src="https://i.imgur.com/4e302ms.png" height="80%" width="80%" alt="SOC Lab"/>
<br />
<br />
</p>

<h3>Windows Workstation Virtual Machine:</h3>
<p align="center">
Windows 10 Workstation Setup<br />
<img src="https://i.imgur.com/p1aw3wd.png" height="80%" width="80%" alt="SOC Lab"/>
<br />
<br />
Windows 10 Workstation IP <br />
<img src="https://i.imgur.com/XHSmegt.png" height="80%" width="80%" alt="SOC Lab"/>
<br />
<br />
First pfSense and workstation interaction <br />
<img src="https://i.imgur.com/zCKA6iE.png" height="80%" width="80%" alt="SOC Lab"/>
<br />
<br />
Inserting workstation into the domain <br />
<img src="https://i.imgur.com/Cm7p0Af.png" height="80%" width="80%" alt="SOC Lab"/>
<br />
<br />
Installing Sysmon<br />
<img src="https://i.imgur.com/pidDaEp.png" height="80%" width="80%" alt="SOC Lab"/>
<br />
<br />
Installing CrowdSec<br />
<img src="https://i.imgur.com/3sqywQU.png" height="80%" width="80%" alt="SOC Lab"/>
<br />
<br />
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
