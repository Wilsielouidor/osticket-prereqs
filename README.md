<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket. Disclaimer steps will be completed using a Macbook which will show differently compared to a windows desktop. <br />



<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Computer)
- Remote Desktop 
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Virtual Machine using Azure
- Internet Information Services (IIS)  
- Install the os Ticket prerequirements access through link:
- <p>https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6
- <p>  PHP Manager
- <p>  Rewrite Module
- <p>  PHP 7.3.8
- <p>  VC Redist.x86.exe
- <p>  MySQL5.5.62
- <p>  HeidiSQL
- <p> osTicket v1.15.8

<h2>Extra Resource</h2>
<ul>
 <li>How to create a <a href="https://learn.microsoft.com/en-us/azure/virtual-machines/windows/quick-create-portal" target="_blank">Virtual Machine</a> and connect through Azure portal </li>
</ul>
<h2>Sign into Azure</h2>
<ul>
 <li>Sign into the <a href= "https://portal.azure.com" target="_blank">Azure portal</a> </li>
</ul>

<h1> Create Virtual Machine</h1>
<ul>
 <li> Create Resource group</li>
</ul>
<p></p>

<img width="80%" alt="Screen Shot 2023-09-20 at 4 28 49 PM" src="https://github.com/Wilsielouidor/osticket-prereqs/assets/142513380/a6790aaf-1d64-43a6-9521-896881c4492d">
<p></p>

<h2> Instance Details</h2>
<ul> 
 <li>Under Instance details: create a Virtual Machine name</li>
 <li>For image use Windows 10 Pro</li> 
 <li>Size: use 2 or 4vcpus, 16 Gib of memory</li>
</ul>

 <p><img width="80%" alt="Screen Shot 2023-09-20 at 4 35 41 PM" src="https://github.com/Wilsielouidor/osticket-prereqs/assets/142513380/93e55d07-0bc9-46d5-ac50-a89f48fd60a1"></p>

 <h2> Administrator Account</h2>
<ul>
 <li>Under Administrator account provide username and password to use for later when connecting to the Virtual Machine.</li>
 <li>Leave the remaining defaults</li>
 <li>check box under licensing and click review and create </li>
</ul>
<p>
 
<img width="80%" alt="Screen Shot 2023-09-20 at 4 38 42 PM" src="https://github.com/Wilsielouidor/osticket-prereqs/assets/142513380/aaa877bd-af21-40d2-a99e-fe6a2a7a15de">

<h1> Install Dependencies and osTicket</h1>
<p>
 <h2> Login to Virtual Machine</h2>
<ul>
 <li>Use Remote Desktop to connect to Virtual Machine</li>
 <ul> 
  <li>Note: if you are using mac you would need to download microsoft remote desktop from your app store </li>
  <li><img width="40%" alt="Screen Shot 2023-10-06 at 8 36 45 AM" src="https://github.com/Wilsielouidor/osticket-prereqs/assets/142513380/9715324a-2996-41ad-bd1f-96fd614a6726">

</li>
 </ul>
 <li>Copy and paste public IP address that was just created onto Remote desktop</li>
 <li>use login credentials that were created under azure virtual machine</li>
</ul>
<p>
<img width="80%" alt="Screen Shot 2023-09-20 at 6 48 07 PM" src="https://github.com/Wilsielouidor/osticket-prereqs/assets/142513380/a98a0374-8762-45da-9e9b-aac96c3f1784">
</p>
</ b>
<p>
<img width="60%" alt="Screen Shot 2023-09-20 at 6 50 58 PM" src="https://github.com/Wilsielouidor/osticket-prereqs/assets/142513380/e1ad5f0c-3a7b-4203-b25d-1a18fb370843"> 
</b>
</p>


<img width="60%" alt="Screen Shot 2023-09-20 at 6 53 02 PM" src="https://github.com/Wilsielouidor/osticket-prereqs/assets/142513380/48506a06-c685-4788-857a-220e4b8020ca">



