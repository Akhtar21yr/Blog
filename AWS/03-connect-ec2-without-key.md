# Connect to Your EC2 Instance Without a Key Pair Using Username and Password

This guide will walk you through the steps to connect to your EC2 instance using a username and password instead of a key pair.

## Prerequisites

- You should have an EC2 instance running. If you need help launching one, refer to my [previous guide](https://github.com/Akhtar21yr/Blog/blob/main/AWS/02-first-ec2.md).

## Step-by-Step Guide

### Step 1: Connect to Your Instance with a Key Pair OR  Through AWS Browser cli 

Initially, use the SSH method with your key pair to connect to your instance:

```ssh
ssh -i "your-key-pair.pem" ec2-user@your-instance-public-dns
```
![aws-sh-text](./aws-smd-ssh-key.png)
OR (if you don't have key)

connect through browser cli provided by amazon.

- [x]  Step 1

### Step 2: Set Up Password Authentication

**1.Edit the SSH Configuration File:**
```sh
sudo nano /etc/ssh/sshd_config
```
#### Modify the Following Lines : 

Find and change the line:
```sh
PasswordAuthentication no
```
to:
```sh
PasswordAuthentication yes
```
#### Press "control + s " to save
![alt text](./image.png)


**2.Edit the 60-cloudimg-settings File:**
```sh
sudo nano /etc/ssh/sshd_config.d/60-cloudimg-settings.conf
```
#### Modify the Following Lines : 

Find and change the line:
```sh
PasswordAuthentication no
```
to:
```sh
PasswordAuthentication yes
```
#### Press "control + s " to save

**3.Restart the SSH Service:**
```sh
sudo systemctl restart ssh
```
- [x]  Step 2

### Step 3: Create a User and Set a Password
**1.Add a New User:**
```sh
sudo adduser <new_username>
```
**2.Set a Password for the New User:**
```sh
sudo passwd <new_username>
```
- [x]  Step 3

### Step 4: Connect Using Username and Password
Now, you can connect to your instance using the new username and password:
```sh
ssh new_username@your_instance_public_ip
```
- [x]  Step 4

## Conclusion
You have successfully configured your EC2 instance to allow connections using a username and password. This method can be useful for scenarios where you prefer traditional login methods over key pairs.

For more details, check out my detailed blog post.

Happy learning and secure computing!

#AWS #CloudComputing #EC2 #TechTeaching #LearningJourney #CloudInnovation












