<h1>Sentinel SIEM</h1>

<h2>Description</h2>
This project consists of building a simple Microsoft Sentinel SIEM following muptiple tutorials. After Setup, I used it to make a simple rule and check for alert creation. 
The rule consisted of a simple KQL query that alerts if a successfull RDP connection was initiated. 
In order to generate the alert, I left the RDP port (3389) open to public and connected via RDP from my own PC. 
The alert was generated successfully as seen on the last part of this page. 


<h2>Languages and Utilities Used</h2>

- <b> Microsoft Azure Cloud</b>
- <b> Microsoft Sentinel</b>
- <b> Kusto Query Language</b>


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
Data Connectors<br />
<img src="https://imgur.com/YSDrt1Z.png" height="80%" width="80%" alt="SOC Lab"/>
<br />
<br />
Data Connection Rule <br />
<img src="https://imgur.com/WOG1Aya.png" height="80%" width="80%" alt="SOC Lab"/>
<br />
<br />
Rule Creation <br />
<img src="https://imgur.com/ZH5FA8l.png" height="80%" width="80%" alt="SOC Lab"/>
<br />
<br />
Rule Settings<br />
<img src="https://imgur.com/989hRyD.png" height="80%" width="80%" alt="SOC Lab"/>
<br />
<br />
The Rule is Ready<br />
<img src="https://imgur.com/EJZi0mt.png" height="80%" width="80%" alt="SOC Lab"/>
<br />
<br />
</p>

<h3>Rule Testing</h3>
<p align="center">
Connecting via RDP<br />
<img src="https://imgur.com/zqHKdB0.png" height="80%" width="80%" alt="SOC Lab"/>
<br />
<br />
Connecting via RDP from my PC<br />
<img src="https://imgur.com/h1qL3CA.png" height="80%" width="80%" alt="SOC Lab"/>
<br />
<br />
Connected Successfully<br />
<img src="https://imgur.com/CoDw9ac.png" height="80%" width="80%" alt="SOC Lab"/>
<br />
<br />
Incident Spotted via Advanced Hunting<br />
<img src="https://imgur.com/zWRombk.png" height="80%" width="80%" alt="SOC Lab"/>
<br />
<br />
Incident-Alert Created as Expected<br />
<img src="https://imgur.com/UDeYSY3.png" height="80%" width="80%" alt="SOC Lab"/>
<br />
<br />
Alerting Correctly For My Desktop (as seen on the CMD console)<br />
<img src="https://imgur.com/ehI8m0n.png" height="80%" width="80%" alt="SOC Lab"/>
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
