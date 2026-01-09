<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1> osTicket Post-Installation Configuration Guide </h1> 

This guide walks through the post-install setup and configuration of osTicket, an open-source support ticketing platform.

---

<h2> Environments and Technologies Used </h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

---

## Operating Systems Used

- Windows 10 (21H2)

---

## Post-Install Configuration Objectives

- Configure `Roles`
- Configure `Departments`
- Configure `Teams`
- Configure `Agents`
- Configure `Users`
- Configure `SLA`
- Configure `Help Topics`

---

## Accessing osTicket

### 🔐 Admin / Agent Login

Use the following URL to access the **Admin and Agent Control Panel**:

`http://localhost/osTicket/scp/login.php`

This portal is used by administrators and help desk agents to manage tickets and system settings.

---

### 👤 End User Portal

End users (customers) submit tickets using this URL: `http://localhost/osTicket`

---

## Admin Panel vs Agent Panel

osTicket separates configuration and daily ticket work into two panels.

### 🛠 Admin Panel

Used for **system-wide configuration**, including:

* Roles and permissions
* Departments and teams
* SLA plans
* Help topics
* Agent configuration

### 🎧 Agent Panel

Used for **day-to-day operations**, including:

* Managing tickets
* Responding to users
* Creating and editing user accounts

Understanding this separation is essential for proper security and workflow management.

---

## Configuring Roles

Roles define **what actions agents are allowed to perform** within osTicket.

### Steps

1. Log in to the **Admin Panel**
2. Navigate to:

   **Agents → Roles**
3. Create a new role
   
<img width="468" height="293" alt="image" src="https://github.com/user-attachments/assets/57d42bf7-49e7-4458-83f7-401fc43b59b5" />

### Example Role

* **Role Name:** Supreme Admin
* **Purpose:** Full system access and permissions. Select all **Tickets, Tasks,** and **Knowledgebase** boxes. So the new Role we are creating will have all the Permissions 

<img width="315" height="208" alt="image" src="https://github.com/user-attachments/assets/ea6f1957-e832-4299-aa5a-4dd038179b82" />

<img width="329" height="149" alt="image" src="https://github.com/user-attachments/assets/36a14cb0-f610-47d3-bfbe-7c187439eed3" />

---

## Configuring Departments

Departments control **ticket visibility, routing, and responsibility**.

### Steps

1. Log in to the **Admin Panel**
2. Navigate to:

   **Agents → Departments**
3. Create departments based on organizational needs

### Example Department

* **SysAdmins** – Handles system, server, and infrastructure-related issues

---

## Configuring Teams

Teams allow agents from **multiple departments** to collaborate on tickets.

### Steps

1. Log in to the **Admin Panel**
2. Navigate to:

   **Agents → Teams**
3. Create a team and assign agents from different departments

### Example Team

* **Online Banking** – Includes agents from Support, Networking, and SysAdmins

---

## User Registration Settings

By default, osTicket allows unregistered users to create tickets. For secure or enterprise environments, registration should be required.

### Steps

1. Log in to the **Admin Panel**
2. Navigate to:

   **Settings → User Settings**
3. Update the following options:

* ❌ Disable **Unregistered users can create tickets**
* ✅ Enable **Require registration and login to create tickets**

---

## Configuring Agents

Agents are **help desk staff members** who work on tickets.

### Steps

1. Log in to the **Admin Panel**
2. Navigate to:

   **Agents → Add New**
3. Create agent accounts and assign departments

### Example Agents

* **Jane** – Department: SysAdmins
* **John** – Department: Support

---

## Configuring Users (End Customers)

Users are the **customers** who submit support tickets.

### Steps

1. Log in to the **Agent Panel**
2. Navigate to:

   **Users → Add New**
3. Create user accounts

### Example Users

* Karen
* Ken

---

## Configuring SLA Plans

SLA (Service Level Agreement) plans define **expected response and resolution times**.

### Steps

1. Log in to the **Admin Panel**
2. Navigate to:

   **Manage → SLA**
3. Create SLA plans based on severity

### Example SLA Plans

| SLA Name | Grace Period | Schedule       |
| -------- | ------------ | -------------- |
| Sev-A    | 1 Hour       | 24/7           |
| Sev-B    | 4 Hours      | 24/7           |
| Sev-C    | 8 Hours      | Business Hours |

---

## Configuring Help Topics

Help Topics guide users when submitting tickets and help route tickets correctly.

### Steps

1. Log in to the **Admin Panel**
2. Navigate to:

   **Manage → Help Topics**
3. Create help topics relevant to your organization

### Example Help Topics

* Business Critical Outage
* Personal Computer Issues
* Equipment Request
* Password Reset
* Other

---

## Recommended Next Steps

After completing this post-install configuration, consider:

* Configuring **email piping** for ticket creation
* Integrating **Active Directory / LDAP authentication**
* Creating **ticket filters and automation rules**
* Enabling **logging, reporting, and auditing**

---

## 📘 Notes

This file is intentionally kept as **one Markdown document** for easier reading on GitHub and simpler maintenance.

You are encouraged to fork, modify, and adapt this guide to match your environment.
