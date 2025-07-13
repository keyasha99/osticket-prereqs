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

<h3>Create an Azure Virtual Machine - Windows 10, 2vcpus</h3>

<p>
<img src="https://i.imgur.com/GWreerA.png" alt="osTicket Installation"/>
</p>
<p>
To begin this tutorial, you will create a Windows 10 VM. In Microsoft Azure, look up Virtual machines and go to it.
</p>
<br />

<p>
<img src="https://i.imgur.com/VoaxXjH.png" alt="osTicket Installation"/>
</p>
<p>
Click the Create button and go to Virtual machine.
</p>
<br />

<p>
<img src="https://i.imgur.com/xERjTzh.png" alt="osTicket Installation"/>
</p>
<p>
For Resource group, go to Create new and name it. Once done, click OK.
</p>
<br />

<p>
<img src="https://i.imgur.com/y67f6Uk.png" alt="osTicket Installation"/>
</p>
<p>
Name your virtual machine and set the region to whatever region you live in.
</p>
<br />

<p>
<img src="https://i.imgur.com/qUTHP8y.png" alt="osTicket Installation"/>
</p>
<p>
For image, select the Windows 10 Pro that you see in the picture. For size, make sure you select one with at least 2vcpus.
</p>
<br />

<p>
<img src="https://i.imgur.com/66kGHc4.png" alt="osTicket Installation"/>
</p>
<p>
Create a username and password to log into the VM.
</p>
<br />

<p>
<img src="https://i.imgur.com/QM6Sq4F.png" alt="osTicket Installation"/>
</p>
<p>
Check the box for Licensing and click Next to Disks.
</p>
<br />

<p>
<img src="https://i.imgur.com/Q7cOcxv.png" alt="osTicket Installation"/>
</p>
<p>
Click Next to Networking.
</p>
<br />

<p>
<img src="https://i.imgur.com/hIriBJC.png" alt="osTicket Installation"/>
</p>
<p>
Here, Azure should have created a virtual network for you already. Leave everything as is and go to Review + create.
</p>
<br />

<p>
<img src="https://i.imgur.com/n2G1tZ7.png" alt="osTicket Installation"/>
</p>
<p>
Click Create.
</p>
<br />

<p>
<img src="https://i.imgur.com/3QYOmcX.png" alt="osTicket Installation"/>
</p>
<br />

<p>
<img src="https://i.imgur.com/e2r09wA.png" alt="osTicket Installation"/>
</p>
<p>
Once the virtual machine is finished deploying, go back into Virtual machines.
</p>
<br />

<p>
<img src="https://i.imgur.com/gBULkws.png" alt="osTicket Installation"/>
</p>
<p>
Go to the Start icon on your computer and open Remote Desktop Connection.
</p>
<br />

<img src="https://i.imgur.com/oSLzLFf.png" alt="osTicket Installation"/>
</p>
<p>
Copy and paste your VM's public IP address in the bar and click Connect.
</p>
<br />

<img src="https://i.imgur.com/HpTEtHB.png" alt="osTicket Installation"/>
</p>
<p>
Go to More choices.
</p>
<br />

<img src="https://i.imgur.com/kdjig6R.png" alt="osTicket Installation"/>
</p>
<p>
Click Use a different account.
</p>
<br />

<img src="https://i.imgur.com/7AWvYBh.png" alt="osTicket Installation"/>
</p>
<p>
Enter the username and password you've created during the setup of the VM and click OK.
</p>
<br />

<img src="https://i.imgur.com/WHw0SWr.png" alt="osTicket Installation"/>
</p>
<p>
Click Yes and you'll be logged into the VM.
</p>
<br />

- Download the [osTicket-Installation-Files.zip](https://drive.google.com/uc?export=download&id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD) and unzip it onto your desktop. The folder should be called “osTicket-Installation-Files”

- Install / Enable IIS in Windows WITH CGI

<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/G8pVCzh.png" height="80%" width="80%" alt="osTicket Installation"/>
</p>
<p>
From the osTicket-Installation-Files, install the PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi). Then, install the Rewrite Module (rewrite_amd64_en-US.msi).
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
Check the Modify Security Settings. To make things easier, I set the username and password to root, but you can use whatever you want. I suggest saving a text file for all the credentials you will be using. The osTicket Admin login is saved for later. Continue with the installation.
</p>
<br />

<p>
<img src="https://i.imgur.com/QXfWn02.png" height="80%" width="80%" alt="osTicket Installation"/>
</p>
<p>
Now you're going to register PHP. Open IIS as an Administrator and click on PHP.
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
Return to the osticket-vm Home and reload IIS by going to the right side of the window and clicking on Stop and then Start.
</p>
<br />

