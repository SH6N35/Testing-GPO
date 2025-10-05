<h1>Testing Group Policy Objects</h1>

<h2>Description</h2>
This project demonstrates how to add a windows machine to a windows server as well as testing gpo's on this client machine.
<br />


<h2>Languages and Utilities Used</h2>

- <b>VMware Workstation Pro</b>
- <b>Group Policy Managment</b> 

<h2>Environments Used </h2>

- <b>Windows Server 2022 ISO</b>
- <b>Windows 10 Enterprise</b>

<h2>Program walk-through:</h2>

<p align="center">
Install a new Windows VM in VMware pro: <br/>
<img src="https://i.imgur.com/9iuyncE.png"/>
<br />
<br />
Open cmd in Windows server VM and use the command prompt ipconfig this will show us the assigned IP address subnet and gateway use this to assign a static IP to the server:  <br/>
<img src="https://i.imgur.com/Y2Aw5Yg.png"/>
<br />
<br />
Assign those values to your servers IPv4 properties without a static IP our windows 10 vm would need to be reconfigured to this server every time we restarted it!: <br/>
<img src="https://i.imgur.com/M24olMC.png"/>
<br />
<br />
Open your Windows 10 Enterprise VM and configure the IPv4 properties to use your servers DNS address:  <br/>
<img src="https://i.imgur.com/tFp36Uq.png"/>
<br />
<br />
Add your VM to the domain:  <br/>
<img src="https://i.imgur.com/mpFB28a.png"/>
<br />
<br />
Sign in to this newly added VM with an already created user in the domain:  <br/>
<img src="https://i.imgur.com/JVKVyMi.png"/>
<br />
<br />
Apply GPO's by dragging them into their respective OU's ex: Password policy is used by the computer so drag it into the computer OU:  <br/>
<img src="https://i.imgur.com/mMQ1tyT.png"/>
<br />
<br />
The new computer will be added to your servers AD add it under it's respective OU this is best pratice in the work place:  <br/>
<img src="https://i.imgur.com/2dSi5ZY.png"/>
<br />
<br />
GPO's typically update every 30-90 minutes you can force them to update by using the cmd prompt gpupdate /force:  <br/>
<img src="https://i.imgur.com/KV70F89.png"/>
<br />
<br />
</p>
