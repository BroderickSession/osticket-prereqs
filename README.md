<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket. Following this demonstration will result in a functional osTicketing system with an admin account, an internal admin and agent panel and a page that end users, can access and use to submit tickets.<br />





<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- PHP Manager 
- Rewrite Module
- PHP 7.3.8
- VC_redist.x86
- MySQL
- OsTicket
- HeidiSQL

<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Create a virtual machine in Azure that runs
Windows 10 and has 2-4 cores. Once it's intiated connect to it with remote desktop and enable IIS.
Do this by clicking on the search bar and searching control panel then go to programs and then click Windows features on or off and enable Internet Information Serves and then enable CGI inisde of Application Development Features and
Common HTTP Features also make sure lIS
Management Console is enabled inside of WebManagement Tools.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Open a web browser and type in 127.0.0.1 and if the installation worked then this page should appear. This address is the loopback address.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Install PHP Manager band be sure to click download anyway. then install the rewrite module and do the same. Use these links:
PHP Manager
Rewrite Module
</p>
<br />
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Create a folder in the C drive called PHP this is directory C:\PHP. Next install PHP 7.3.8 by using the link below:
PHP 7.3.8
</p>
<br />
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
This will download a ZIP file go to downloads in file explore right click on the folder and extract to
C:PHP
</p>
<br />
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Install VC_Redist and MySQL. The links will be below. When the setup wizard for MySQL launches do a typial and standard setup. Then set the password to be password1.
VC
MySQL
</p>
<br />
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Go to the Windows search bar and type in Internet Information Services to open its management window. Click on PHP manager and then register PHP with the directory shown in the above screen shot. After registering PHP reload IIS.
</p>
<br />
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Use the installation file link to install OsTicket and extract the upload folder to c:\inetpub|wwwroot and rename it to osTicket then reload IIS. Be sure to be running IIS as an administrator
Installation File
</p>
<br />
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
If every step was done correctly then you should see this screen when you click browse 80 on lIS after going to the Default Website branch on the left of the lIS manager.
</p>
<br />
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Go to the PHP manager and click on enable extensions and enable the extensions listed below by scrolling to it, right clicking and clicking enable rule:
Enable: php_imap.dll
Enable: php_intl.dll
Enable: php_oprache.dll
</p>
<br />
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Go to C:\inetpub wwwroot\osTicket\ include\ost-sampleconfig.php and rename the file ost-config .php then right click it go to properties and then security. Go to permissions disable its inheritence then add a principal and give everyone read/write permission.
</p>
<br />
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Install Heidi SQL and use root/password1 as the login and create a database called osTicket. Do this by right clicking unnamed then going to create new and then database.
HeidiSQL
</p>
<br />
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Go to OsTicket in your web browser continue the setup by adding in these texts for these fields:
MySQL Database: osTicker
MySQL Username: root
MySQL Password: password1
This should complete the installation and prompt you to begin the cleanup process which is to delete C: inetpub\wwwroot|osTicket\setup and to set permissions to Read only for
C: inetpub wwwroot osTicket include ost-config.php This concludes the setup demonstration for osTicket.
</p>
<br />
