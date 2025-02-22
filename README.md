<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

 
<h2>Description</h2>  
This tutorial outlines the post-install configuration of the open-source helpdesk ticketing system osTicket. It consists of setting up multiple agents along with their departments, roles, and permissions. As well as, configuring SLAs (Service Level Agreements), help topics, and users.<br />


<h2>List of Prerequisites</h2>

- Microsoft Azure
- Virtual Machine
- osTicket 

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)
- Windows 10
    

<h2>Program walk-through:</h2>
<p align="center">
First, we will acknowledge what agent panel vs admin panel looks like. We are admin and will use http://localhost/osTicket/scp/login.php to log in. Below is the agent panel (help desk): <br/>
<img src="https://i.imgur.com/e8IkkAn.png" height="80%" width="80%" 
<br />
<br />
In Admin panel, notice there are more admin technical control:  <br/>
<img src="https://i.imgur.com/7CW3RAj.png" height="80%" width="80%" 
<br />
<br />
In admin panel, we will configure Roles for grouping permissions in Admin Panel > Agents > Roles > Add New Role > we can name it Supreme Admin:  <br/>
<img src="https://i.imgur.com/MnAc8EI.png" height="80%" width="80%" 
<br />
<br />
For Supreme Admin, we will check off all permissions in tickets, tasks, and knowledge > Add new Role:  <br/>
<img src="https://i.imgur.com/nvTAz7N.png" height="80%" width="80%" <br/>
<br />
<br />
<img src="https://i.imgur.com/5HOSetv.png" height="80%" width="80%" <br/> 
<br />
<br />
<img src="https://i.imgur.com/ZyjpjHl.png" height="80%" width="80%"    
<br />
<br />
Supreme Admin (in admin panel you will see the button to switch to agent panel in right corner and vice versa):  <br/>
<img src="https://i.imgur.com/aRLt2q0.png" height="80%" width="80%" 
<br />
<br />
Configuring Departments for ticket visability to sysadmin. in Admin Panel > Agents > Departments > Give Top Level Department > we can name it SysAdmins:   <br/>
<img src="https://i.imgur.com/sxQB0bC.png" height="80%" width="80%" 
<br />
<br />
Configuring Teams for teams for different departments. In this situation we will use and name it online banking team. in Admin Panel > Agents > Teams (Pull Agents from different Departments):  <br/>
<img src="https://i.imgur.com/HB7NXYv.png" height="80%" width="80%" 
<br />
<br />
Configuring for anyone to create tickets. in Admin Panel > Settings -> User Settings > UNCHECK: unregistered users can create tickets. For lab purposes this is what we want:  <br/>
<img src="https://i.imgur.com/aLWoQjm.png" height="80%" width="80%" 
<br />
<br />
Configuring Agents/Workers, in this situation these are the actual workers in help desk. We can name our agents Jane Doe and John Doe. In Admin Panel > Agents > Create. We can set up Jane for primary sysadmin and Supreme Admin Access (will have all permissions, we will not uncheck any boxes) > online banking team:  <br/>
<img src="https://i.imgur.com/tnnwAeD.png" height="80%" width="80%" 
<br />
<br />
We can setup and type out Jane and John account name/passwords on this notepad just in case we forget:  <br/>
<img src="https://i.imgur.com/9zTiaQI.png" height="80%" width="80%" 
<br />
<br />
We can configure John. Email is fake and this situation john@gmail.com for support department and view only, we won't be assigning a team for John:  <br/>
<img src="https://i.imgur.com/nDIqeS0.png" height="80%" width="80%" 
<br />
<br />
To set up Jane Password, Agents > Jane Doe > Jane (should be typed in) > Set Password > uncheck Send the agent a password reset email and Require password at next login > type in Password1 > Update:  <br/>
<img src="https://i.imgur.com/fYfPaHH.png" height="80%" width="80%" 
<br />
<br />
Same step for set up for John:  <br/>
<img src="https://i.imgur.com/KO3Eucn.png" height="80%" width="80%" 
<br />
<br />
We will configure a user account name Karen. We will switch to Agent Panel > User > New:  <br/>
<img src="https://i.imgur.com/pwYB5ze.png" height="80%" width="80%" 
<br />
<br />
We can use a fake email karen@gmail.com > Add User:  <br/>
<img src="https://i.imgur.com/3DAdec3.png" height="80%" width="80%" 
<br />
<br />
Configure SLA, how much time to respond to a ticket. We can go back to Admin Panel > Manage > SLA:  <br/>
<img src="https://i.imgur.com/uBu1uDF.png" height="80%" width="80%" 
<br />
<br />
Click Add New SLA Plan and we can configure for name Sev-A (Grace Period: 1 hour, Schedule: 24/7):  <br/>
<img src="https://i.imgur.com/62MQWzS.png" height="80%" width="80%" 
<br />
<br />
Click Add New SLA Plan and we can configure for name Sev-B (Grace Period: 4 hours, Schedule: 24/7):  <br/>
<img src="https://i.imgur.com/Kns3Zkm.png" height="80%" width="80%" 
<br />
<br />
Click Add New SLA Plan and we can configure for name Sev-C (Grace Period: 8 hours, Business Hours):  <br/>
<img src="https://i.imgur.com/MiGTgPS.png" height="80%" width="80%" 
<br />
<br />
SLA PLAN:  <br/>
<img src="https://i.imgur.com/W6Odb7U.png" height="80%" width="80%" 
<br />
<br />
Next we can configure Help Topics 5 (for when users create tickets) Admin Panel > Manage > Help Topic > The first topic when be on Business Critical Outage > Parent topic: Report a Problem > Add Topic <br/>
<img src="https://i.imgur.com/jdICoxV.png" height="80%" width="80%" 
<br />
<br />
Help Topic 2 Personal Computer Issues > Parent topic: Report a Problem > Add Topic: <br/>
<img src="https://i.imgur.com/FRU9678.png" height="80%" width="80%" 
<br />
<br />
Help Topic 3 Equipment Request > Parent topic: General Inquiry > Add Topic: <br/>
<img src="https://i.imgur.com/ZQlxGPW.png" height="80%" width="80%" 
<br />
<br />
Help Topic 4 Password Reset > Parent topic: Report a Problem > Add Topic:  <br/>
<img src="https://i.imgur.com/I837xUM.png" height="80%" width="80%" 
<br />
<br />
Help Topic 5 Other > Parent topic: General Inquiry > Add Topic:  <br/>
<img src="https://i.imgur.com/ezHVGL1.png" height="80%" width="80%" 
<br />
<br />

<h2>osTicket Setup Complete!</h2>

<b> We've successfully set up multiple agents along with their departments, roles, and permissions. As well as, configured SLAs (Service Level Agreements), help topics, and users! osTicket is now setup for the next project where I will create and work different tickets using multiple agents and users!  </b>
<br />
<br />
