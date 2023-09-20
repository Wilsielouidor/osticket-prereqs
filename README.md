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



  
2) Install/Enable IIS in with CGI and Common HTTP Features 
</p>
<br />

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
