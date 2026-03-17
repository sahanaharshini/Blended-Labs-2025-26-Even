# Build Your VPC and Launch a Web Server (AWS) 

## Author

* **Name**: Sahana Harshini K
* **Register Number**: 212223060236
* **Date of Submission**: 17-03-2026

---

## Objective

The objective of this experiment is to understand how to design and configure a basic network infrastructure in AWS using a Virtual Private Cloud (VPC). This lab focuses on creating a VPC with a public subnet, configuring an Internet Gateway and route table, launching an EC2 instance, and hosting a simple web server that can be accessed over the internet.

---

## Prerequisites

* Basic understanding of cloud computing concepts
* AWS account or AWS Academy Lab access
* Web browser with internet connectivity

---

## Tools Used

* AWS Management Console
* Amazon VPC
* Amazon EC2
* Internet Gateway
* Route Table
* Security Groups

---

## Tasks Performed

### Task 1: Create a VPC

Create a new Virtual Private Cloud (VPC) with a private IP address range. The VPC acts as a logically isolated network in AWS where all other resources will be deployed.

Students should create a VPC with an appropriate CIDR block (for example, 10.0.0.0/16) and assign a meaningful name.


### Task 2: Create a Public Subnet

Create a subnet inside the VPC to host public resources. Enable auto-assign public IPv4 so that instances launched in this subnet receive a public IP address.

The subnet should use a smaller CIDR range (for example, 10.0.1.0/24).


### Task 3: Create and Attach Internet Gateway

Create an Internet Gateway (IGW) and attach it to the VPC. This allows communication between resources in the VPC and the internet.


### Task 4: Configure Route Table

Create a route table and add a default route (0.0.0.0/0) pointing to the Internet Gateway. Associate this route table with the public subnet.

This step ensures that traffic from the subnet can reach the internet.


### Task 5: Create Security Group

Create a security group to act as a virtual firewall for the EC2 instance. Configure inbound rules to allow:

SSH on port 22

HTTP on port 80


### Task 6: Launch EC2 Instance

Launch an EC2 instance inside the public subnet using Amazon Linux 2 AMI and a suitable instance type (t2.micro).

Attach the previously created security group and key pair.


### Task 7: Configure Web Server

Install and start a web server (Apache HTTPD) on the EC2 instance using user data or manual commands.

Create a simple HTML page and verify that it can be accessed from a web browser using the public IP address of the instance.---

## Workflow (Student Explanation)

## **Step 1**: Login

Open AWS Management Console

Select region: N. Virginia (us-east-1)

Login to your account

## **Step 2**: Create VPC

Go to VPC service

Create a custom VPC

Add:

Public subnet

Private subnet

Attach:

Internet Gateway (IG) → for internet access

NAT Gateway → for private subnet internet access

## **Step 3**: Add More Subnets

Create extra subnets in another Availability Zone

Update route tables:

Public subnet → internet access

Private subnet → NAT gateway access

## **Step 4**: Create Security Group

Create a Security Group

Name: Web Security Group

Allow:

HTTP (Port 80)

Source: Anywhere (0.0.0.0/0)

## **Step 5**: Launch EC2 Instance

Go to EC2 service

Launch instance in public subnet

Enable:

Auto-assign public IP

Attach:

Security group

Key pair

## **Step 6**: Setup Web Server

Add user data script:

Install Apache

Deploy web app

Open browser and enter:

Public DNS of EC2

Verify the website is working
---

## Output Screenshots (Attach 3)

### Screenshot 1: VPC and Subnet Details

<img width="1598" height="696" alt="image" src="https://github.com/user-attachments/assets/669d03b9-311c-427e-a4a9-3e932acec85b" />

---

### Screenshot 2: EC2 Instance Running

<img width="1595" height="711" alt="image" src="https://github.com/user-attachments/assets/2d0e5fdc-df6d-447e-a496-faa2e92f37a5" />

---

### Screenshot 3: Web Server Output in Browser

<img width="1600" height="809" alt="image" src="https://github.com/user-attachments/assets/49dfefbc-7285-4e33-af4e-d5b58a357a97" />

---

## Result 

This experiment successfully demonstrated the creation of a custom VPC and deployment of a public-facing web server in AWS. By configuring networking components such as subnets, route tables, and security groups, and by launching an EC2 instance with a web server, the basic architecture of a cloud-hosted application was understood.
