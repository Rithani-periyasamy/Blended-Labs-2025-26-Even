# Lab 5 – Build a Database Server (AWS)

## Author

* **Name**: Rithani P
* **Register Number**: 212225040340
* **Date of Submission**:20.11.2026
---

## Objective

The objective of this experiment is to understand how to deploy and configure a database server in AWS. This lab focuses on launching an EC2 instance, installing a database management system (DBMS), configuring basic database settings, creating a sample database, and validating connectivity to the database server.

---

## Prerequisites

* Basic understanding of cloud computing concepts
* AWS account or AWS Academy Lab access
* An existing VPC and EC2 knowledge (from previous labs)
* Basic knowledge of Linux commands and SQL

---

## Tools Used

* AWS Management Console
* Amazon EC2
* Security Groups
* SSH Client (Terminal / PuTTY)
* MySQL / MariaDB / PostgreSQL (any one)

---

## Tasks Performed

### Task 1: Launch EC2 Instance for Database Server

Launch a new EC2 instance using Amazon Linux 2 AMI. Select an appropriate instance type and configure key pair and security group.

---

### Task 2: Configure Security Group for Database Access

Modify the security group to allow:

* SSH (Port 22) for remote access
* Database port (e.g., MySQL – 3306 or PostgreSQL – 5432)

---

### Task 3: Connect to EC2 Instance

Connect to the EC2 instance using SSH from your local machine.

---

### Task 4: Install Database Server

Install a database server software such as MySQL, MariaDB, or PostgreSQL on the EC2 instance using package manager commands.

---

### Task 5: Start and Configure Database Service

Start the database service and configure basic settings such as root password and user privileges.

---

### Task 6: Create a Sample Database

Create a sample database and a table inside it. Insert a few records into the table.

---

### Task 7: Test Database Connectivity

Test the database server by connecting to it locally or remotely and performing basic SQL queries.

---

## Workflow (Student Explanation)

(Write the steps you followed in your own words)

First, a security group named DB Security Group was created to allow the web server to connect to the database using port 3306 (MySQL).
1.A DB Subnet Group was created with subnets from two Availability Zones to allow the database to run in a Multi-AZ environment for high availability.
2.A MySQL RDS instance named lab-db was created with the database name lab, username main, and password lab-password.
3.The database was associated with the DB Security Group and the Lab VPC so that the web server can securely connect to the database.
4.The web application running on the EC2 server was opened using its IP address, and the RDS endpoint, database name, username, and password were entered to interact with the database.

## Output Screenshots (Attach 3)

### Screenshot 1: EC2 Instance for Database Server

(Insert Screenshot Here)
<img width="1263" height="581" alt="WhatsApp Image 2026-11-20 at 7 01 51 PM" src="https://github.com/user-attachments/assets/4645c382-269a-4e1b-92a0-0e3ed7f5615d" />

---

### Screenshot 2: Database Service Running

(Insert Screenshot Here)
<img width="1264" height="580" alt="WhatsApp Image 2026-11-20 at 7 03 56 PM" src="https://github.com/user-attachments/assets/30de22a4-a6de-4e86-ac62-069863dc1da2" />

---

### Screenshot 3: Sample Database and Table

(Insert Screenshot Here)
<img width="1251" height="671" alt="WhatsApp Image 2026-11-20 at 7 05 09 PM" src="https://github.com/user-attachments/assets/f3834a3d-2504-45ff-b8ff-27132a7287e0" />

---

## Result

This experiment demonstrated how to build a database server in AWS using an EC2 instance. By installing and configuring a DBMS, creating a sample database, and testing connectivity, the fundamentals of hosting and managing a cloud-based database server were underst
