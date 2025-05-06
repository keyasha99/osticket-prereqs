<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Create an Azure Virtual Machine - Windows 10, 2vcpus
- Download the [osTicket-Installation-Files.zip](https://drive.google.com/uc?export=download&id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD) and unzip it onto your desktop. The folder should be called “osTicket-Installation-Files”
- Install / Enable IIS in Windows WITH CGI

<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/G8pVCzh.png" height="80%" width="80%" alt="osTicket Installation"/>
</p>
<p>
From the osTicket-Installation-Files, install the PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi). Once that is finished, install the Rewrite Module (rewrite_amd64_en-US.msi).
</p>
<br />

<p>
<img src="https://i.imgur.com/MDYZl8v.png" height="80%" width="80%" alt="osTicket Installation"/>
</p>
<p>
Create the directory C:\PHP by creating a new folder in the Windows (C:) drive.
</p>
<br />

<p>
<img src="https://i.imgur.com/B8ixJ4r.png" height="80%" width="80%" alt="osTicket Installation"/>
</p>
<p>
Going back to the osTicket-Installation-Files folder, unzip PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) into the “C:\PHP” folder.
</p>
<br />

<p>
<img src="https://i.imgur.com/FtUTUCp.png" height="80%" width="80%" alt="osTicket Installation"/>
</p>
<p>
From the osTicket-Installation-Files folder, install VC_redist.x86. Then, install MySQL 5.5.62 (mysql-5.5.62-win32.msi).
</p>
<br />

<p>
<img src="https://i.imgur.com/AXbPmv6.png" height="80%" width="80%" alt="osTicket Installation"/>
</p>
<p>
Select the Typical setup type and continue with the installation.
</p>
<br />

<p>
<img src="https://i.imgur.com/SunpYWM.png" height="80%" width="80%" alt="osTicket Installation"/>
</p>
<p>
Make sure the box is checked for Launch the MySQL Instance Configuration Wizard.
</p>
<br />

<p>
<img src="https://i.imgur.com/ErU8ivN.png" height="80%" width="80%" alt="osTicket Installation"/>
</p>
<p>
Select Standard Configuration and continue.
</p>
<br />

<p>
<img src="https://i.imgur.com/BLLA2pe.png" height="80%" width="80%" alt="osTicket Installation"/>
</p>
<p>
Check the Modify Security Settings and to make things easier, set the username and password to root. I suggest saving a text file for all of the credentials that you will be using. The osTicket Admin login is saved for later. Continue with installation.
</p>
<br />

<p>
<img src="https://i.imgur.com/QXfWn02.png" height="80%" width="80%" alt="osTicket Installation"/>
</p>
<p>
Open IIS as an Administrator. Click on PHP.
</p>
<br />

<p>
<img src="https://i.imgur.com/iuZhaeo.png" height="80%" width="80%" alt="osTicket Installation"/>
</p>
<p>
Click on Register new PHP version. Follow along through the next couple of pictures.
</p>
<br />

<p>
<img src="https://i.imgur.com/AmSEQVJ.png" height="80%" width="80%" alt="osTicket Installation"/>
</p>
<br />

<p>
<img src="https://i.imgur.com/VvFQAZD.png" height="80%" width="80%" alt="osTicket Installation"/>
</p>
<br />

<p>
<img src="https://i.imgur.com/vsXYn5A.png" height="80%" width="80%" alt="osTicket Installation"/>
</p>
<br />

<p>
<img src="https://i.imgur.com/uOZYGOC.png" height="80%" width="80%" alt="osTicket Installation"/>
</p>
<br />

<p>
<img src="https://i.imgur.com/0oXzSqr.png" height="80%" width="80%" alt="osTicket Installation"/>
</p>
<p>
Go back to the osticket-vm Home and reload IIS by going to the right side of the window and clicking on Stop and then Start.
</p>
<br />

<p>
<img src="https://i.imgur.com/KflXZZe.png" height="80%" width="80%" alt="osTicket Installation"/>
</p>
<p>
Now you're going to install osTicket v1.15.8. First, go to the osTicket-Installation-Files folder and unzip the folder. You don't have to change the destination for the unzipped folder. Leave this window open.
</p>
<br />

