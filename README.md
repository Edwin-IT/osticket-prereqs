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

<h2>Overview</h2>

<h2>Part 1: Create Virtual Machine in Azure</h2>

- Step 1: Create a Windows 10 Virtual Machine (VM)

<h2>Part 2: Installation</h2>

- Step 1: In VM1 install and enable IIS
- Step 2: Install Web Platform Installer
- Step 3: Install osTicket v1.15.8
- Step 4: Open IIS and enable extensions
- Step 5: Refresh the osTicket website then Rename and assign permissions to ost-sampleconfig.php
- Step 6: Click “Install Now!” and clean up


<h2>Steps</h2>

<h2>Part 1</h2>

<p>
<img src=".png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src=".png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
- Step 1: Create a Windows 10 Virtual Machine (VM) with 2-4 Virtual CPUs. A resource group and a new Virtual Network (Vnet) will be created in the process.
</p>
<br />

<h2>Part 2</h2>

<p>
<img src=".png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src=".png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
- Step 1: In VM1 install and enable IIS.
 
<p>
<img src=".png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
- Step 2: After installing, Add MySQL 5.5, then add all simple versions of x86 PHP until 7.3. Make sure PHP Version 7.3.8, PHP Manager 1.5.0 for IIS10, and Microsof Visual C++ 2009 are installed.

<p>
<img src=".png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
- Step 3: After installing osTicket, extract and copy the “upload” folder into c:\inetpub\wwwroot, then rename it osTicket.

<p>
<img src=".png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src=".png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src=".png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
- Step 4: Go to sites,  click Default, then osTicket and then click “Browse *:80”.  Go back to osTicket and click PHP Manager. Enable php_imap.dll, php_intl.dll, and php_opcache.dll.

<p>
<img src=".png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
- Step 5: Change C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php to: C:\inetpub\wwwroot\osTicket\include\ost-config.php. Click Disable inheritance, then Remove All, then New Permissions, then Everyone, then All. Click continue on the website.
 
<p>
<img src=".png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src=".png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
- Step 6: After installing, Delete C:\inetpub\wwwroot\osTicket\setup. Then set Permissions to “Read” only in C:\inetpub\wwwroot\osTicket\include\ost-config.php.
</p>
<br />
