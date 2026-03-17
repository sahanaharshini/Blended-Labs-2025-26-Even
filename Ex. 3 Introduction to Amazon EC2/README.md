# Lab 3 – Introduction to Amazon Elastic Compute Cloud (EC2)

## Author

* **Name**: Sahana Harshini K
* **Register Number**: 212223060236
* **Date of Submission**: 17-03-2026

---

## Objective

The objective of this experiment is to understand the fundamentals of Amazon Elastic Compute Cloud (EC2). This lab focuses on launching and managing a virtual server, understanding instance types and AMIs, connecting to an EC2 instance, monitoring its status, and performing basic instance operations such as start, stop, and terminate.

---

## Prerequisites

* Basic understanding of cloud computing concepts
* AWS account or AWS Academy Lab access
* Web browser with internet connectivity
* Basic knowledge of Linux commands (optional)

---

## Tools Used

* AWS Management Console
* Amazon EC2
* Key Pair
* Security Group
* SSH Client (PuTTY / Terminal)

---

## Tasks Performed

### Task 1: Explore Amazon EC2 Dashboard

Explore the EC2 service dashboard in the AWS Management Console. Observe the different sections such as Instances, AMIs, Instance Types, Key Pairs, Security Groups, and Elastic IPs.

---

### Task 2: Launch an EC2 Instance

Launch a new EC2 instance using Amazon Linux 2 AMI. Select an appropriate instance type (t2.micro) under the free tier. Configure basic settings such as instance name, key pair, and security group.

---

### Task 3: Configure Security Group

Configure a security group to allow inbound access:

* SSH (Port 22) from your IP address
* HTTP (Port 80) from anywhere (0.0.0.0/0)

This security group acts as a firewall for the instance.

---

### Task 4: Connect to EC2 Instance

Connect to the running EC2 instance using SSH. Use the downloaded key pair and connect via terminal or PuTTY.

For Amazon Linux:

```
ssh -i "keyname.pem" ec2-user@<Public-IP>
```

---

### Task 5: Perform Basic Instance Operations

Perform the following operations from the EC2 console:

* Stop the instance
* Start the instance
* Reboot the instance

Observe the state changes of the instance.

---

### Task 6: Monitor EC2 Instance

Monitor the EC2 instance using the Monitoring tab. Observe metrics such as CPU utilization, network in/out, and instance status checks.

---

### Task 7: Terminate EC2 Instance

Terminate the EC2 instance after completing the experiment to avoid unnecessary AWS charges.

---

## Workflow (Student Explanation)
Steps Followed

## **Step 1**: Launch EC2 Instance

Created a new EC2 instance named Web Server

Selected region: N. Virginia

Chose Amazon Linux 2023 AMI

Selected instance type: t2.micro

## **Step 2**: Configure Instance

Enabled:

Termination protection

Stop protection

Created and attached a Security Group

Added user data script to:

Install Apache

Start web server

## **Step 3**: Monitor Instance

Checked instance status using:

Status checks

CloudWatch metrics

System logs

Ensured the instance was running properly

## **Step 4**: Enable Web Access

Updated Security Group to allow:

HTTP (Port 80)

Opened browser and accessed:

Web server using public IP

## **Step 5**: Modify and Manage Instance

Changed instance type to t2.small

Increased EBS storage size

Checked EC2 service quotas

Tested stop protection

Finally, stopped the instance
---

## Output Screenshots (Attach 3)

### Screenshot 1: EC2 Dashboard / Instance List

<img width="1920" height="1080" alt="Screenshot (66)" src="https://github.com/user-attachments/assets/c17e04fc-28c0-4cc6-803a-46c0d0e9d4c1" />
---

### Screenshot 2: SSH Connection to Instance

<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/59323949-120a-4751-ad23-478a194a357a" />

---

### Screenshot 3: Instance Monitoring / Status

<img width="1600" height="696" alt="image" src="https://github.com/user-attachments/assets/d8cf71c9-8e0b-4700-b68d-aceb1e6a7d5a" />

---

## Result 

This experiment provided hands-on experience with Amazon EC2 by demonstrating how to launch, connect, manage, and monitor a virtual server in AWS. It helped in understanding the concept of Infrastructure as a Service (IaaS) and how compute resources can be provisioned and controlled on demand in the cloud.
