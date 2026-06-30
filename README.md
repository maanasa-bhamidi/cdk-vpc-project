# AWS CDK Python VPC Project

A hands-on **Infrastructure as Code (IaC)** project that builds a secure and isolated AWS networking environment using **Python** and the **AWS Cloud Development Kit (CDK)**.

---

## 📌 Project Overview

This project demonstrates how to provision AWS infrastructure entirely through code. With a single deployment command, it creates a secure networking foundation following AWS best practices.

The infrastructure includes:

- A custom Amazon VPC
- Public and private subnets
- Security Group with controlled inbound access
- IAM Role for secure EC2 access to Amazon S3
- Fully automated deployment using AWS CDK

---

## 🛠️ Infrastructure Created

### 🌐 Custom Amazon VPC
- Creates a dedicated Virtual Private Cloud (VPC)
- Separates resources into:
  - Public Subnets
  - Private Subnets
- Provides a secure and isolated networking environment

### 🔒 Security Group
Configures firewall rules that allow only:

- SSH (Port 22)
- HTTP (Port 80)

All other inbound traffic remains blocked unless explicitly permitted.

### 🔑 IAM Role
Creates an IAM Role that grants EC2 instances:

- Read-only access to Amazon S3
- No hardcoded credentials
- Secure access using IAM best practices

---

## ☁️ AWS Services Used

| Service | Purpose |
|----------|---------|
| Amazon VPC | Creates an isolated virtual network |
| Amazon EC2 Security Groups | Controls inbound and outbound network traffic |
| AWS IAM | Provides secure permissions using roles |
| AWS CDK (Python) | Defines and deploys infrastructure as code |

---

## 📂 Project Structure

```text
cdk-vpc-project/
│
├── app.py
├── requirements.txt
├── cdk.json
├── README.md
│
└── cdk_vpc_project/
    ├── __init__.py
    └── cdk_vpc_project_stack.py
```

---

## 🚀 Deployment Steps

### 1. Clone the repository

```bash
git clone https://github.com/maanasa-bhamidi/cdk-vpc-project.git
cd cdk-vpc-project
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Bootstrap your AWS environment

```bash
cdk bootstrap
```

### 4. Deploy the infrastructure

```bash
cdk deploy
```

When prompted, confirm the deployment.

---

## 🧹 Destroy the Infrastructure

To avoid unwanted AWS charges, remove the deployed resources when finished.

```bash
cdk destroy
```

---

## 🎯 What I Learned

Through this project, I gained hands-on experience with:

- Writing Infrastructure as Code using Python and AWS CDK
- Designing secure AWS networking with Amazon VPC
- Creating public and private subnet architectures
- Configuring Security Groups for controlled network access
- Implementing IAM Roles using the principle of least privilege
- Automating cloud infrastructure deployment instead of manual AWS Console configuration

---

## 📚 Technologies Used

- Python
- AWS CDK
- Amazon VPC
- AWS IAM
- Amazon EC2 Security Groups

---

## 📸 Architecture

> *(Add your architecture diagram or deployment screenshots here.)*

Example:

```
Internet
    │
    ▼
Public Subnet
    │
Security Group
    │
Private Subnet
    │
EC2 Instance
    │
IAM Role
    │
Amazon S3
```

---

## 👨‍💻 Author

**Maanasa Bhamidi**

GitHub: https://github.com/maanasa-bhamidi