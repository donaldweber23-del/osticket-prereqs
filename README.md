# osticket-prereqs
 <p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How To Install osTicket with Prerequisites](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Login to Virtual Machine and intstall OS ticket foder from Lab 3, Ticket Installation
- Login to Manilla folder and Extract files from the Download 
- Enable IIS in windows with CGI
- Unzip and Install files
- Open IIS and run as admin
- Start the process of installing and configuring ticket system
- Install Heidi and create Ticket Database.
- <img width="915" height="803" alt="image" src="https://github.com/user-attachments/assets/bf3f952b-59d8-4ac4-9659-0ba693f80d22" />


<h2>Installation Steps</h2>

<p>
<img width="1660" height="1054" alt="image" src="https://github.com/user-attachments/assets/fc05f2b1-d867-4fa9-a3d1-6815db0d4f95" />
<img width="1389" height="1063" alt="image" src="https://github.com/user-attachments/assets/30ec7ebe-8494-4e31-97f3-ee00bb49f2d6" />


</p>
<p>
Connect to your AZURE virtual machine using Remote Desktop Protocol. Get through sign in windows and then copy the OS zip files from the checklist in Lab 3, osTicketinstallation to your internet explorere in your virtual machine
Login to the Manilla folder, right click on the osTicket zip files and click extract all
</p>
<br />

<p>
<img width="1615" height="1004" alt="image" src="https://github.com/user-attachments/assets/71fdd8a7-9612-445d-8329-86f877cc7bf1" />
</p>
<p>
Enable Interent information services. Open control panel, click unistal program and then on the top left click on the windows feature. Inside locate the check box for IIS and enable. Follow the dropdown menu under world wide web services to Application Equipment Features. Enable CGI</p>
<br />

<p>
<img width="1652" height="1046" alt="image" src="https://github.com/user-attachments/assets/91d1e867-e731-4dd4-9ed1-26a8265dde7c" />
</p>
<p>
Install PHP Manager for IIS, Install rewrite module, Unzip PHP 7.3.8 into a C:\PHP (By creating new folder in C drive), and install VC_redist.x86.exe and MySQL 5.5.62 files (Typical setup, lauch configuration Wizard, Stadard configuration, username Root, password Root</p>

<img width="1734" height="944" alt="image" src="https://github.com/user-attachments/assets/4e89dbd1-a5ee-429b-9458-0cc9a7edbc63" />

Open IIS as an Admin

Register PHP from within IIS (PHP Manager -> C:\PHP\php-cgi.exe)

Reload IIS (Open IIS, Stop and Start the server)

Install osTicket v1.15.8
From the “osTicket-Installation-Files” folder, unzip “osTicket-v1.15.8.zip” and copy the “upload” folder into “c:\inetpub\wwwroot”
Within “c:\inetpub\wwwroot”, Rename “upload” to “osTicket”

<img width="1758" height="1060" alt="image" src="https://github.com/user-attachments/assets/d5c158fe-ddde-4fa2-a51c-cf6487e38fec" />
<img width="1433" height="1048" alt="image" src="https://github.com/user-attachments/assets/7b90d1a1-6eb2-49aa-9afc-7b8004e9daf5" />

Go to sites -> Default -> osTicket
On the right, click “Browse *:80”

Note that some extensions are not enabled
Go back to IIS, sites -> Default -> osTicket
Double-click PHP Manager
Click “Enable or disable an extension”
Enable: php_imap.dll
Enable: php_intl.dll
Enable: php_opcache.dll
Refresh the osTicket site in your browser, observe the changes

Rename: ost-config.php
From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php
To: C:\inetpub\wwwroot\osTicket\include\ost-config.php
<img width="955" height="269" alt="image" src="https://github.com/user-attachments/assets/07e2eaf6-ffba-4951-9698-089138ca752a" />

<img width="1481" height="815" alt="image" src="https://github.com/user-attachments/assets/503e1025-ddbe-4b4e-a375-7c7e40c854ce" />
<img width="1584" height="850" alt="image" src="https://github.com/user-attachments/assets/c177e16f-5ebb-4c58-98f4-7877d0721029" />

Assign Permissions: ost-config.php
Disable inheritance -> Remove All
New Permissions -> Everyone -> All

<img width="1162" height="821" alt="image" src="https://github.com/user-attachments/assets/5586bf4d-d490-42ec-bfc8-f28dc1a92427" />

Continue Setting up osTicket in the browser (click Continue)
Name Helpdesk
Default email (receives email from customers)

<img width="1007" height="938" alt="image" src="https://github.com/user-attachments/assets/e8b5a7d4-9e09-4074-a3ad-292d4fa8411b" />

From the “osTicket-Installation-Files” folder, install HeidiSQL.
Open Heidi SQL

<img width="856" height="670" alt="image" src="https://github.com/user-attachments/assets/5f4b7005-68b4-49f5-8c0b-9cd5fc93d5b9" />

Create a new session, root/root
Connect to the session

<img width="1001" height="652" alt="image" src="https://github.com/user-attachments/assets/24ca8008-d398-42b2-8ff6-cb492f94baea" />

Create a database called “osTicket”

<img width="1007" height="644" alt="image" src="https://github.com/user-attachments/assets/b2032403-6686-438c-9f0f-10bef72f97e4" />


Continue Setting up osTicket in the browser
MySQL Database: osTicket
MySQL Username: root
MySQL Password: root
Click “Install Now!”





Re
<br />

</p
 