<p>
<img src="https://i.imgur.com/FIzJk2T.png" height="80%" width="80%" alt="osTicket Installation"/>
</p>
<p>
Open another File Explorer window and go to Windows (C:) drive. Click on the inetpub folder and then the wwwroot folder.
</p>
<br />

<p>
<img src="https://i.imgur.com/QAU6tof.png" height="80%" width="80%" alt="osTicket Installation"/>
</p>
<p>
Copy the  the “upload” folder into “c:\inetpub\wwwroot” by dragging in and rename "upload" to osTicket.
</p>
<br />

<p>
<img src="https://i.imgur.com/KUgXGXB.png" height="80%" width="80%" alt="osTicket Installation"/>
</p>
<p>
Open IIS and reload it again.
</p>
<br />

<p>
<img src="https://i.imgur.com/S2q8Tmh.png" height="80%" width="80%" alt="osTicket Installation"/>
</p>
<p>
On the left side of the window, click on the os-ticket vm server and expand it. Go to Sites, Default Web Site, then osTicket. On the right side, click on Browse *:80 (http) to load the osTicket site.
</p>
<br />

<p>
<img src="https://i.imgur.com/n19nDBT.png" height="80%" width="80%" alt="osTicket Installation"/>
</p>
<p>
As you can see, there are some extensions that are not enabled. You have to go back to IIS and enable them. 
</p>
<br />

<p>
<img src="https://i.imgur.com/0WxfI1T.png" height="80%" width="80%" alt="osTicket Installation"/>
</p>
<p>
Double click on PHP Manager.
</p>
<br />

<p>
<img src="https://i.imgur.com/Gbi6ASp.png" height="80%" width="80%" alt="osTicket Installation"/>
</p>
<p>
Under PHP Extension, click on Enable or disable an extension.
</p>
<br />

<p>
<img src="https://i.imgur.com/C8x2Ywj.png" height="80%" width="80%" alt="osTicket Installation"/>
</p>
<p>
Find and enable these extensions by right-clicking on them and selecting Enable: php_imap.dll, php_intl.dll, & php_opcache.dll. After, you can refresh the osTicket website and see the changes.
</p>
<br />

<p>
<img src="https://i.imgur.com/WYvQ2TI.png" height="80%" width="80%" alt="osTicket Installation"/>
</p>
<p>
Go to C:\inetpub\wwwroot\osTicket\include. Scroll down to ost-sampleconfig.php and rename it to ost-config.php.
</p>
<br />

<p>
<img src="https://i.imgur.com/VyCl6Tq.png" height="80%" width="80%" alt="osTicket Installation"/>
</p>
<p>
Now you're going to assign permissions. Right click on ost-config.php and got to Properties. Go to the Security tab and click on Advanced.
</p>
<br />

<p>
<img src="https://i.imgur.com/B8ixJ4r.png" height="80%" width="80%" alt="osTicket Installation"/>
</p>
<p>
Going back to the osTicket-Installation-Files folder, unzip PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) into the “C:\PHP” folder.
</p>
<br />

<p>
<img src="https://i.imgur.com/B8ixJ4r.png" height="80%" width="80%" alt="osTicket Installation"/>
</p>
<p>
Going back to the osTicket-Installation-Files folder, unzip PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) into the “C:\PHP” folder.
</p>
<br />

<p>
<img src="https://i.imgur.com/B8ixJ4r.png" height="80%" width="80%" alt="osTicket Installation"/>
</p>
<p>
Going back to the osTicket-Installation-Files folder, unzip PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) into the “C:\PHP” folder.
</p>
<br />

<p>
<img src="https://i.imgur.com/B8ixJ4r.png" height="80%" width="80%" alt="osTicket Installation"/>
</p>
<p>
Going back to the osTicket-Installation-Files folder, unzip PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) into the “C:\PHP” folder.
</p>
<br />

<p>
<img src="https://i.imgur.com/B8ixJ4r.png" height="80%" width="80%" alt="osTicket Installation"/>
</p>
<p>
Going back to the osTicket-Installation-Files folder, unzip PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) into the “C:\PHP” folder.
</p>
<br />
