<p align="center">
<img src="https://www.synaxiom.com/wp-content/uploads/2016/06/osticket.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites</h1>
This tutorial is a continuation of the installation of osTicket which is linked below if you have not completed it yet.</p>

- [osTicket: Prerequisites and Installation](https://github.com/bvongpradith/osticket-prereqs)

<h2>Environments and Technologies Used in Tutorial</h2>

- Microsoft Azure
- Remote Desktop
- Internet Information Services (IIS)
- osTicket
- HeidiSQL

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>Steps</h2>

- Configure Roles
- Configure Departments
- Configure Teams
- Download and install the Rewrite Module
- Allow anyone to create tickets
- Configure Agents (employees)
- Configure Users (customers)
- Configure SLAs
- Configure Help Topics

<h2>Detailed Steps</h2>

<p>
<img src="https://i.imgur.com/yl8X1a0.png"/>
</p>
<p>
We'll first go to the login (http://localhost/osTicket/scp/login.php) to login with the admin credentials from the previous tutorial.
</p>
<br />

<p>
<img src="https://i.imgur.com/dmMYsqY.png"/>
</p>
<p>
Next, click "Admin Panel" at the top right of the screen. The button will change to "Agent Panel" when you navigate inside the admin panel.
</p>
<br />

<p>
<img src="https://i.imgur.com/vUsbc7t.png"/>
</p>
<p>
Then go to Agents > Roles > Add New Role
</p>
<br />

<p>
<img src="https://i.imgur.com/MDQsMQh.png"/>
</p>
<p>
Now, name the role to "Supreme Admin" and then allow all permissions in the next tab. Click "Add Role".
</p>
<br />

<p>
<img src="https://i.imgur.com/L2QivIM.png"/>
</p>
<p>
Navigate to "Departments" and then click "Add New Department".
</p>
<br />

<p>
<img src="https://i.imgur.com/iEfRDDl.png"/>
</p>
<p>
Name the department to "SysAdmins" and then press "Create Dept".
</p>
<br />

<p>
<img src="https://i.imgur.com/cIVVFxB.png"/>
</p>
<p>
Head to the "Teams" panel and click "Create New Team". Name the new team "Level II Support" and press create.
</p>
<br />

<p>
<img src="https://i.imgur.com/RNCgiNh.png"/>
</p>
<p>
Afterwards, go to "Settings" > Users > Make sure the box for registration requirement is not checked > make the method public > Save Changes.
</p>
<br />

<p>
<img src="https://i.imgur.com/ovR6mDa.png"/>
</p>
<p>
Now go into the agents panel and add new agent.
</p>
<br />

<p>
<img src="https://i.imgur.com/zd2iMRm.png"/>
<img src="hthttps://i.imgur.com/agz55hK.png"/>
<img src="hthttps://i.imgur.com/JIuH5J6.png"/>
</p>
<p>
Create these accounts:

- Name:	Jane Doe
- Email Address: jane.doe@osticket.com
- Username: jane.doe
- Set the password to "Password1"
- Go to Access and set the department to SysAdmins and select Supreme Admin for the role.
- Go to the teams section and select Level II Support, then create.
  
After, create a second account for " John Doe"
</p>
<br />

<p>
<img src="https://i.imgur.com/rSCzZwo.png"/>
</p>
<p>
Then go to Agent panel > Users > Add User
</p>
<br />

<p>
<img src="https://i.imgur.com/xJAOXFN.png"/>
</p>
<p>
 Add the following users:
 
- Email Address: ken@osticket.com
- Full Name: Ken
  
- Email Address: karen@osticket.com
- Full Name: Karen
</p>
<br />

<p>
<img src="https://i.imgur.com/Wely6u8.png"/>
</p>
<p>
Head to Admin Panel > Manage > SLA > Add New SLA Plan.
</p>
<br />

<p>
<img src="https://i.imgur.com/mCNUD9g.png"/>
</p>
<p>
Next, add the following SLAs
  
- SEV-A with a grace period of 1 hour, and a 24/7 schedule
- SEV-B with a grace period of 4 hours, and a 24/7 schedule
- SEV-C with a grace period of 8 hours, and a Mon-Fri business hours schedule
</p>
<br />

<p>
<img src="https://i.imgur.com/vQ1k6as.png"/>
</p>
<p>
Now, navigate to "Help Topics" and add the following help topics:
  
- Business Critical Outage
- Personal Computer Issues
- Equipment Request
- Password Reset
