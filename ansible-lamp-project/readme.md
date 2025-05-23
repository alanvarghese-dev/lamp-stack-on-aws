# 🚀 Automated LAMP Stack Deployment Using Ansible on AWS EC2

This project demonstrates a fully automated deployment of the "LAMP Stack (Linux, Apache, MySQL, PHP)" on an "AWS EC2 instance" using "Ansible". Designed for beginners transitioning into DevOps or Cloud Infrastructure roles, this project emphasizes hands-on configuration, automation, and real-world troubleshooting experience.

---

## 📌 Table of Contents

- Project Overview
- Tools & Technologies Used
- Architecture
- Step-by-Step Workflow
- Troubleshooting & Solutions
- Screenshots
- What I Learned 
- About Me

---

## 📂 Project Overview

This project automates the provisioning and configuration of a web server running on Ubuntu using Ansible. It installs and configures:

- Apache (Web Server)
- MySQL (Database Server)
- PHP (Server-side Scripting Language)

All of this is done **without manual installation**, making it repeatable, scalable, and ideal for real-world DevOps practices.

---

## 🧰 Tools & Technologies Used

- **Amazon Web Services (AWS)** – EC2 (Ubuntu 22.04)
- **Ansible** – Configuration Management Tool
- **Linux (Ubuntu)** – Base Operating System
- **Apache** – Web Server
- **MySQL** – Database
- **PHP** – Backend Scripting
- **Git & GitHub** – Version Control & Portfolio Hosting
- **macOS Terminal** – Ansible Control Node

---

## 🏗️ Architecture


+--------------------+ SSH +---------------------------+

| Ansible Control | ------------------> | AWS EC2 Ubuntu Instance |


| Node (Mac) | | (LAMP Stack Installed) |

+--------------------+ +---------------------------+

|
| Inventory & YAML Playbook
|
↓

Automated LAMP Setup


---

## ✅ Step-by-Step Workflow

1. Created EC2 Ubuntu instance & configured SSH access
2. Installed Ansible on macOS
3. Created an Ansible inventory file
4. Wrote an Ansible playbook (`lamp.yaml`) to:
   - Update system
   - Install Apache
   - Install PHP and dependencies
   - Install MySQL
5. Ran playbook using:
   - zsh
   - ansible-playbook -i inventory lamp.yaml
6. Verified Apache, PHP, and MySQL were installed successfully
7. Created a phpinfo() page to test PHP integration
8. Tested MySQL login and configuration
9. Uploaded project and documentation to GitHub

---

##🧯 Troubleshooting & Solutions

| Issue                                   | Diagnosis                    | Solution                                                   |
| ----------------------------------- | ---------------------------- | ---------------------------------------------------------- |
| EC2 instance unreachable            | Ansible showed `UNREACHABLE` | Fixed SSH key permission and verified `lamp-key.pem` path  |
| Operation timed out                 | Manual SSH failed            | Added inbound rules for port 22 in AWS Security Group      |
| `sudo mysql` failed with ERROR 2002 | MySQL service not running    | Reinstalled MySQL after purging and removed broken configs |
| Ansible skipped tasks               | Incorrect inventory path     | Fixed path and ensured host was defined properly           |
| Playbook syntax error               | YAML indentation issue       | Fixed spacing and used online YAML validators              |
| Git authentication failed           | Token not accepted           | Switched to GitHub Desktop for easier repo syncing         |


---

## 🖼 Screenshots

All screenshots are stored in the /screenshots/ directory, including:

 - EC2 Launch

 - SSH Access

 - Ansible Playbook Execution

 - Apache Welcome Page

 -PHP Info Page

 -MySQL Login and Secure Install


---

## 🧠 What-I-Learned

 
 - How to launch and SSH into AWS EC2 instances

 - How to write and debug Ansible playbooks

 - How to configure LAMP stack from scratch via automation

 - Troubleshooting broken installs (MySQL, SSH, etc.)

 - Real-world GitHub documentation & version control

 - Cloud-based deployment and beginner DevOps principles


---

## 👨‍💻 About Me...

I’m currently pursuing a Postgraduate Diploma in Infrastructure Management. My studies cover topics aligned with RHCSA, MCSA, CCNA, CompTIA A+, Network+, Security+, and AWS Solutions Architect Associate. I'm building strong foundational projects to transition into DevOps, Cloud Engineering, or Cybersecurity roles.

I'm actively seeking entry-level opportunities related to:

 - DevOps / Site Reliability Engineering (SRE)

 - Cloud System Administration

 - IT Infrastructure

 - Network or Security Operations

---

## 🔗 Portfolio

This is Project #1 of my hands-on DevOps & Cloud projects.

📁 GitHub Repository: https://github.com/alanvarghese-dev/lamp-stack-on-aws

   LinkedIn: www.linkedin.com/in/alan-varghese-dev/
