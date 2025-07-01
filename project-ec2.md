# Project: Launching an EC2 Instance and Hosting a Web Server (NGINX)

## Objective
Set up an Amazon EC2 instance, connect to it via SSH, install NGINX, and make a basic cloud server publicly accessible via the internet.

---

## Steps I Followed

1. Launch EC2 Instance
- Opened AWS Console → EC2 → Launch Instance
- Selected **Ubuntu Server 22.04 LTS (64-bit)**
- Instance type: **t2.micro** (Free tier)
- Created and downloaded a new key pair: `test-key-pare.pem`
- Allowed SSH (port 22) and HTTP (port 80) in the security group
- Launched instance

---

2. Connect to EC2 via SSH
Opened Git Bash and ran:

- bash gdwschmod 400 ~/cloud-learning/test-key-pare.pem
- ssh -i ~/cloud-learning/test-key-pare.pem ubuntu@18.132.40.196>
- Accepted the fingerprint warning by typing yes
- Successfully connected and saw:
- Welcome to Ubuntu 22.04 LTS

---

3. Update Ubuntu Packages
- sudo apt update && sudo apt upgrade -y

---

4. Install NGINX Web Server
- sudo apt install nginx -y

---

5. Enable HTTP Access in Security Group
 -   Went to EC2 → Instances → Security Group
 -   Edited Inbound Rules:
 -   Added Rule: HTTP, port 80, source: Anywhere (0.0.0.0/0)
 -   Saved the rule

---

6. Test the Web Server
    Opened a browser
    Visited: http://18.132.40.196/

    Saw the NGINX welcome page
   ![Screenshot 2025-07-01 200745](https://github.com/user-attachments/assets/27f684ca-d9d7-45f7-b77b-8a5992bbf4a9)

   ---
8. What I Learned

- How to launch a basic Ubuntu EC2 server.
- How SSH keys work and how to connect securely.
- How to install and run a web server in the cloud.
- How to expose ports and make services publicly available

---