<h2>Install IIS</h2>  
Note: Open <a href="https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6" target="_blank">Installation Files</a> on microsoft edge web browser as needed
 <ul>
  <li>Open Install IIS in with CGI and Common HTTP Features by going to control panel</li>
  <li>Click Programs</li>
   <li>Turn windows features on and off</li>
  <li>Check box of Internet Information Services</li> 
  <li>Expand world wide web services by pressing the plus sign next to it</li> 
  <li>Expand application Development Features check CGI </li>
 </ul>
<img width="60%" alt="Screen Shot 2023-09-20 at 11 37 00 PM" src="https://github.com/Wilsielouidor/osticket-prereqs/assets/142513380/708d3403-d9a8-44a9-8216-9abbfb21622d">



<p>
 <h4>Collapse Application Development--> Expand Common HTTP Features and make sure all features are checked and then click OK.</h4>
</p>

</b> 
<img width="60%" alt="Screen Shot 2023-09-20 at 11 43 21 PM" src="https://github.com/Wilsielouidor/osticket-prereqs/assets/142513380/896e2af9-1e47-4b7a-a6b7-9e87d5e59463">


<p><h4>After IIS is installed, make sure it works by going to the web browser and type in 127.0.0.1 as it shows in the image below.</h4>
 <ul>
  <li>Note: 127.0.0.1 (a universal home address for all computers) is a loopback address that is used to load a webpage on the same webpage being used. Such as testing to see if the IIS is working effectively, once osTicket is downloaded the osTicket would run efficiently.</li>
 </ul>
</p>
<img width="60%" alt="Screen Shot 2023-09-20 at 11 48 10 PM" src="https://github.com/Wilsielouidor/osticket-prereqs/assets/142513380/e643c53a-1aac-41b5-8676-6d1b5d086007">

</p>
<br />
<h2> Download Files</h2> 
<ul> 
<li>From <a href="https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6" target="_blank">Installation Files</a> </li>
<li>Download PHP Manager--> download rewrite </li>
 </ul>
 </p>
<img width="60%" alt="Screen Shot 2023-09-21 at 12 01 24 AM" src="https://github.com/Wilsielouidor/osticket-prereqs/assets/142513380/68b5931b-2b60-45fd-b03d-f00b6adabc0e">

<img width="60%" alt="Screen Shot 2023-09-21 at 12 06 16 AM" src="https://github.com/Wilsielouidor/osticket-prereqs/assets/142513380/fd90e8e0-1b52-457c-8d3c-a6190cf51a8d">

<p> <h2>Create Directory C:\PHP </h2>
 <ul>
  <li>Create a folder by clicking the folder icon on the bottom</li>
  <li> Click this PC->Windows C</li>
  <li>Create new folder by right clicking where there is an open space</li>
  <li> Go down to new and then folder</li>
  <li> Name the folder PHP</li>
 </ul>
<img width="80%" alt="Screen Shot 2023-09-21 at 12 11 55 AM" src="https://github.com/Wilsielouidor/osticket-prereqs/assets/142513380/4f399163-bd09-43f3-83db-eb53c0e0a151">
</p>


<p> <img width="80%" alt="Screen Shot 2023-09-21 at 12 13 39 AM" src="https://github.com/Wilsielouidor/osticket-prereqs/assets/142513380/c258d785-4cce-4aa6-9ef2-a67d3f7e2687"> </p>
<br />

<p> <img width="80%" alt="Screen Shot 2023-09-21 at 12 15 19 AM" src="https://github.com/Wilsielouidor/osticket-prereqs/assets/142513380/c66f0513-8f5b-48c1-8f28-540803a2034b"> </p>
<br />


<h2>From <a href="https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6" target="_blank">Installation Files</a></h2>
 <ul>
 <li>Download PHP 7.3.8 file</li>
  <li>Extract PHP 7.3.8 files from download folder into PHP folder by right clicking the file from recently downloaded files</li>
 </ul>

