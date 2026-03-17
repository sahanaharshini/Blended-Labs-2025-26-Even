# Lab 4 – Working with Amazon Elastic Block Store (EBS)

## Author

* **Name**: Sahana Harshini K
* **Register Number**: 212223060236
* **Date of Submission**: 17-03-2026

---

## Objective

The objective of this experiment is to understand how Amazon Elastic Block Store (EBS) provides persistent block-level storage for EC2 instances. This lab focuses on creating and attaching an EBS volume, formatting and mounting it on an EC2 instance, storing data, and verifying data persistence after instance reboot.

---

## Prerequisites

* Basic understanding of cloud computing concepts
* AWS account or AWS Academy Lab access
* An existing EC2 instance (Amazon Linux 2 preferred)
* Basic knowledge of Linux commands

---

## Tools Used

* AWS Management Console
* Amazon EC2
* Amazon EBS
* SSH Client (Terminal / PuTTY)

---

## Tasks Performed

### Task 1: Explore Amazon EBS

Explore the Amazon EBS service through the EC2 dashboard. Observe different volume types such as General Purpose SSD (gp2/gp3), Provisioned IOPS SSD, Throughput Optimized HDD, and Cold HDD.

---

### Task 2: Create an EBS Volume

Create a new EBS volume in the same Availability Zone as the EC2 instance. Choose an appropriate size and volume type.

---

### Task 3: Attach EBS Volume to EC2 Instance

Attach the created EBS volume to the running EC2 instance as an additional block device.

---

### Task 4: Format the EBS Volume

Connect to the EC2 instance using SSH and format the attached volume with a file system (for example, ext4).

---

### Task 5: Mount the EBS Volume

Mount the formatted volume to a directory in the EC2 instance (for example, /data or /mnt/ebs).

---

### Task 6: Store Data in EBS Volume

Create files and directories inside the mounted EBS volume and store sample data.

---

### Task 7: Verify Data Persistence

Reboot the EC2 instance and verify that the data stored in the EBS volume is still available after reboot.

---

## Workflow (Student Explanation)

## **Step 1**: Login and Open EC2

Logged in to AWS Management Console

Opened EC2 Dashboard

Went to Elastic Block Store (EBS) section

## **Step 2**: Explore Volume Types

Observed different EBS volume types:

General Purpose SSD (gp2/gp3)

Provisioned IOPS SSD

Throughput Optimized HDD

Cold HDD

## **Step 3**: Create EBS Volume

Clicked on Volumes → Create Volume

Selected volume type: gp3 (General Purpose SSD)

Entered size (example: 8 GB)

Chose same Availability Zone as EC2

Clicked Create Volume

## **Step 4**: Attach Volume to EC2

Selected the created volume

Clicked Attach Volume

Chose running EC2 instance

Attached as device: /dev/xvdf

## **Step 5**: Connect to Instance

Connected to EC2 using SSH

Checked disk using command:

lsblk

## **Step 6**: Format the Volume

Formatted the disk using:

sudo mkfs -t ext4 /dev/xvdf

## **Step 7**: Mount the Volume

Created a folder:

sudo mkdir /mnt/ebs

Mounted the volume:

sudo mount /dev/xvdf /mnt/ebs

Verified using:

df -h

## **Step 8**: Store Data

Created a file:

sudo touch /mnt/ebs/sample.txt

Added some sample data inside the file

## **Step 9**: Reboot and Verify

Rebooted the EC2 instance

Reconnected using SSH

Checked the mounted folder

Verified that data was still available

## **Conclusion**

EBS volume provides persistent storage

Data remains safe even after instance reboot
---

## Output Screenshots (Attach 3)

### Screenshot 1: EBS Volume Created

<img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/c908286c-b4c3-4833-9df0-f465ad106be0" />

---

### Screenshot 2: EBS Volume Attached to EC2


<img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/0385e2d9-46e9-4e4d-8db2-71c8683f94dc" />

<img width="1216" height="1020" alt="image" src="https://github.com/user-attachments/assets/4cb8d019-4d50-4da7-ad2d-e5d4f2f91229" />

<img width="1216" height="1020" alt="image" src="https://github.com/user-attachments/assets/5f5264d6-a275-4b3b-98a3-db98885b572b" />

---

### Screenshot 3: Mounted Volume with Data


<img width="1216" height="1020" alt="image" src="https://github.com/user-attachments/assets/1a450ebc-118b-4cf6-a1ce-642519d3821d" />

<img width="1216" height="1020" alt="image" src="https://github.com/user-attachments/assets/33296046-5379-45d8-9662-1b8719e44213" />

---

## Result / Conclusion

This experiment demonstrated how Amazon EBS provides persistent storage for EC2 instances. By creating, attaching, formatting, and mounting an EBS volume, and by verifying data after reboot, the concept of durable block storage in the cloud was clearly understood.
