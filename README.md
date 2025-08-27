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

<h3>VM and Sentinel Creation walk-through:</h3>
<p align="center">
Making Azure Account <br/>
<img src="https://imgur.com/IssyYWm.png" height="80%" width="80%" alt="SOC Lab"/>
<br />
<br />
Vitrual Machine Creation <br/>
<img src="https://imgur.com/4UvzpfK.png" height="80%" width="80%" alt="SOC Lab"/>
<br />
<br />
Creating Log Analytics Workspace  <br/>
<img src="https://imgur.com/tdUMrzn.png" height="80%" width="80%" alt="SOC Lab"/>
<br />
<br />
Leaving RDP open in order to get alerts <br/>
<img src="https://imgur.com/ENQ33XK.png" height="80%" width="80%" alt="SOC Lab"/>
<br />
<br />
Microsoft Sentinel Created <br/>
<img src="https://imgur.com/41qlYo0.png" height="80%" width="80%" alt="SOC Lab"/>
<br />
<br />
</p>

<h3>Sentinel Setup:</h3>
<p align="center">
Date Connectors<br />
<img src="https://imgur.com/YSDrt1Z.png" height="80%" width="80%" alt="SOC Lab"/>
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
