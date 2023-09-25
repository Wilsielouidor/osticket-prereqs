<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket. Disclaimer steps will be completed using a Macbook which will show differently compared to a windows desktop. <br />


<h2>Video Demonstration</h2>

- ### [YouTube: How To Install osTicket with Prerequisites](https://www.youtube.com)

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

<h1>Sign into Azure</h1>
Sign into the <a href= "https://portal.azure.com" target="_blank">Azure portal</a>

<h1> Create Virtual Machine</h1>
1) Create Resource group-->for image use Windows 10 with 2 or 4 virtual CPUs
<p></p>

<img width="852" alt="Screen Shot 2023-09-20 at 4 28 49 PM" src="https://github.com/Wilsielouidor/osticket-prereqs/assets/142513380/a6790aaf-1d64-43a6-9521-896881c4492d">
<p></p>

2) Under Instance details: create a Virtual Machine name--> For image use Windows 10 Pro--> Size use 2 or 4vcpus, 16 Gib of memory
<img width="789" alt="Screen Shot 2023-09-20 at 4 35 41 PM" src="https://github.com/Wilsielouidor/osticket-prereqs/assets/142513380/93e55d07-0bc9-46d5-ac50-a89f48fd60a1">
 <p></p>
 
3) Under Administrator account provide username and password to use for later when connecting to the Virtual Machine.
Leave the remaining defaults--> check box under licensing and click review and create
<p>
 
<img width="782" alt="Screen Shot 2023-09-20 at 4 38 42 PM" src="https://github.com/Wilsielouidor/osticket-prereqs/assets/142513380/aaa877bd-af21-40d2-a99e-fe6a2a7a15de">

<h1> Install Dependencies and osTicket</h1>
<p>
1) Use Remote Desktop to connect to Virtual Machine--> Copy and paste public IP address that was just created onto Remote desktop and use login credentials that were created under azure virtual machines

<img width="1434" alt="Screen Shot 2023-09-20 at 6 48 07 PM" src="https://github.com/Wilsielouidor/osticket-prereqs/assets/142513380/a98a0374-8762-45da-9e9b-aac96c3f1784">  <img width="611" alt="Screen Shot 2023-09-20 at 6 50 58 PM" src="https://github.com/Wilsielouidor/osticket-prereqs/assets/142513380/e1ad5f0c-3a7b-4203-b25d-1a18fb370843"> <img width="611" alt="Screen Shot 2023-09-20 at 6 53 02 PM" src="https://github.com/Wilsielouidor/osticket-prereqs/assets/142513380/48506a06-c685-4788-857a-220e4b8020ca">



  
2) Open <a href="https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6" target="_blank">Installation Files</a> on microsoft edge web browser as needed
 Open Install/Enable IIS in with CGI and Common HTTP Features by going to control panel--> programs--> Turn windows features on and off--> Check box of Internet Information Services--> expand world wide web services by pressing the plus sign next to it--> expand application Development Features check CGI
<img width="416" alt="Screen Shot 2023-09-20 at 11 37 00 PM" src="https://github.com/Wilsielouidor/osticket-prereqs/assets/142513380/708d3403-d9a8-44a9-8216-9abbfb21622d">



Collapse Application Development--> Expand Common HTTP Features and make sure all features are checked and then click OK.
<img width="424" alt="Screen Shot 2023-09-20 at 11 43 21 PM" src="https://github.com/Wilsielouidor/osticket-prereqs/assets/142513380/896e2af9-1e47-4b7a-a6b7-9e87d5e59463">


After IIS is installed, make sure it works by going to the web browser and type in 127.0.0.1 and it shows the image below.
<img width="762" alt="Screen Shot 2023-09-20 at 11 48 10 PM" src="https://github.com/Wilsielouidor/osticket-prereqs/assets/142513380/e643c53a-1aac-41b5-8676-6d1b5d086007">

</p>
<br />
From <a href="https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6" target="_blank">Installation Files</a> download PHP Manager--> download rewrite 

<img width="665" alt="Screen Shot 2023-09-21 at 12 01 24 AM" src="https://github.com/Wilsielouidor/osticket-prereqs/assets/142513380/68b5931b-2b60-45fd-b03d-f00b6adabc0e">

<img width="513" alt="Screen Shot 2023-09-21 at 12 06 16 AM" src="https://github.com/Wilsielouidor/osticket-prereqs/assets/142513380/fd90e8e0-1b52-457c-8d3c-a6190cf51a8d">

<p> Create Directory C:\PHP
<img width="1153" alt="Screen Shot 2023-09-21 at 12 11 55 AM" src="https://github.com/Wilsielouidor/osticket-prereqs/assets/142513380/4f399163-bd09-43f3-83db-eb53c0e0a151">
</p>


<p> <img width="1138" alt="Screen Shot 2023-09-21 at 12 13 39 AM" src="https://github.com/Wilsielouidor/osticket-prereqs/assets/142513380/c258d785-4cce-4aa6-9ef2-a67d3f7e2687"> </p>

<p> <img width="1132" alt="Screen Shot 2023-09-21 at 12 15 19 AM" src="https://github.com/Wilsielouidor/osticket-prereqs/assets/142513380/c66f0513-8f5b-48c1-8f28-540803a2034b"> </p>


From installation files download PHP 7.3.8--> Extract PHP 7.3.8 files into PHP folder 

<head2> From installation files download and install VC_redist.x86.exe. </head2>


<ul>From the installation files, download and install MySQL 5.5.62
<li>Typical Setup</li>
<li>Launch configuration Wizard (after install)</li>
<li>Standard Configuration</li>
<li>Password1</li>
</ul>

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
