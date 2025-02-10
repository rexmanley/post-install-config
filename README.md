# post-install-config<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Post-Install Configuration</h1>
This tutorial outlines the post-install configuration of the open-source help desk ticketing system osTicket.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How To Configure osTicket, post-installation](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>Post-Install Configuration Objectives</h2>

- Admin/analyst login 
- end users osTicket website
- Agent panel
- Admin panel


<h2>Configuration Steps</h2>

![image](https://github.com/user-attachments/assets/ea8bbd26-71c1-40bf-8300-301879f69430)

<p>
Admin/Analyst Login Page:
http://localhost/osTicket/scp/login.php 


End Users osTicket URL:
http://localhost/osTicket 



![image](https://github.com/user-attachments/assets/076a8353-7000-4374-96c7-836aa243e3ea)

Create a role (for grouping permissions)
Admin Panel -> Agents -> Roles
Supreme Admin.
(in the permissons tab check every box and add role)

![image](https://github.com/user-attachments/assets/b8819ed0-32ee-45da-bf2c-457d0677afb8)

Create a new Department (Ticket Visibility, Help Desk vs SysAdmins, vs Networking)
Admin Panel -> Agents -> Departments
SysAdmins 

![image](https://github.com/user-attachments/assets/3e15e23c-42b3-4314-a175-f936e37407b0)

Create a Team
Admin Panel -> Agents -> Teams (Pull Agents from different Departments)
Online Banking

![image](https://github.com/user-attachments/assets/0b93ab3b-525f-4629-bf3c-b1730b5cc107)

Allow anyone to create tickets
Admin Panel -> Settings -> User Settings (UNCHECK: unregistered users can create tickets)
Registration Required: Require registration and login to create tickets

![image](https://github.com/user-attachments/assets/f3c45706-882a-496d-a479-250fcd5b0bc7)

Configure Agents (workers)
Admin Panel -> Agents -> Add New
Jane (Dept: SysAdmins)
John (Dept: Support)

![image](https://github.com/user-attachments/assets/1f7b9441-fc94-45ae-9486-18a46c572ddd)

Configure Users (customers)
Agent Panel -> Users -> Add New
Karen
Ken

![image](https://github.com/user-attachments/assets/81f1c7c9-4943-42ec-9618-a1df3db572bc)

Configure SLA
Admin Panel -> Manage -> SLA
Sev-A (Grace Period: 1 hour, Schedule: 24/7)
Sev-B (Grace Period: 4 hours, Schedule: 24/7)
Sev-C (Grace Period: 8 hours, Business Hours)

![image](https://github.com/user-attachments/assets/dbd9229f-50ba-4fc7-91dc-4ea346d8071e)

Configure Help Topics (For when users create a ticket)
Admin Panel -> Manage -> Help Topics
Business Critical Outage
Personal Computer Issues
Equipment Request
Password Reset
Other

