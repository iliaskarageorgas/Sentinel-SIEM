<h1>Sentinel SIEM</h1>

<h2>Description</h2>
This project consists of building a simple Microsoft Sentinel SIEM following muptiple tutorials. 


<h2>Languages and Utilities Used</h2>

- <b> Microsoft Azure Cloud</b>
- <b> Microsoft Sentinel</b>


<h2>Errors Occured </h2>

- <b>The specified domain either does not exist or could not be contacted:</b> This poped-up when I tried to join the domain SOC with the workstation VM. This happened because when I assigned the IP for the workstation, I put a wrong IP as a prefered DNS server. The correct way is to set as the DNS the AD server, so in my case the "SOC_AD" VM. On the image below the IP of the DNS is 192.168.10.10 which is not a system in my environment. The right way is the AD's IP 192.168.1.2. 
<p align="center">
<img src="https://i.imgur.com/XHSmegt.png" height="80%" width="80%" alt="SOC Lab"/>
<br />
<br />
</p> 
The AD server needs to be the DNS server of the workstation because firstly there is no DNS server in the environment and secondly because Active Directory relies heavily on name resolution, so the workstation can properly resolve domain names, locate AD resources such as domain controllers, and authenticate users.

<h2>Sources Used </h2>

- <b>Microsoft Sentinel Webpage: </b> https://www.microsoft.com/en-us/security/business/siem-and-xdr/microsoft-sentinel/
- <b>Basic Creation Tutorial: </b> https://medium.com/@cyberchops/building-microsoft-sentinel-siem-with-live-attack-monitoring-on-a-map-849749d60e6d
- <b>Helpful Article </b> https://hub.metronlabs.com/microsoft-sentinel-architecture-a-step-by-step-overview-of-integration-and-log-processing/
- <b>Helpful Video Tutorial </b> https://www.youtube.com/watch?v=g5JL2RIbThM

<h2>Creation walk-through:</h2>

<p align="center">
Making Azure Account <br/>
<img src="https://imgur.com/IssyYWm.png" height="80%" width="80%" alt="SOC Lab"/>
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
