# 🚀 End-to-End DevOps CI/CD Pipeline on AWS EKS

## 📌 Project Overview

This project demonstrates a complete DevOps implementation for deploying a containerized web application on AWS EKS using modern DevOps tools and practices.

The solution automates infrastructure provisioning, configuration management, continuous integration, continuous deployment, security scanning, and monitoring.

---

## 🏗️ Architecture

```text
Developer
    │
    ▼
 GitHub Repository
    │
    ▼
 Jenkins CI/CD Pipeline
    │
 ┌──┴───────────────┐
 │                  │
 ▼                  ▼
SonarQube      OWASP Dependency Check
Code Analysis  Vulnerability Scan
 │
 ▼
Trivy Security Scan
 │
 ▼
Docker Build
 │
 ▼
Docker Hub / AWS ECR
 │
 ▼
AWS EKS Cluster
 │
 ▼
Kubernetes Deployment
 │
 ▼
Prometheus + Grafana Monitoring
```

---

# 🛠️ Tools & Technologies

| Category                 | Tools                  |
| ------------------------ | ---------------------- |
| Cloud Provider           | AWS                    |
| Infrastructure as Code   | Terraform              |
| Configuration Management | Ansible                |
| CI/CD                    | Jenkins                |
| Containerization         | Docker                 |
| Container Registry       | Docker Hub / AWS ECR   |
| Orchestration            | Kubernetes (EKS)       |
| Code Quality             | SonarQube              |
| Security Scan            | Trivy                  |
| Dependency Scan          | OWASP Dependency Check |
| Monitoring               | Prometheus             |
| Visualization            | Grafana                |
| Version Control          | Git & GitHub           |

---

# 📂 Project Structure

```text
project-root/
│
├── terraform/
│   ├── ec2.tf
│   ├── variables.tf
│   ├── outputs.tf
│   └── terraform.tf
│
├── ansible/
│   ├── hosts.ini
│   └── basic_setup.yml
│
├── kubernetes/
│   ├── deployment.yaml
│   ├── service.yaml
│   └── ingress.yaml
│
├── Jenkinsfile
│
├── Dockerfile
│
└── README.md
```

---

# 🎯 Project Objectives

✅ Automate AWS infrastructure provisioning using Terraform

✅ Configure servers automatically using Ansible

✅ Implement CI/CD pipeline using Jenkins

✅ Deploy application to AWS EKS

✅ Perform Security & Vulnerability Scanning

✅ Monitor application and infrastructure health

✅ Achieve Infrastructure as Code (IaC)

---

# ☁️ AWS Infrastructure

The following AWS resources are provisioned:

* VPC
* Subnets
* Security Groups
* EC2 Instance (Jenkins Master)
* EKS Cluster
* S3 Bucket (Terraform State)
* IAM Roles & Policies

---

# 🐳 Dockerization

Build Docker Image:

```bash
docker build -t my-app .
```

Run Container:

```bash
docker run -d -p 3000:3000 my-app
```

---

# ⚙️ Terraform Deployment

Initialize Terraform:

```bash
terraform init
```

Validate Configuration:

```bash
terraform validate
```

Review Changes:

```bash
terraform plan
```

Create Infrastructure:

```bash
terraform apply -auto-approve
```

Destroy Infrastructure:

```bash
terraform destroy -auto-approve
```

---

# 🤖 Ansible Configuration

Verify Connectivity:

```bash
ansible ubuntu_servers -i hosts.ini -m ping
```

Run Playbook:

```bash
ansible-playbook -i hosts.ini basic_setup.yml
```

The playbook installs:

* Docker
* Docker Compose
* Jenkins
* AWS CLI
* kubectl
* eksctl
* Trivy

---

# 🔧 Jenkins Setup

Access Jenkins:

```text
http://<EC2-PUBLIC-IP>:8080
```

Install Plugins:

* Docker
* Pipeline Stage View
* SonarQube Scanner
* OWASP Dependency Check
* GitHub Integration

---

# 🔍 SonarQube Integration

Run SonarQube:

```bash
docker run -d \
--name sonarqube \
-p 9000:9000 \
sonarqube:lts-community
```

Access:

```text
http://<EC2-PUBLIC-IP>:9000
```

Features:

* Static Code Analysis
* Code Smells Detection
* Bug Detection
* Quality Gates

---

# 🛡️ Security Scanning

## OWASP Dependency Check

Detect vulnerable dependencies before deployment.

## Trivy Scan

Filesystem Scan:

```bash
trivy fs .
```

Docker Image Scan:

```bash
trivy image my-image:latest
```

---

# ☸️ Kubernetes Deployment

Deploy Application:

```bash
kubectl apply -f deployment.yaml
kubectl apply -f service.yaml
```

Check Pods:

```bash
kubectl get pods
```

Check Services:

```bash
kubectl get svc
```

---

# 📊 Monitoring

## Prometheus

Collects:

* Node Metrics
* Container Metrics
* Kubernetes Metrics

## Grafana

Provides dashboards for:

* CPU Usage
* Memory Usage
* Pod Health
* Cluster Performance

---

# 🚀 CI/CD Pipeline Stages

### Stage 1: Source Code Checkout

```text
GitHub → Jenkins
```

### Stage 2: Code Quality Analysis

```text
SonarQube Scan
```

### Stage 3: Dependency Vulnerability Scan

```text
OWASP Dependency Check
```