<p>
<img src="https://i.imgur.com/KflXZZe.png" height="80%" width="80%" alt="osTicket Installation"/>
</p>
<p>
Now, you're going to install osTicket v1.15.8. First, go to the osTicket-Installation-Files folder and unzip it. You don't have to change the destination for the unzipped folder. Leave this window open.
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
Copy the  the “upload” folder into “c:\inetpub\wwwroot” by dragging it and rename "upload" to osTicket.
</p>
<br />

<p>
<img src="https://i.imgur.com/KUgXGXB.png" height="80%" width="80%" alt="osTicket Installation"/>
</p>
<p>
Open IIS and reload it.
</p>
<br />

<p>
<img src="https://i.imgur.com/S2q8Tmh.png" height="80%" width="80%" alt="osTicket Installation"/>
</p>
<p>
On the left side of the window, click on the os-ticket vm server and expand it. Go to Sites, Default Web Site, then osTicket. On the right side, click Browse *:80 (http) to load the osTicket site.
</p>
<br />

<p>
<img src="https://i.imgur.com/n19nDBT.png" height="80%" width="80%" alt="osTicket Installation"/>
</p>
<p>
As you can see, some extensions are not enabled. You have to go back to IIS and enable them.  
</p>
<br />

<p>
<img src="https://i.imgur.com/0WxfI1T.png" height="80%" width="80%" alt="osTicket Installation"/>
</p>
<p>
Double-click on PHP Manager.
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
Find and enable these extensions by right-clicking on them and selecting Enable: php_imap.dll, php_intl.dll, and php_opcache.dll. Then, you can refresh the osTicket website to see the changes.
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
NNow, you'll assign permissions. Right-click on ost-config.php and go to Properties. Then, go to the Security tab and click on Advanced.
</p>
<br />

<p>
<img src="https://i.imgur.com/LJQlPt2.png" height="80%" width="80%" alt="osTicket Installation"/>
</p>
<p>
Click on Disable inheritance and select Remove all inherited permissions from this object. After that, click on Add and then Select a principal in the next window.
</p>
<br />

<p>
<img src="https://i.imgur.com/GjEIMbI.png" height="80%" width="80%" alt="osTicket Installation"/>
</p>
<p>
Assign permissions to anyone you want for the object name. For this tutorial, I put Everyone. Click Check Names and then OK.
</p>
<br />

<p>
<img src="https://i.imgur.com/o6JnkkW.png" height="80%" width="80%" alt="osTicket Installation"/>
</p>
<p>
Check the box Full Control and click OK.
</p>
<br />

<p>
<img src="https://i.imgur.com/6x662wu.png" height="80%" width="80%" alt="osTicket Installation"/>
</p>
<p>
Click Apply and then OK.
</p>
<br />

<p>
<img src="https://i.imgur.com/ogpd39P.png" height="80%" width="80%" alt="osTicket Installation"/>
</p>
<p>
Go back to the osTicket site and click Continue at the bottom of the page. Fill out your information in the fields. Open up the credential text file from earlier on your computer and use it to fill out the Admin User username and password.
</p>
<br />

<p>
<img src="https://i.imgur.com/ymNwr28.png" height="80%" width="80%" alt="osTicket Installation"/>
</p>
<p>
Before filling out the Database Settings, you have to install HeidiSQL.
</p>
<br />

<p>
<img src="https://i.imgur.com/oasU3Wq.png" height="80%" width="80%" alt="osTicket Installation"/>
</p>
<p>
Go to the osTicket-Installation-Files folder to install it.
</p>
<br />

<p>
<img src="https://i.imgur.com/imPa3qo.png" height="80%" width="80%" alt="osTicket Installation"/>
</p>
<p>
To create a new session, click New at the bottom left corner. For username and password, type root and click Open.
</p>
<br />

<p>
<img src="https://i.imgur.com/mUAc48R.png" height="80%" width="80%" alt="osTicket Installation"/>
</p>
<p>
Now you have to create a database. To do this, right-click Unnamed, go to Create new and select Database. Name it osTicket and click OK.
</p>
<br />

<p>
<img src="https://i.imgur.com/wDdoJzF.png" height="80%" width="80%" alt="osTicket Installation"/>
</p>
<p>
Go back to osTicket site, fill out the SQL Database, Username, & Password, and click Install Now.
</p>
<br />

<p>
<img src="https://i.imgur.com/t59YztA.png" height="80%" width="80%" alt="osTicket Installation"/>
</p>
<p>
Now that you've finished installing osTicket, bookmark your osTicket URL for the help desk login page and http://localhost/osTicket/ for End Users.
</p>
<br />
