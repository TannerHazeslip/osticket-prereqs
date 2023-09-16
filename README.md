# osticket-prereqs
<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>




<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- PHP Manager for IIS
- Rewrite module
- PHP 7.3.8
- VC_redist.x86.exe
- MySQL 5.5.61
-  HeidiSQL

<h2>Installation Steps</h2>
First we will need to install IIS

Turn on the CGI and all non checked common HTTP windows features by following this path

Windows -> programs-> -> Turn windows features on or off ->  internet information services -> world wide web services -> application Development Features -> CGI

<img src="https://cdn.discordapp.com/attachments/1149514851564138576/1149515697186164796/Capture.PNG" height="50%" width="50%" alt="Disk Sanitization Steps"/>

Windows -> programs-> -> Turn windows features on or off ->  internet information services -> world wide web services -> common HTTP Features (Then check any box that isnt checked)

<img src="https://cdn.discordapp.com/attachments/1149514851564138576/1149526900268617808/Capture.PNG" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<p>

</p>
<br />
Download and install PHP manager for IIS and Rewrite module
<p>
<img src="https://cdn.discordapp.com/attachments/1149514851564138576/1151589069353128067/Capture.PNG" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
Create a folder named PHP then download PHP 7.3.8 and extract the files to the PHP folder
<p>
<img src="https://cdn.discordapp.com/attachments/1149514851564138576/1151590493302554746/Capture.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />
Download and install VC_redlistx86.exe
<p>
<img src="https://cdn.discordapp.com/attachments/1149514851564138576/1151591147077115914/Capture.PNG" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
Download and install MySQL-5.5.62-win32.msi and create a password
<p>
  <img src="https://cdn.discordapp.com/attachments/1149514851564138576/1151592028283617331/Capture.PNG" height="50%" width="50%" alt="Disk Sanitization Steps"/>
  <img src="https://cdn.discordapp.com/attachments/1149514851564138576/1151592300389081118/Capture.PNG" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
</p>
Open IIS as an admin
<img src="https://cdn.discordapp.com/attachments/1149514851564138576/1152349547599769640/Capture.PNG" height="50%" width="50%" alt="Disk Sanitization Steps"/>
Register PHP from within IIS
<img src="https://cdn.discordapp.com/attachments/1149514851564138576/1152350154947567688/Capture.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://cdn.discordapp.com/attachments/1149514851564138576/1152350389526605834/Capture.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
Browse to the php-cgi folder
<img src="https://cdn.discordapp.com/attachments/1149514851564138576/1152351265712525402/Capture.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
Download osTicket V1.15.8 and extract the "Upload" folder to c:\inetpub\wwwroot
<img src="https://cdn.discordapp.com/attachments/1149514851564138576/1152352854200291499/Capture.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
Rename the "upload" folder to "osTicket
<img src="https://cdn.discordapp.com/attachments/1149514851564138576/1152353317104656425/Capture.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
Within osTicket go to Sites -> Default -> osTicket and click on brows*:80
<img src="https://cdn.discordapp.com/attachments/1149514851564138576/1152353963241386006/Capture.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://cdn.discordapp.com/attachments/1149514851564138576/1152354379425382451/Capture.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
Go back to IIS: Sites-> Default -> osTicket and open PHP manager
<img src="https://cdn.discordapp.com/attachments/1149514851564138576/1152355304063905822/Capture.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
Click on enable or disable an extension
<img src="https://cdn.discordapp.com/attachments/1149514851564138576/1152355583672975452/Capture.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
Enable "php_imap.dll", "php_intl.dll", and "php_opcache.dll"
<img src="https://cdn.discordapp.com/attachments/1149514851564138576/1152355583672975452/Capture.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
Refresh osTicket in your browser and it should look like this
<img src="https://cdn.discordapp.com/attachments/1149514851564138576/1152356723554783362/Capture.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
From C:\inetpub\wwwroot\osTicket\include rename ost-sampleconfig to ostconfig
<img src="https://cdn.discordapp.com/attachments/1149514851564138576/1152357916620378133/Capture.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
Assign permissions to ost-config.php
</p>
Disable Inheritance
<img src="https://cdn.discordapp.com/attachments/1149514851564138576/1152358801941463040/Capture.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://cdn.discordapp.com/attachments/1149514851564138576/1152359024352829520/Capture.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://cdn.discordapp.com/attachments/1149514851564138576/1152359413533909022/Capture.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://cdn.discordapp.com/attachments/1149514851564138576/1152359655109046313/Capture.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
Then click on add permissions
<img src="https://cdn.discordapp.com/attachments/1149514851564138576/1152360152104706151/Capture.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
Type in "everyone" and then hit check names
<img src="https://cdn.discordapp.com/attachments/1149514851564138576/1152360696135299132/Capture.PNG" height="50%" width="50%" alt="Disk Sanitization Steps"/>
Give everyone(for now) full control
<img src="https://cdn.discordapp.com/attachments/1149514851564138576/1152360989770121306/Capture.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
Continue setting up osTicket in the browser
<img src="https://cdn.discordapp.com/attachments/1149514851564138576/1152361498832801923/Capture.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
Name the helpdesk and assign an admin user(dont forget)
<img src="https://cdn.discordapp.com/attachments/1149514851564138576/1152361798620680213/Capture.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
Install and laucnh HeidiSQLServer
</p>
Create a new connecteion
<img src="https://cdn.discordapp.com/attachments/1149514851564138576/1152362820986470560/Capture.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
Use the password you created when setting up MySQL server
<img src="https://cdn.discordapp.com/attachments/1149514851564138576/1152363189355413545/Capture.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
Create a new database in HeidiSQL named osTicket
<img src="https://cdn.discordapp.com/attachments/1149514851564138576/1152365344892129352/Capture.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://cdn.discordapp.com/attachments/1149514851564138576/1152365526983643227/Capture.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
Enter the MySQL information into the browser and hit the install button
<img src="https://cdn.discordapp.com/attachments/1149514851564138576/1152366004840714261/Capture.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
Delete the C:\inet\wwwroot\osTicket\Setup folder
<img src="https://cdn.discordapp.com/attachments/1149514851564138576/1152367075713634304/Capture.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
Set the permissions of C:\inetpub\osTicket\ost-config.php to "Read" only
<img src="https://cdn.discordapp.com/attachments/1149514851564138576/1152367366286610493/Capture.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://cdn.discordapp.com/attachments/1149514851564138576/1152367592141500506/Capture.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://cdn.discordapp.com/attachments/1149514851564138576/1152657658982178956/Capture.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://cdn.discordapp.com/attachments/1149514851564138576/1152657789135618221/Capture.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
Browse to the help desk login at http://localhost/osTicket/scp/login.php or to the end user osTicket URL at http://localhost/osTicket/ 
</p>
<br />