### Stage 4: Security Scan

```text
Trivy Scan
```

### Stage 5: Build Docker Image

```text
Docker Build
```

### Stage 6: Push Image

```text
Docker Hub / AWS ECR
```

### Stage 7: Deploy to EKS

```text
Kubernetes Deployment
```

### Stage 8: Monitoring

```text
Prometheus + Grafana
```

---

# 📸 Screenshots

Add screenshots here:

```text
screenshots/
├── architecture.png
├── jenkins-dashboard.png
├── sonarqube-report.png
├── trivy-scan.png
├── grafana-dashboard.png
└── eks-cluster.png
```

---

# 📈 Key Features

* Fully Automated CI/CD Pipeline
* Infrastructure as Code
* Security Scanning
* Code Quality Analysis
* Kubernetes Deployment
* AWS EKS Integration
* Monitoring & Alerting
* Production Ready Architecture

---

# 🏆 Learning Outcomes

Through this project I gained hands-on experience with:

* Terraform
* Ansible
* Jenkins
* Docker
* Kubernetes
* AWS EKS
* SonarQube
* Trivy
* Prometheus
* Grafana
* CI/CD Best Practices

---

# 👨‍💻 Author

**Ismail Saiyed**

DevOps Engineer | Cloud Enthusiast | Kubernetes Practitioner

GitHub: https://github.com/<your-github-username>

LinkedIn: https://linkedin.com/in/<your-profile>

---

# ⭐ Support

If you found this project helpful, please consider giving it a ⭐ on GitHub.

# steps followed

Step-1 Create new Iam user

Go to aws console->IAM-> create user

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/3897eb7c-27ea-4758-ad0f-01c665553662" />

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/4343bdd2-e76f-443f-8ab6-10e58bc3dcd4" />

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/a7fbad86-73e3-4814-9cc0-c10246d24e3a" />

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/1e1bd5eb-527d-4006-904a-d38e06f71da5" />

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/ded5f18e-933a-4dfd-b85f-82463d04d35e" />

configuring aws in local computer

aws configure

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/1262a993-838b-4f0b-8dd9-cb8b0e5e9afd" />

Enter your credentials for the newly create IAM user as above

Step-2 creating an jenkinsmaster ec2 instance using terraform

Ec2.tf

Step-2 creating an jenkinsmaster ec2 instance using terraform
Ec2.tf
provider "tls" {}

resource "tls_private_key" "generated" {
  algorithm = "RSA"
  rsa_bits  = 4096
}

resource "aws_key_pair" "deployer" {
  key_name   = "capstone-user-key"
  public_key = tls_private_key.generated.public_key_openssh
}

resource "local_file" "private_key" {
  content         = tls_private_key.generated.private_key_pem
  filename        = "${path.module}/capstone-user-key.pem"
  file_permission = "0400"
}

resource "aws_default_vpc" "default" {

}

resource "aws_security_group" "allow_user_to_connect" {
  name        = "allow TLS"
  description = "Allow user to connect"
  vpc_id      = aws_default_vpc.default.id
  ingress {
    description = "port 22 allow"
    from_port   = 22
    to_port     = 22
    protocol    = "tcp"
    cidr_blocks = ["0.0.0.0/0"]
  }

  egress {
    description = " allow all outgoing traffic "
    from_port   = 0
    to_port     = 0
    protocol    = "-1"
    cidr_blocks = ["0.0.0.0/0"]
  }

  ingress {
    description = "port 80 allow"
    from_port   = 80
    to_port     = 80
    protocol    = "tcp"
    cidr_blocks = ["0.0.0.0/0"]
  }

   ingress {
    description = "port 8080 jenkins allow"
    from_port   = 8080
    to_port     = 8080
    protocol    = "tcp"
    cidr_blocks = ["0.0.0.0/0"]
  }

  ingress {
    description = "port 443 allow"
    from_port   = 443
    to_port     = 443
    protocol    = "tcp"
    cidr_blocks = ["0.0.0.0/0"]
  }

  tags = {
    Name = "mysecurity"
  }
}

resource "aws_instance" "jenkinsmaster" {
  ami             = var.ami_id
  instance_type   = var.instance_type
  key_name        = aws_key_pair.deployer.key_name
  security_groups = [aws_security_group.allow_user_to_connect.name]
  tags = {
    Name = "jenkinsmaster"
  }
  root_block_device {
    volume_size = 30 
    volume_type = "gp3"
  }
}

Terraform.tf
terraform {
  required_providers {
    aws = {
      source  = "hashicorp/aws"
      version = "5.65.0"
    }
  }
}

provider "aws" {
  region = var.aws_region
}


Outputs.tf
output "ec2_public_ip" {
  description = "Public IP of the EC2 instance"
  value       = aws_instance.jenkinsmaster.public_ip
}


Variables.tf
variable "aws_region" {
  description = "AWS region where resources will be provisioned"
  default     = "ap-south-1"
}

variable "ami_id" {
  description = "AMI ID for the EC2 instance"
  default     = "ami-07a00cf47dbbc844c"
}

variable "instance_type" {
  description = "Instance type for the EC2 instance"
  default     = "t2.large"
}


Commands to execute above files

a.	Terraform init

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/39df7416-48e9-4d71-8a43-359b85fa71d7" />

b.	Terraform plan

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/49d0f847-a58f-4d89-8a6c-3f859be684b4" />
















