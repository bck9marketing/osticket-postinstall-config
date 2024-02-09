<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Post-Install Configuration</h1>
This tutorial outlines the post-install configuration of the open-source help desk ticketing system osTicket.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How To Configure osTicket, post-installation](https://youtu.be/i4pj6DpWM28)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>Post-Install Configuration Objectives</h2>

- Configure Roles, Departments, and Teams.
- Configure Service-Level Agreement(SLA)
- Configure Help Topics

<h2>Configuration Steps</h2>

<p>
<img src="https://github.com/bck9marketing/osticket-postinstall-config/assets/159003800/9e68d718-8307-4fe7-a9d3-1088acf79cc7" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
In this section we're going to start off by configuring a Supreme Admin role. First navigate to http://localhost/osTicket/scp/login.php through your browser. Log in with our previously created osTicket account - User: bob / Password: Password1. Once logged in, click "Admin Panel" in the top right.
</p>
<br />

<p>
<img src="https://github.com/bck9marketing/osticket-postinstall-config/assets/159003800/3002a9c4-88f9-4f90-b5dd-a2cc841cb345" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://github.com/bck9marketing/osticket-postinstall-config/assets/159003800/de820c07-8e80-4d24-a4d6-a28ab338c8ad" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Scroll over to the "Agents" tab and then click "Roles". Click "Add New Role".Here we will name the role "Supreme Admin" under the "Definition" tab, and under the "Permissions" tab, check everything under Tickets/Tasks/Knowledgebase. Once finished click "Add Role".
</p>
<br />

<p>
<img src="https://github.com/bck9marketing/osticket-postinstall-config/assets/159003800/dd8aa42b-16b4-4069-9abb-076c273b1e55" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next under that same "Agents" tab click "Departments" and then click "Add New Department". Name the department "System Administrators". Leave everything else as is and click "Create Dept".
</p>
<br />

<p>
<img src="https://github.com/bck9marketing/osticket-postinstall-config/assets/159003800/7d3e4990-67aa-4f4f-a365-fd75d079b9d6" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Under the same "Agents" tab, click "Teams" and then "Add New Team". We'll name this team "Level II Support" and under the "Members" tab we'll add "Bob" to this team. Once finished click "Create Team".
</p>
<br />

<p>
<img src="https://github.com/bck9marketing/osticket-postinstall-config/assets/159003800/d76d665d-20f5-474f-9a87-689bac39996b" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://github.com/bck9marketing/osticket-postinstall-config/assets/159003800/d4948452-e6d1-4c25-966a-30fdad840167" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://github.com/bck9marketing/osticket-postinstall-config/assets/159003800/44b57674-3495-4d72-ae0f-2af8d8c720a5" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://github.com/bck9marketing/osticket-postinstall-config/assets/159003800/7a255643-428e-4198-85c4-350032fbdc6e" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://github.com/bck9marketing/osticket-postinstall-config/assets/159003800/7c64fea3-b18f-432a-896d-9f0cd71aebc6" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lastly under the "Agents" tab, go to "Agents". Click "Add New Agent". We'll name the first agent Jane Doe and give her a basic username, email, and password. To give set passwords, click "Set Password", unselect "Send the agent a password reset email" and unselect "Require password change at next login". Then click "Set". Next go to the "Access" tab and add Jane to the "System Administrators" department and give her the "Supreme Admin" role. We'll also click "Add" under "Extended Access" and put her in the "Support" dept with the "Supreme Admin" role. This is so she also gets tickets that go to the Support dept. Next go to the "Teams" tab, select "Level II Support" in the dropdown and click "Add". Once finished, click "Create".<br>
 Now make one more agent named "John Doe", except this time we'll only put him in the "Support" department with "Expanded Access".<br>
   Our agents' info should be similar to the following:<br>
  - Name: Jane Doe / Email Address: jane.doe@osticket.com / Username: jane.doe / Password: Password1<br>
  - Name: John Doe / Email Address: john.doe@osticket.com / Username: john.doe / Password: Password1<br>
</p>
<br />

<p>
<img src="https://github.com/bck9marketing/osticket-postinstall-config/assets/159003800/d601a07b-956f-4be7-9686-f121f6fc6134" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://github.com/bck9marketing/osticket-postinstall-config/assets/159003800/d57860ec-25db-4130-8a7a-853220bd2267" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://github.com/bck9marketing/osticket-postinstall-config/assets/159003800/0666c6c8-d031-4f29-a757-648008db336f" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Now that we have created Roles, Departments, and Teams, we can head over to the "Agent Panel" and create some Users/Customers. In the "Agent Panel", scroll down to the "Users" tab and click "Add User". Here we'll create some very simple users. We'll name them Karen and Ken. Just input their names, give them simple emails, and then click "Add User".<br>
  - Karen / karen@osticket.com<br>
  - Ken / ken@osticket.com<br>
</p>
<br />

<p>
<img src="https://github.com/bck9marketing/osticket-postinstall-config/assets/159003800/05ff8a75-a2b6-4f6c-b632-9fc17057373b" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://github.com/bck9marketing/osticket-postinstall-config/assets/159003800/b3936c21-83c8-4c5b-a8ec-0b69baceadc3" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://github.com/bck9marketing/osticket-postinstall-config/assets/159003800/50dc1322-b942-4bc8-81fc-48b7d6ef7ede" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://github.com/bck9marketing/osticket-postinstall-config/assets/159003800/0bee15f0-9d16-464c-ad15-6fc1b01695f8" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://github.com/bck9marketing/osticket-postinstall-config/assets/159003800/92d3aaa3-5f5f-459f-bae1-0639c0567ce2" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Head back to the "Admin Panel", scroll over to the "Manage" tab, and click "SLA". Click "Add New SLA Plan". Here we will create 3 different SLA plans with varying degrees of severity. Fill out the "Name", "Grace Period", and "Schedule" according to the following list and then click "Add Plan":<br>
  - Name: Sev-A / Grace Period: 1 / Schedule: 24/7<br>
  - Name: Sev-B / Grace Period: 4 / Schedule: 24/7<br>
  - Name: Sev-C / Grace Period: 8 / Schedule: Monday-Friday(Business hours)<br>
</p>
<br />

<p>
<img src="https://github.com/bck9marketing/osticket-postinstall-config/assets/159003800/d6161d92-66af-4741-af5f-cb4e63ef2fa7" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
To finish this section off, we'll create some Help Topics. Under the same "Manage" tab click "Help Topics" and then click "Add New Help Topic". Here we will create 4 different help topics. Name them according to the list below, and then click Add Topic.<br>
  - Business Critical Outage<br>
  - Personal Computer Issues<br>
  - Equipment Request<br>
  - Password Reset<br>
</p>
<br />

<p>
<img src="https://github.com/bck9marketing/osticket-postinstall-config/assets/159003800/f83974c6-cad5-4e61-bba1-a75230d2817d" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
With those Help Topics created, our list should look like this^. We have now finished configuring osTicket and can begin testing how the average user would be able to submit tickets, as well as test how an employee would solve said tickets.
</p>
<br />
