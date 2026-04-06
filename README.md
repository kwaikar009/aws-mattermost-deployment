
 # 🚀 Scalable Team Communication Platform Deployment on AWS (Mattermost)

## 📌 Project Overview

This project demonstrates the deployment of a **self-hosted enterprise team communication platform (Mattermost)** on AWS using a secure and scalable cloud architecture.

The solution is built within a custom VPC using public and private subnets to ensure controlled access, isolation, and secure communication between application and database layers.

---

## 🏗️ Architecture Highlights

* Custom VPC with public and private subnets
* Application server hosted in **public subnet**
* Database server hosted in **private subnet** for enhanced security
* Internet Gateway for external access
* NAT Gateway for outbound internet access from private subnet
* EC2 instances used for application and database hosting
* Secure communication configured using Security Groups

---

## ☁️ AWS Services Used

* EC2 (Compute)
* VPC (Networking)
* Subnets (Public & Private)
* Internet Gateway
* NAT Gateway
* Security Groups
* Elastic IP

---

## ⚙️ Implementation Steps

### 1. Network Setup

* Created custom VPC with CIDR block
* Configured:

  * Public subnet for application server
  * Private subnet for database server

### 2. Internet & Routing

* Attached Internet Gateway to VPC
* Configured route tables for public and private subnets
* Set up NAT Gateway for private subnet outbound traffic

### 3. EC2 Deployment

* Launched EC2 instances using **Amazon Linux 2 AMI**
* Assigned Elastic IP to application server
* Used application server as a **bastion host** to access private database server

### 4. Application Setup (Mattermost)

* Manually Installed and configured Mattermost on application server.
* Verified application accessibility via browser

### 5. Database Setup

* Installed MySQL on database server
* Configured connectivity between application and database layers

---

## 🔐 Security Considerations

* Database server deployed in private subnet to restrict direct public access
* Security Groups configured to allow controlled access between application and database layers
* SSH access managed via bastion host

---

## 🛠️ Challenges Faced

* Initial connectivity issues between application and database servers due to Security Group misconfiguration
* Required debugging of routing and access rules for private subnet
* Resolved application access issues after deployment

---

## 📈 Key Learnings

* Hands-on experience in **VPC design and subnet isolation**
* Understanding of **secure cloud architecture and access control**
* Experience deploying and validating real-world applications on AWS

---

## 🚀 Future Enhancements
* Restrict database access to application server only (remove public access)
* Implement Application Load Balancer for scalability
* Add Auto Scaling for high availability

## 🔧 DevOps Perspective
* Deployment was performed manually using AWS Console and SSH
* The setup can be automated using Infrastructure as Code (IaC) tools like Terraform
* Application deployment can be integrated into a CI/CD pipeline using Jenkins or GitHub Actions



---
