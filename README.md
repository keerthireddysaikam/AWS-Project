# 🚀 AWS High Availability Web Application with ALB, Monitoring & Automation

## 📌 Project Overview

This project demonstrates the design and implementation of a **Highly Available, Automated, and Monitored Web Application Infrastructure** on AWS Cloud.

The architecture ensures:

* High Availability across multiple Availability Zones
* Load-balanced traffic distribution
* Automated monitoring and alerting
* Scheduled cost optimization
* Serverless automation using Lambda
* Centralized monitoring dashboard

This project simulates a production-ready DevOps deployment environment.

---

## 🏗 Architecture Components

* Custom VPC (CIDR: 10.0.0.0/22)
* 2 Public Subnets (Different Availability Zones)
* 2 EC2 Instances (Nginx installed)
* Application Load Balancer (ALB)
* Target Group with health checks
* CloudWatch Alarms
* AWS Lambda for automation
* EventBridge for scheduling
* SNS for notifications
* S3 bucket for application storage
* CloudWatch Dashboard for monitoring

---

## 🔧 Technologies Used

* AWS EC2
* AWS VPC
* Application Load Balancer (ALB)
* AWS CloudWatch
* AWS Lambda
* Amazon EventBridge
* Amazon SNS
* Amazon S3
* Nginx
* Linux (Ubuntu)

---

## 🛠 Implementation Steps

### 1️⃣ VPC & Networking Setup

* Created custom VPC with CIDR `10.0.0.0/22`
* Created 2 public subnets in different Availability Zones
* Attached Internet Gateway
* Configured Route Tables
* Configured Security Groups for HTTP (80) and SSH (22)

---

### 2️⃣ EC2 Configuration

* Launched 2 EC2 instances in different Availability Zones
* Installed Nginx on both instances
* Deployed two different web applications:

  * VM1 → Web Application 1
  * VM2 → Web Application 2
* Verified application access via public IP

---

### 3️⃣ Application Load Balancer (ALB)

* Created Application Load Balancer
* Created Target Group
* Registered both EC2 instances
* Configured health checks
* Verified traffic distribution between instances

---

### 4️⃣ Monitoring & Alerts

* Created CloudWatch Alarm:

  * Trigger condition: CPU Utilization > 70%
* Configured SNS Topic for email notifications
* Subscribed email to SNS topic
* Verified alert delivery

---

### 5️⃣ Lambda Automation

Developed Lambda functions to:

* Stop EC2 instance when CPU utilization exceeds threshold
* Send notification when instance state changes
* Start/Stop instances programmatically

This ensures automated infrastructure management.

---

### 6️⃣ Scheduled Start/Stop (Cost Optimization)

Used Amazon EventBridge to:

* Start EC2 instances at 9:00 AM
* Stop EC2 instances at 5:00 PM
* Send notifications on state change

This simulates office-hour usage to reduce infrastructure cost.

---

### 7️⃣ CloudWatch Dashboard

Created a custom CloudWatch dashboard to monitor:

* CPU Utilization
* Alarm status
* Instance state

Provides centralized monitoring visibility.

---

### 8️⃣ S3 Storage

* Stored web application files in S3 bucket
* Configured proper IAM permissions
* Used S3 as centralized application storage

---

## 📊 DevOps Concepts Demonstrated

* High Availability Architecture
* Load Balancing
* Infrastructure Monitoring
* Alerting & Notifications
* Serverless Automation
* Scheduled Infrastructure Management
* Cost Optimization
* Observability
* Cloud Networking

---

## 🔐 Security Best Practices

* Restricted Security Group rules
* IAM roles for EC2 and Lambda
* Principle of Least Privilege
* Health checks for instance validation

---

## 👨‍💻 Author

Ajith Kumar
Aspiring DevOps Engineer
