# 🛠️ AWS EC2 Linux Support Lab

A hands-on AWS + Linux administration project focused on simulating
real-world Cloud / L1 Support Engineer responsibilities.

This project goes beyond simple deployment --- it demonstrates
provisioning, configuration, troubleshooting, and cost awareness in a
live AWS environment.

------------------------------------------------------------------------

## 📦 Technologies

-   AWS EC2
-   Ubuntu Server 22.04 LTS
-   Apache HTTP Server
-   Linux CLI
-   SSH (Key-based Authentication)
-   AWS Security Groups
-   HTML & CSS

------------------------------------------------------------------------

## 🦄 Features

Here's what this lab demonstrates:

-   **EC2 Provisioning**: Launching and configuring a Linux server in
    AWS.
-   **Secure SSH Access**: Connecting using RSA key-pair authentication.
-   **Linux Administration**: Managing users, permissions, and system
    updates.
-   **Web Server Hosting**: Installing and configuring Apache.
-   **Firewall Configuration**: Managing inbound rules using Security
    Groups.
-   **Live Troubleshooting**: Intentionally breaking and restoring
    connectivity.
-   **Cost Awareness**: Proper instance shutdown after completion.

------------------------------------------------------------------------

## 🏗️ Architecture

User (Browser)\
↓\
Public IP\
↓\
AWS Security Group (Firewall)\
↓\
EC2 Instance (Ubuntu 22.04)\
↓\
Apache Web Server\
↓\
Static HTML Website

This is a simple Infrastructure-as-a-Service (IaaS) setup demonstrating
core cloud fundamentals.

------------------------------------------------------------------------

## 🚀 What You Can Do

After completing this lab, you can:

-   Launch and configure EC2 instances
-   Connect securely using SSH
-   Install and manage Apache web servers
-   Configure Linux users and permissions
-   Manage firewall rules via Security Groups
-   Troubleshoot network-level access issues

------------------------------------------------------------------------

## 👩🏽‍🍳 The Process

I started by launching an EC2 instance using Ubuntu Server 22.04 LTS in
the Mumbai region (ap-south-1).\
A key pair was generated for secure SSH authentication.

Next, I configured a security group allowing:

-   SSH (Port 22) from my IP\
-   HTTP (Port 80) from anywhere

After connecting via SSH, I performed system updates and basic Linux
command verification.

Then, I installed Apache using:

``` bash
sudo apt install apache2 -y
```

After starting the Apache service, I verified access through the public
IP address.

To simulate a real-world support issue, I removed the HTTP (Port 80)
inbound rule from the security group.

Result: The website became inaccessible.

Fix: Re-added the HTTP rule and verified restoration immediately.

This reinforced the understanding of how firewall misconfigurations
impact production systems.

------------------------------------------------------------------------

## 🛠️ Troubleshooting Faced

### ❌ Website Not Accessible

Cause: - HTTP (Port 80) removed from Security Group

Fix: - Re-added HTTP inbound rule - Confirmed Apache service was running

------------------------------------------------------------------------

### ❌ Permission & User Management Issues

Commands practiced:

``` bash
sudo adduser testuser
sudo passwd testuser
sudo userdel testuser
chmod 600 test.txt
```

This helped strengthen Linux permission fundamentals.

------------------------------------------------------------------------

## 💰 Cost Discipline

-   Used Free Tier eligible `t2.micro`
-   Stopped instance after completion
-   Avoided unnecessary billing

Cloud cost management is part of real-world responsibility.

------------------------------------------------------------------------

## 📚 What I Learned

### 🖥️ EC2 Fundamentals

-   Instance provisioning
-   AMI selection
-   Key-pair authentication
-   Security Group configuration

### 🐧 Linux Administration

-   User creation & deletion
-   File permissions
-   Service management using `systemctl`
-   Package installation with `apt`

### 🌐 Networking Basics

-   Role of Security Groups as firewall
-   Difference between network issues vs server issues
-   Importance of verifying services before debugging network

### 🧠 Support Mindset

Instead of randomly changing settings, I learned to:

-   Identify the failure point
-   Validate configurations step-by-step
-   Restore services systematically

------------------------------------------------------------------------

## 🎯 How It Can Be Improved

-   Add HTTPS with SSL (Let's Encrypt)
-   Configure Nginx instead of Apache
-   Use Elastic IP
-   Automate deployment using User Data script
-   Add monitoring using CloudWatch

------------------------------------------------------------------------

## 🏁 Final Result

A fully functional Linux web server deployed on AWS EC2, with real-world
troubleshooting experience that aligns with Cloud / AWS L1 Support
Engineer expectations.

This project strengthens foundational cloud infrastructure skills and
prepares for more advanced DevOps and Cloud Engineering roles.

------------------------------------------------------------------------

## 🏁 Screenshots

![EC2 Instance Running on Mobxtreme and basic commands executed](Screenshots/Mobax.png)

![Website ran on EC2 instance](Screenshots/Website.png)
