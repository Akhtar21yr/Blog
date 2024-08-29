![mine](../assets/mine/github-banner-mine.png)
## **Remotely Data Transfer: EC2 to EC2 Using Key or Password**
Transferring data between two AWS EC2 instances can be done securely using SSH with either an SSH key pair or a password (though SSH keys are the recommended method for security).

![alt text](../assets/aws/12-ec2-to-ec2/scp-between-linux-computers-featured-removebg-preview.png)
* #### **Pre-Requisites**

  * **SSH Access**: Ensure that both EC2 instances have SSH access enabled (TCP port 22 open) in their security groups.  
  * **SSH Key Pair**: Have access to the private key (`.pem` file) associated with the EC2 instances, if using key-based authentication.  
  * **Network Connectivity**: Ensure both instances are in the same VPC or have network connectivity if in different VPCs.

### **Using SSH Key for Data Transfer**

**Step 1: Configure Security Groups**

* Modify the security groups of both EC2 instances to allow SSH traffic from each other's public or private IP addresses.

**Step 2: Transfer Data Using `scp`**

**Using `scp`**:  
 
```sh
scp -i /path/to/private_key.pem /path/to/local/file ec2-user@remote_host:/path/to/destination/
```

  
  * `-i` specifies the SSH private key.  
  * Replace `/path/to/private_key.pem` with the path to your private key file.  
  * Replace `/path/to/local/file` with the file path you want to transfer.  
  * Replace `ec2-user` with the username (`ec2-user` for Amazon Linux, `ubuntu` for Ubuntu, etc.).  
  * Replace `remote_host` with the destination EC2 instance's public or private IP address or DNS.

**Step 3: Transfer Data Using `rsync`**

**Using `rsync`**:  
```sh
rsync -avz -e "ssh -i /path/to/private_key.pem" /path/to/local/directory/ ec2-user@remote_host:/path/to/destination/
```

*   
  * `-e` specifies SSH options, such as the key file.  
  * This command syncs the local directory to the remote instance, transferring only changed files.