<p><img width="60%" alt="Screen Shot 2023-09-25 at 12 12 47 PM" src="https://github.com/Wilsielouidor/osticket-prereqs/assets/142513380/1403a330-03db-473b-a60f-09868f441785"> </p>

 <p> <img width="60%" alt="Screen Shot 2023-09-25 at 12 14 03 PM" src="https://github.com/Wilsielouidor/osticket-prereqs/assets/142513380/5fb5776d-147a-4e77-ad9b-f5ec217396a2"> </p>

 <p><img width="60%" alt="Screen Shot 2023-09-25 at 12 17 17 PM" src="https://github.com/Wilsielouidor/osticket-prereqs/assets/142513380/ed5c7260-b258-4587-accf-2d46dbbd0c55"> 


</p>
<br />


<h2> From <a href="https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6" target="_blank">Installation Files</a> download and install VC_redist.x86.exe. </h2>

<p> 
 <img width="60%" alt="Screen Shot 2023-09-25 at 12 30 26 PM" src="https://github.com/Wilsielouidor/osticket-prereqs/assets/142513380/e7945b28-0db2-4243-9d06-ca16cd74d94b">
</p>
<br />

<ul>
<h2>From <a href="https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6" target="_blank">Installation Files</a>, download and install MySQL 5.5.62 </h2>
 <li>Typical Setup</li>
 <li>Launch configuration Wizard (after install)</li>
 <li>Standard Configuration</li>
 <li>Password1</li>
 <li>Execute</li>
</ul>

<p>
<img width="60%" alt="Screen Shot 2023-09-25 at 12 56 15 PM" src="https://github.com/Wilsielouidor/osticket-prereqs/assets/142513380/eccf074e-3fa2-4c20-8bc7-f336dd94f364">

 
<img width="60%" alt="Screen Shot 2023-09-25 at 1 04 42 PM" src="https://github.com/Wilsielouidor/osticket-prereqs/assets/142513380/5d138853-05f2-4310-b16c-e3bfaa46fc30">

</p>

