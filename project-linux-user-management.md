# Project: Linux User Management and AWS Console Practice

## Objective

The goal of this task was to learn how to manage users and permissions on a Linux server, practice using basic Linux commands, and get more familiar with the AWS EC2 dashboard.

---

## Steps Taken

### 1. Connected to EC2 via SSH

I used the SSH key to connect to my EC2 instance:

```bash
ssh -i ~/cloud-learning/test-key-pare.pem ubuntu@<your-ec2-ip>
```

---

2. Created a New User

I created a new user called devuser and set a password:
```bash
sudo adduser devuser
```

---

3. Gave Sudo Access to the User

To give devuser administrative privileges:
```bash
sudo usermod -aG sudo devuser
```

---

4. Switched to the New User

I logged into the new user and verified it:
```bash
su - devuser
whoami
```
Output confirmed I was logged in as devuser.

---

5. Tested File Permissions

I created a file and changed its permissions to understand how chmod works:
```bash
cd /home/devuser
touch test.txt
ls -l
chmod 700 test.txt
ls -l
chmod 777 test.txt
ls -l
```
I saw how permission bits changed for the file.

---

6. Practiced Basic Linux Commands

I used the following commands to explore system info:
```bash
df -h         # Disk usage
top           # Process list
uptime        # System load
hostname -I   # Get IP address
history       # View command history
```

---


7. AWS Console Review

In the AWS Console, I:

- Visited the EC2 dashboard
- Viewed the running instance details
- Inspected the security group (checked open ports)
- Noted the region: eu-west-2 (London)

---

Screenshots

-  Logged in as devuser
-  File permissions before and after chmod
-  EC2 instance and security group in AWS Console

![Screenshot 2025-07-02 195618](https://github.com/user-attachments/assets/ed874a19-64ae-4b7c-8e25-645060ac5d1e)

---

Summary

Today I learned how to:

 - Add users and manage permissions on a Linux server
 - Switch users and grant sudo access
 - Work with file permissions using chmod
 - Use basic system commands
 - Navigate the AWS EC2 dashboard and security settings

This sets the foundation for securing servers and preparing for automation with cloud tools.

---