<h2>Complete Configuration within IIS</h2>
<p>
<ul>
 <li> Type in IIS next to the bottom of the start button</li>
 <li>Click Run as Admin</li>
 <li>Register PHP from within IIS</li>
 <ul>
 <li>Click PHP manger--> Register new PHP version--> Click browse button (which are the 3 dots)--> Find file C:\PHP\php-cgi.cxe--> Then click OK</li>
 </ul>
 <li>Reload IIS (Open IIS, restart server</li>
</p> 
 <p>
  <img width="60%" alt="Screen Shot 2023-09-25 at 1 17 39 PM" src="https://github.com/Wilsielouidor/osticket-prereqs/assets/142513380/59554d0d-68eb-42fa-b4ec-6515e49b5bdb">

 </p>
</ul>

<p>
  <img width="60%" alt="Screen Shot 2023-09-25 at 1 17 39 PM" src="https://github.com/Wilsielouidor/osticket-prereqs/assets/142513380/59554d0d-68eb-42fa-b4ec-6515e49b5bdb">

 </p> 
 </ul>

<ul>
 <p>
  <img width="80%" alt="Screen Shot 2023-09-25 at 1 33 54 PM" src="https://github.com/Wilsielouidor/osticket-prereqs/assets/142513380/d70bb34b-bd43-4d52-b762-baac18ecd611">

<img width="80%" alt="Screen Shot 2023-09-25 at 1 47 02 PM" src="https://github.com/Wilsielouidor/osticket-prereqs/assets/142513380/1bbfd0b8-45b0-45f3-bc2a-3be19f4ac562">

<img width="80%" alt="Screen Shot 2023-09-25 at 1 58 51 PM" src="https://github.com/Wilsielouidor/osticket-prereqs/assets/142513380/5fa25b54-d1da-4dd8-8835-97afda36b79e">

 </p>
</ul>



<h2>Install osTicket v1.15.8</h2>
<ul>
<li>Download osTicket from <a href="https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6" target="_blank">Installation Files</a> Folder</li>
<li>Extract and copy “upload” folder to c:\inetpub\wwwroot</li>
<li>Within c:\inetpub\wwwroot, Rename “upload” to “osTicket” (Make sure you rename it exactly as you see it)</li>
 
</ul>

<img width="80%" alt="Screen Shot 2023-09-25 at 2 12 44 PM" src="https://github.com/Wilsielouidor/osticket-prereqs/assets/142513380/c789e54c-63bf-4ff9-9014-2a54e4a67269">

<img width="80%" alt="Screen Shot 2023-09-25 at 2 11 18 PM" src="https://github.com/Wilsielouidor/osticket-prereqs/assets/142513380/a00512c1-a97f-4fa4-938d-ca9f0e210fff">


Reload IIS (Open IIS, Stop and Start the server)

Go to sites -> Default -> osTicket
On the right, click “Browse *:80”

<img width="80%" alt="Screen Shot 2023-09-25 at 2 20 51 PM" src="https://github.com/Wilsielouidor/osticket-prereqs/assets/142513380/c3fc242e-51c2-4a74-bbd3-f17b7c759f72">

<img width="80%" alt="Screen Shot 2023-09-25 at 2 21 58 PM" src="https://github.com/Wilsielouidor/osticket-prereqs/assets/142513380/a10a3901-4063-4179-b725-e92ff43d58e0">

<h2>Enable Extension to allow osTicket to run Smoothly</h2>
Note that some extensions are not enabled
<ul>
<li>Go back to IIS, sites -> Default -> osTicket</li>
<li>Double-click PHP Manager</li>
<li>Click “Enable or disable an extension”</li>
 <ul>
<li>Enable: php_imap.dll</li>
<li>Enable: php_intl.dll</li>
<li>Enable: php_opcache.dll</li>
 </ul>
 <li>Refresh the osTicket site in your browse, observe the changes</li>
</ul>


<img width="80%" alt="Screen Shot 2023-09-25 at 2 26 17 PM" src="https://github.com/Wilsielouidor/osticket-prereqs/assets/142513380/89153f62-1f7b-4233-b36b-b282428f8f0f">

<img width="80%" alt="Screen Shot 2023-09-25 at 2 27 45 PM" src="https://github.com/Wilsielouidor/osticket-prereqs/assets/142513380/95ff6aa9-099e-4b86-a261-f68a38680b02">

<h2>After extensions have been enabled </h2>

<img width="80%" alt="Screen Shot 2023-09-25 at 2 32 39 PM" src="https://github.com/Wilsielouidor/osticket-prereqs/assets/142513380/2da29e14-510c-455c-a5da-4e93e44665f8">


<h3>Rename: ost-sampleconfig.php</h3>
<ul>
<li>From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php</li>
<li>To: C:\inetpub\wwwroot\osTicket\include\ost-config.php</li>

<img width="80%" alt="Screen Shot 2023-09-25 at 2 36 21 PM" src="https://github.com/Wilsielouidor/osticket-prereqs/assets/142513380/d2373cbe-a1f2-4ad2-aa04-7d1114547dc9">

<img width="80%" alt="Screen Shot 2023-09-25 at 2 38 23 PM" src="https://github.com/Wilsielouidor/osticket-prereqs/assets/142513380/d137453c-edf8-4267-b1e3-d773d65aba8c">


<li>Assign Permissions: ost-config.php</li>
<li>Disable inheritance -> Remove All</li>
   <li>Right click on ost-config--> properties--> security tab--> advanced--> disable inheritance--> Remove all inheritance 
New Permissions -> Everyone -> All</li>
    <li>Click add--> Select a prinicple--> type in "everyone"--> check names--> check full control--> apply and click OK</li>
</ul>
<p>
<img width="80%" alt="Screen Shot 2023-09-25 at 2 44 23 PM" src="https://github.com/Wilsielouidor/osticket-prereqs/assets/142513380/72ff287b-ad98-4b1c-9402-7419f32184c4">
</p>
<p>
<img width="80%" alt="Screen Shot 2023-09-25 at 2 47 18 PM" src="https://github.com/Wilsielouidor/osticket-prereqs/assets/142513380/114a9bb7-597d-465a-8e90-ba785519b1be">
</p>
<p>
<img width="80%" alt="Screen Shot 2023-09-25 at 2 50 33 PM" src="https://github.com/Wilsielouidor/osticket-prereqs/assets/142513380/4e34b9f4-13f8-4e02-9a36-08cb4375b810">
</p>



Continue Setting up osTicket in the browser (click Continue)
Name Helpdesk
Default email (receives email from customers)

<img width="80%" alt="Screen Shot 2023-09-25 at 2 58 04 PM" src="https://github.com/Wilsielouidor/osticket-prereqs/assets/142513380/d32146b7-9d68-4b2c-b6cd-abffe08d04aa">


<h2>From the <a href="https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6" target="_blank">Installation Files</a>, download and install HeidiSQL.</h2>

<img width="80%" alt="Screen Shot 2023-09-25 at 3 00 50 PM" src="https://github.com/Wilsielouidor/osticket-prereqs/assets/142513380/bc737bb5-0f16-4bd3-beb8-19332fa2f154">
<ul>
<li>Open Heidi SQL</li>
<li>Create a new session, root/Password1</li>
<li>Connect to the session</li>
<li>Create a database called “osTicket”</li>
 Note: Make sure it is typed in exactly how it was typed when renaming the upload folder previously.
   <li>right click unamed--> create new--> database--> name "osTicket" (exactly the way you see it)--> click OK</li>
</ul>

<img width="80%" alt="Screen Shot 2023-09-25 at 3 04 59 PM" src="https://github.com/Wilsielouidor/osticket-prereqs/assets/142513380/3a687088-7a3d-462e-bf8d-90a059ec3ce0">

<img width="80%" alt="Screen Shot 2023-09-25 at 3 13 53 PM" src="https://github.com/Wilsielouidor/osticket-prereqs/assets/142513380/c2e8a3a1-a2ce-46d1-9d5b-048a64156805">


<img width="80%" alt="Screen Shot 2023-09-25 at 3 16 59 PM" src="https://github.com/Wilsielouidor/osticket-prereqs/assets/142513380/7f700d51-6e74-4243-99db-eb390816960e">


<h2>Continue Setting up osticket in the browser</h2>
<ul>
<li>MySQL Database: osTicket</li>
<li>MySQL Username: root</li>
<li>MySQL Password: Password1</li>
<li>Click “Install Now!”</li>
</ul>
<img width="80%" alt="Screen Shot 2023-09-25 at 3 19 16 PM" src="https://github.com/Wilsielouidor/osticket-prereqs/assets/142513380/e6f4513c-16bb-4560-8a5f-d0b1698541c0">

<img width="80%" alt="Screen Shot 2023-09-25 at 3 21 58 PM" src="https://github.com/Wilsielouidor/osticket-prereqs/assets/142513380/69c2ae06-22d1-487f-b01e-511055279f6c">


<h2>Clean up</h2>
<p>
<ul>
<li>Delete: C:\inetpub\wwwroot\osTicket\setup</li>
</p>
<img width="80%" alt="Screen Shot 2023-09-25 at 3 23 28 PM" src="https://github.com/Wilsielouidor/osticket-prereqs/assets/142513380/19ccc315-8a4c-4df8-bc8b-930e1031585e">

<li>Set Permissions to “Read” only: C:\inetpub\wwwroot\osTicket\include\ost-config.php</li>
</ul>
<img width="80%" alt="Screen Shot 2023-09-25 at 3 27 19 PM" src="https://github.com/Wilsielouidor/osticket-prereqs/assets/142513380/7ebe33ae-7407-43f9-8792-13968493b95e">



<h2>Congratulations, hopefully it is installed with no errors!</h2>
<ul>
<li>Browse to your help desk login page: http://localhost/osTicket/scp/login.php</li>
</ul>

<img width="80%" alt="Screen Shot 2023-09-25 at 3 31 42 PM" src="https://github.com/Wilsielouidor/osticket-prereqs/assets/142513380/33a046bf-8e43-4a3c-af37-51343a67ebb3">

<img width="80%" alt="Screen Shot 2023-09-25 at 3 33 16 PM" src="https://github.com/Wilsielouidor/osticket-prereqs/assets/142513380/5174c9f5-2121-4681-b3f9-81eea09290f1">


