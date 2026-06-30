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

**S Narsimha**

DevOps Engineer | Cloud Enthusiast

GitHub: https://github.com/s-narsimha

This repository contains the Capstone Project completed collaboratively by *Group 1 (Batch 14)* as part of the HeroVired Multi-Cloud Architecture & DevOps Program.

Our team worked together throughout the project by following the official capstone guidelines, performing all required hands-on practical implementations, and applying DevOps best practices to build a complete end-to-end CI/CD pipeline for a containerized web application on AWS EKS.

The project covers Infrastructure as Code, configuration management, continuous integration and deployment, containerization, Kubernetes orchestration, security scanning, and monitoring using industry-standard DevOps tools.

*Group Members:*

* Ismail Abdulrahim Saiyed
* Ritesh Sharma
* Saurabh Suman
* Hari Kumar
* S. Narsimha Deekshitulu



---



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


c.	Terraform apply

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/3e5dc33c-e70a-431d-bfcf-d100f4006c4f" />

Output:

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/b4627a04-d1fe-45a6-b7d2-0723fd2112a5" />

Step-3 : configuring following on Jenkins master using Ansible configuration management Tool

IMP: After creation of  ec2-instance as in previous step update public ip in hosts.ini in ansible folder

•	docker
•	docker-compose-v2
•	jenkins
•	awscli
•	kubectl
•	eksctl
•	trivy

Hosts.ini

[ubuntu_servers]
jenkinsmaster ansible_host=65.2.122.131
[ubuntu_servers:vars]
ansible_user=ubuntu
ansible_ssh_private_key_file=~/capstone-user-key.pem
ansible_ssh_common_args='-o StrictHostKeyChecking=no'

basic_setup.yml
---
- name: Setup Docker, Docker Compose v2 and Jenkins on Ubuntu 24
  hosts: all
  become: yes

  vars:
    jenkins_keyring: /etc/apt/keyrings/jenkins-keyring.asc
    docker_keyring: /etc/apt/keyrings/docker.gpg

  tasks:

    # -----------------------------
    # SYSTEM UPDATE
    # -----------------------------
    - name: Update apt cache
      apt:
        update_cache: yes

    - name: Install required packages
      apt:
        name:
          - ca-certificates
          - curl
          - gnupg
          - lsb-release
        state: present

    # -----------------------------
    # DOCKER INSTALLATION
    # -----------------------------
    - name: Ensure keyrings directory exists
      file:
        path: /etc/apt/keyrings
        state: directory
        mode: '0755'

    - name: Download Docker GPG key
      get_url:
        url: https://download.docker.com/linux/ubuntu/gpg
        dest: /tmp/docker.asc

    - name: Convert Docker GPG key
      command: gpg --dearmor -o {{ docker_keyring }} /tmp/docker.asc
      args:
        creates: "{{ docker_keyring }}"

    - name: Add Docker repository
      apt_repository:
        repo: "deb [arch=amd64 signed-by={{ docker_keyring }}] https://download.docker.com/linux/ubuntu {{ ansible_distribution_release }} stable"
        state: present
        filename: docker

    - name: Update apt cache after Docker repo
      apt:
        update_cache: yes

    - name: Install Docker Engine & plugins
      apt:
        name:
          - docker-ce
          - docker-ce-cli
          - containerd.io
          - docker-buildx-plugin
          - docker-compose-plugin
        state: latest

    - name: Start and enable Docker
      systemd:
        name: docker
        state: started
        enabled: yes

    - name: Add ubuntu user to docker group
      user:
        name: ubuntu
        groups: docker
        append: yes

    # -----------------------------
    # JAVA INSTALLATION
    # -----------------------------
    - name: Install Java and fontconfig
      apt:
        name:
          - fontconfig
          - openjdk-21-jre
        state: present

    # -----------------------------
    # JENKINS INSTALLATION
    # -----------------------------
    - name: Download Jenkins GPG key
      get_url:
        url: https://pkg.jenkins.io/debian-stable/jenkins.io-2026.key
        dest: "{{ jenkins_keyring }}"
        mode: '0644'

    - name: Add Jenkins repository
      apt_repository:
        repo: "deb [signed-by={{ jenkins_keyring }}] https://pkg.jenkins.io/debian-stable binary/"
        state: present
        filename: jenkins

    - name: Update apt cache after Jenkins repo
      apt:
        update_cache: yes

    - name: Install Jenkins
      apt:
        name: jenkins
        state: present

    - name: Enable and start Jenkins
      systemd:
        name: jenkins
        state: started
        enabled: yes

    # -----------------------------
    # PERMISSIONS & RESTARTS
    # -----------------------------
    - name: Add jenkins user to docker group
      user:
        name: jenkins
        groups: docker
        append: yes

    - name: Restart Docker
      systemd:
        name: docker
        state: restarted

    - name: Restart Jenkins
      systemd:
        name: jenkins
        state: restarted

    # -----------------------------
    # CLEANUP
    # -----------------------------
    - name: Remove temporary files
      file:
        path: "{{ item }}"
        state: absent
      loop:
        - /tmp/docker.asc

# -----------------------------
# AWS CLI INSTALLATION (your steps converted)
# -----------------------------

    - name: Install unzip dependency
      apt:
        name: unzip
        state: present
        update_cache: yes

    - name: Download AWS CLI v2 zip
      get_url:
        url: https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip
        dest: /tmp/awscliv2.zip

    - name: Extract AWS CLI zip
      unarchive:
        src: /tmp/awscliv2.zip
        dest: /tmp/
        remote_src: yes

    - name: Install AWS CLI v2
      command: >
        /tmp/aws/install -i /usr/local/aws-cli -b /usr/local/bin --update
      args:
        creates: /usr/local/bin/aws

    - name: Verify AWS CLI installation
      command: aws --version
      register: aws_output
      changed_when: false

    - debug:
        var: aws_output.stdout


    

    # -----------------------------
    # CLEANUP
    # -----------------------------
    - name: Remove AWS CLI temp files
      file:
        path: "{{ item }}"
        state: absent
      loop:
        - /tmp/aws
        - /tmp/awscliv2.zip

# -----------------------------
# KUBECTL INSTALLATION
# -----------------------------

    - name: Download kubectl binary
      get_url:
        url: https://amazon-eks.s3.us-west-2.amazonaws.com/1.19.6/2021-01-05/bin/linux/amd64/kubectl
        dest: /tmp/kubectl
        mode: '0755'

    - name: Move kubectl to /usr/local/bin
      command: mv /tmp/kubectl /usr/local/bin/kubectl
      args:
        creates: /usr/local/bin/kubectl

    - name: Verify kubectl installation
      command: kubectl version --client --short
      register: kubectl_output
      changed_when: false

    - debug:
        var: kubectl_output.stdout

# -----------------------------
# EKSCTL INSTALLATION
# -----------------------------

    - name: Download eksctl tar.gz
      get_url:
        url: https://github.com/weaveworks/eksctl/releases/latest/download/eksctl_Linux_amd64.tar.gz
        dest: /tmp/eksctl.tar.gz

    - name: Extract eksctl binary
      unarchive:
        src: /tmp/eksctl.tar.gz
        dest: /tmp/
        remote_src: yes

    - name: Move eksctl to /usr/local/bin
      command: mv /tmp/eksctl /usr/local/bin/eksctl
      args:
        creates: /usr/local/bin/eksctl

    - name: Verify eksctl installation
      command: eksctl version
      register: eksctl_output
      changed_when: false

    - debug:
        var: eksctl_output.stdout

    # -----------------------------
    # CLEANUP
    # -----------------------------
    - name: Remove eksctl temp files
      file:
        path: "{{ item }}"
        state: absent
      loop:
        - /tmp/eksctl
        - /tmp/eksctl.tar.gz

    # -----------------------------
    # TRIVY INSTALLATION
    # -----------------------------

    - name: Remove old Trivy repo (if exists)
      file:
        path: /etc/apt/sources.list.d/trivy.list
        state: absent

    - name: Remove old Trivy keyring
      file:
        path: /usr/share/keyrings/trivy.gpg
        state: absent

    - name: Download Trivy GPG key (ASCII)
      get_url:
        url: https://aquasecurity.github.io/trivy-repo/deb/public.key
        dest: /tmp/trivy.asc

    - name: Convert Trivy key to GPG (IMPORTANT)
      command: >
        gpg --dearmor -o /usr/share/keyrings/trivy.gpg /tmp/trivy.asc
      args:
        creates: /usr/share/keyrings/trivy.gpg

    - name: Add Trivy repository
      apt_repository:
        repo: "deb [signed-by=/usr/share/keyrings/trivy.gpg] https://aquasecurity.github.io/trivy-repo/deb {{ ansible_distribution_release }} main"
        state: present
        filename: trivy

    - name: Update apt cache
      apt:
        update_cache: yes

    - name: Install Trivy
      apt:
        name: trivy
        state: present



Connecting ec2 instance from local ubuntu terminal
If using windows pc than install Ubuntu terminal from internet


<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/425d7f9c-b039-493c-96dd-7870e2632bc2" />

Open ubuntu terminal  
Go to terraform folder
cd /mnt/c/Users/Admin/Desktop/herovired/Hero-capstone-project/terraform

copy capstone-user-key.pem to ~/ location (home location)
cp capstone-user-key.pem ~/

change the permission
chmod 400 ~/capstone-user-key.pem

go to ansible folder
cd /mnt/c/Users/Admin/Desktop/herovired/Hero-capstone-project/ansible

check for the connectivity
ansible ubuntu_servers -i hosts.ini -m ping

run basic-setup.yml file using below command in ubuntu terminal
ansible-playbook -i hosts.ini basic-setup.yml



output:
saiyedin786@DESKTOP-43VHE2R:/mnt/c/Users/Admin/Desktop/herovired/Hero-capstone-project/ansible$ ansible ubuntu_servers -i hosts.ini -m ping
jenkinsmaster | SUCCESS => {
    "ansible_facts": {
        "discovered_interpreter_python": "/usr/bin/python3"
    },
    "changed": false,
    "ping": "pong"
}
saiyedin786@DESKTOP-43VHE2R:/mnt/c/Users/Admin/Desktop/herovired/Hero-capstone-project/ansible$ ansible-playbook -i hosts.ini basic-setup.yml

PLAY [Setup Docker, Docker Compose v2 and Jenkins on Ubuntu 24] ********************************************************************************************************
TASK [Gathering Facts] *************************************************************************************************************************************************ok: [jenkinsmaster]

TASK [Update apt cache] ************************************************************************************************************************************************changed: [jenkinsmaster]

TASK [Install required packages] ***************************************************************************************************************************************ok: [jenkinsmaster]

TASK [Ensure keyrings directory exists] ********************************************************************************************************************************ok: [jenkinsmaster]

TASK [Download Docker GPG key] *****************************************************************************************************************************************changed: [jenkinsmaster]

TASK [Convert Docker GPG key] ******************************************************************************************************************************************changed: [jenkinsmaster]

TASK [Add Docker repository] *******************************************************************************************************************************************changed: [jenkinsmaster]

TASK [Update apt cache after Docker repo] ******************************************************************************************************************************changed: [jenkinsmaster]

TASK [Install Docker Engine & plugins] *********************************************************************************************************************************changed: [jenkinsmaster]

TASK [Start and enable Docker] *****************************************************************************************************************************************ok: [jenkinsmaster]

TASK [Add ubuntu user to docker group] *********************************************************************************************************************************changed: [jenkinsmaster]

TASK [Install Java and fontconfig] *************************************************************************************************************************************changed: [jenkinsmaster]

TASK [Download Jenkins GPG key] ****************************************************************************************************************************************changed: [jenkinsmaster]

TASK [Add Jenkins repository] ******************************************************************************************************************************************changed: [jenkinsmaster]

TASK [Update apt cache after Jenkins repo] *****************************************************************************************************************************changed: [jenkinsmaster]

TASK [Install Jenkins] *************************************************************************************************************************************************changed: [jenkinsmaster]

TASK [Enable and start Jenkins] ****************************************************************************************************************************************ok: [jenkinsmaster]

TASK [Add jenkins user to docker group] ********************************************************************************************************************************changed: [jenkinsmaster]

TASK [Restart Docker] **************************************************************************************************************************************************changed: [jenkinsmaster]

TASK [Restart Jenkins] *************************************************************************************************************************************************changed: [jenkinsmaster]

TASK [Remove temporary files] ******************************************************************************************************************************************changed: [jenkinsmaster] => (item=/tmp/docker.asc)

TASK [Install unzip dependency] ****************************************************************************************************************************************changed: [jenkinsmaster]

TASK [Download AWS CLI v2 zip] *****************************************************************************************************************************************changed: [jenkinsmaster]

TASK [Extract AWS CLI zip] *********************************************************************************************************************************************changed: [jenkinsmaster]

TASK [Install AWS CLI v2] **********************************************************************************************************************************************changed: [jenkinsmaster]

TASK [Verify AWS CLI installation] *************************************************************************************************************************************ok: [jenkinsmaster]

TASK [debug] ***********************************************************************************************************************************************************ok: [jenkinsmaster] => {
    "aws_output.stdout": "aws-cli/2.34.63 Python/3.14.5 Linux/7.0.0-1004-aws exe/x86_64.ubuntu.26"
}

TASK [Remove AWS CLI temp files] ***************************************************************************************************************************************changed: [jenkinsmaster] => (item=/tmp/aws)
changed: [jenkinsmaster] => (item=/tmp/awscliv2.zip)

TASK [Download kubectl binary] *****************************************************************************************************************************************changed: [jenkinsmaster]

TASK [Move kubectl to /usr/local/bin] **********************************************************************************************************************************changed: [jenkinsmaster]

TASK [Verify kubectl installation] *************************************************************************************************************************************ok: [jenkinsmaster]

TASK [debug] ***********************************************************************************************************************************************************ok: [jenkinsmaster] => {
    "kubectl_output.stdout": "Client Version: v1.19.6-eks-49a6c0"
}

TASK [Download eksctl tar.gz] ******************************************************************************************************************************************changed: [jenkinsmaster]

TASK [Extract eksctl binary] *******************************************************************************************************************************************changed: [jenkinsmaster]

TASK [Move eksctl to /usr/local/bin] ***********************************************************************************************************************************changed: [jenkinsmaster]

TASK [Verify eksctl installation] **************************************************************************************************************************************ok: [jenkinsmaster]

TASK [debug] ***********************************************************************************************************************************************************ok: [jenkinsmaster] => {
    "eksctl_output.stdout": "0.227.0"
}

TASK [Remove eksctl temp files] ****************************************************************************************************************************************ok: [jenkinsmaster] => (item=/tmp/eksctl)
changed: [jenkinsmaster] => (item=/tmp/eksctl.tar.gz)

TASK [Remove old Trivy repo (if exists)] *******************************************************************************************************************************ok: [jenkinsmaster]

TASK [Remove old Trivy keyring] ****************************************************************************************************************************************ok: [jenkinsmaster]

TASK [Download Trivy GPG key (ASCII)] **********************************************************************************************************************************changed: [jenkinsmaster]

TASK [Convert Trivy key to GPG (IMPORTANT)] ****************************************************************************************************************************changed: [jenkinsmaster]

TASK [Add Trivy repository] ********************************************************************************************************************************************changed: [jenkinsmaster]

TASK [Update apt cache] ************************************************************************************************************************************************changed: [jenkinsmaster]

TASK [Install Trivy] ***************************************************************************************************************************************************changed: [jenkinsmaster]

PLAY RECAP *************************************************************************************************************************************************************jenkinsmaster              : ok=45   changed=32   unreachable=0    failed=0    skipped=0    rescued=0    ignored=0

saiyedin786@DESKTOP-43VHE2R:/mnt/c/Users/Admin/Desktop/herovired/Hero-capstone-project/ansible$


<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/c527c5d4-4671-483c-a572-8391eced9347" />

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/eac68a9e-82a3-4245-93f5-dd52d2698b8d" />

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/b925bb1c-1784-45dc-a26c-928503da45f2" />

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/470c2a0e-db1e-4e13-ba47-1244bc373def" />

Verification
-> docker,docker-compose-v2
    docker --version
-> jenkins
   jenkins --version
-> awscli
     aws --version
-> kubectl
   kubectl version --client
-> eksctl
    eksctl version
-> trivy
    trivy –version
    
<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/c17c81c9-c8c0-422b-b3ba-c4013ce2651e" />

Step-4. jenkins setup
ports : 22,80,30000-32767,465,25,3000-10000,

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/2d8cf122-6435-4e39-91b0-56a93d56c94b" />

Open in browser
http://public_ip:8080

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/487bf3ab-15cc-451c-8f24-054bc2618e7f" />

Generate password: username is admin by default

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/559557e9-5b9b-4329-9f24-1cce55cdd30e" />

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/710262fe-b053-4c1b-aaf8-9603f2b4ae54" />

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/3eead453-2693-46ed-9e77-31e21649684f" />

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/1d42f9c7-d934-427e-b2de-30cde601762c" />

Step 5 Pluggin installation
 Go to Jenkins Master 
Manage Jenkins --> Plugins --> Available plugins 
install the below plugins:
   Docker
   Pipeline: Stage View
   OWASP dependency check
   SonarQube Scanner


<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/2ee15fa3-dca7-4275-b8d2-5b693893d38e" />

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/6873a985-d204-4494-83e6-247b142ebe6a" />

Step 6. OWASP setup
install OWASP plugin (already installed in step 5)

jenkins tools- OWASP dependency check

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/2f106c04-88d2-4a1d-837a-ae44b570d2bc" />

Step 7: Jenkins-Github integration
•	Go to Github.com
•	Profile->Settings->developer settings
•	Create new token

<img width="975" height="452" alt="image" src="https://github.com/user-attachments/assets/7998a5e0-6438-4909-8e19-324c5ae579f3" />

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/7437fb20-1764-41f0-8d2e-cdcd4f9973ba" />

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/81e8d05b-4f41-4bd1-9968-444bfd362322" />

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/ac8bdb11-1590-487c-b197-03ada2fb27d2" />

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/4bdfb523-8afa-4696-bdd2-e0e4bfe82213" />

Go to
Manage Jenkins->credentials

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/6afc5f3d-c639-48cf-bc9d-f3aa8c641c94" />

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/ba4ea217-e2be-4123-b5e6-6935ceeac627" />

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/f1681bd7-534f-427a-a84d-9c7e4ae479dd" />


<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/554fc5d1-57e4-42af-8408-3b628f7e8ffc" />

Step-8 Jenkins-DockerHub integration
Go to dockerhub.com and login
Click on Account settings 

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/c349fd54-ea40-46d1-937e-8feabe45c12c" />

Click personal access tokens on left

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/5d909d82-a41a-4554-99db-53ca740351de" />

Click on Generate New token

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/dd33b7f8-78b7-410c-a2f5-61a1d5658029" />

Give some name
And click Generate
Copy new token

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/7d4d0df0-513d-43c0-8c4e-8e03fb00704f" />

Go to Jenkins-> manage Jenkins->credentials
Click on credentials
<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/ab8cd4f8-efd7-486e-8e21-be2d9b957baa" />

Click on Add credentials

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/c23d8642-6542-435b-b2a0-b0202554e950" />

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/c44028d2-b373-4671-8068-f979b0010161" />

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/5987f719-a0b8-4332-a119-61ade2ce22cf" />

Step 9: Sonarqube setup

install SonarQube Scanner

 sudo docker run -itd --name SonarQube-Server -p 9000:9000 sonarqube:lts-community
 
open in browser

   http://public_ip:9000

generate sonar-token in sonarcube portal

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/9f4d12f0-90d4-4d23-8255-0d19d4015d16" />

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/752e69ee-5bb5-4935-8cc1-ac790b731c71" />

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/f43b53fc-210e-4b93-bed4-86dbfc207630" />

Jenkins->manage Jenkins->tools

Look for Sonarqube scanner and fill detail as below and save

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/fcd52687-e106-4ee6-a5d4-882648119867" />

Go to sonarqube server->administration->security->users

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/0d71e473-238d-4da3-be8f-c60e83732fc0" />

Click on update tokens

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/65122b23-2476-4db8-8280-95fbd0583d73" />

Give name and then generate token and then copy it

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/260f09ed-ec36-424c-b30c-f45691a10dfb" />

Now Go to

Manage jenkins->credentials

Click on Credentials

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/9a5f6262-c91a-40dd-9821-06eaab894203" />

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/339a1ee9-b80f-4c26-9f15-62132495309d" />

Manage jenkins->system

Look for sonarqube installations fill as below and then save

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/f6f53c9d-6d43-4375-906c-8a76e007a548" />

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/e3888e9f-b4a4-4a9c-be04-1a83114458bb" />

Now go sonarqube server

Administration->configuration->webhooks

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/69818266-7c45-44c2-909d-43c1743aa96d" />

Click on create

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/53762153-b9fc-40cc-9ca2-7d564f86d875" />

Fill as shown

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/e42a0d85-913a-4ff3-aa0e-b1c136836241" />

Click create

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/4ce6b61a-b012-472e-a7db-697e20b3483b" />


Step:10 Email-setup
Go to gmail.com
Profile-> manage account

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/63e183e6-1dd6-4d08-80f9-cbc9f60c8bcc" />

Click security and signin in left

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/28d0147e-19c7-4b69-b020-8e9ee09682b7" />

Search app password in searchbox and click

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/8be8a393-5f0e-4f9e-a8a4-39951e2e5f76" />

Give some name and create

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/401ac6b1-e966-40fe-848c-866229474a6c" />

Go to Manage jenkins->credentials

Click credentials

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/a51f4a62-e1ea-448f-8edb-70b646c0e971" />


<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/72f0eab5-4cfd-4dd4-8e77-a8b3a28734b5" />

Manage-jenkins->system click system


<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/e33fd79b-cfba-477d-9aff-7030b99cc9a6" />

Fill as below

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/dde24740-f7b0-4889-8af2-8b0a4f188506" />

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/d96494aa-8c18-45d4-8cc9-5878c9aff87f" />

Check for test email in gmail inbox


<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/b57fea70-b418-4804-a026-beedd305582a" />

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/2fd99b9c-2a9b-42b3-8156-91a22ceac338" />

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/737de889-8916-4025-bf55-dae4168fe9f6" />

Step-11 eks cluster setup (manual)
Create EKS Cluster (Master machine)

-->create iam role

12.  Go to:
👉 AWS Console → IAM → Roles → Create Role

Trusted entity: EC2
Attach policies:
AmazonEKSClusterPolicy
AmazonEKSWorkerNodePolicy
AmazonEC2ContainerRegistryReadOnly
AmazonEKS_CNI_Policy
administratoraccess

Name:
eksctl-ec2-role

Step 2: Attach Role to EC2
Go to EC2 → Instances
Select your instance (jenkinsmaster)

Click:
Actions → Security → Modify IAM role
Attach:
eksctl-ec2-role
Step 3: Verify Role

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/8e741047-16c8-4f72-b029-0b595013c138" />

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/431a5e60-5a59-4ab7-97c7-e55e86c5898d" />

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/1992750b-a556-4a4a-8241-f3f9ffc5d868" />

-->create cluster
eksctl create cluster --name=shopnow-cluster --region=ap-south-1 --version=1.30 --without-nodegroup

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/9e49701c-e358-4d5d-a5c7-efca61c13982" />

aws eks list-clusters --region ap-south-1

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/b4f52001-d1fd-4f2f-95b5-1307f32f0199" />


-->make eks-nodegroup-key keypair

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/d1c06406-c10b-4cab-9c85-07952ac83e6c" />

-->Associate IAM OIDC Provider (Master machine)
eksctl utils associate-iam-oidc-provider \
  --region ap-south-1 \
  --cluster shopnow-cluster \
  --approve

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/34ca2376-9443-47e4-aa85-c2ed2b887e38" />

-->Create Nodegroup (Master machine)
eksctl create nodegroup --cluster=shopnow-cluster \
                     --region=ap-south-1 \
                     --name=shopnow \
                     --node-type=t2.large \
                     --nodes=2 \
                     --nodes-min=2 \
                     --nodes-max=2 \
                     --node-volume-size=29 \
                     --ssh-access \
                     --ssh-public-key=eks-nodegroup-key

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/a19509c6-c49b-4c50-82f9-91ef33ba69bc" />

kubectl get nodes

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/bf2b0001-5a5d-46fe-a842-e59b99a7105d" />


Step 12 Argocd setup

kubectl create namespace argocd

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/d710c684-8d38-48f7-8549-12bbee93273a" />

kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/dd0ffc0d-d894-4d97-a82a-723e160b7582" />

kubectl get pods -n argocd

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/5f0345f1-805e-4ce7-9198-d190e9e2fa2d" />

sudo curl --silent --location -o /usr/local/bin/argocd https://github.com/argoproj/argo-cd/releases/download/v2.4.7/argocd-linux-amd64

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/0b1151a9-b72c-46e8-ad1d-68848fd07586" />


sudo chmod +x /usr/local/bin/argocd

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/996725c5-c74d-4388-9644-668f858a9180" />

kubectl get svc -n argocd

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/8d9b685c-cc7d-477c-93eb-cf674e9078c1" />


kubectl patch svc argocd-server -n argocd -p '{"spec": {"type": "NodePort"}}'

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/fb5a2053-9a82-4cb6-bd48-d3bac69d6e85" />

kubectl get svc -n argocd

allow port in security group of node 

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/5fb0fa7b-7f27-4d82-850d-5fd214e033ee" />

Access it on browser, click on advance and proceed with
<public-ip-worker>:<port>
<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/c6392de9-6090-4692-a62e-877d56da4431" />

Fetch the initial password of argocd server

kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 -d; echo
<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/3e902f4a-6581-4a82-8420-3ebff6f0a53c" />

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/9eb7dc4b-5af3-434e-9fab-4727c13321d6" />

Username: admin
Now, go to User Info and update your argocd password

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/4de78d90-c9aa-4c20-987c-c5dc723548d2" />

add github repo in settings repositories

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/1100eb27-9eea-4364-88dc-84abf499e90d" />

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/1c5f4b3a-366d-4b2f-8762-d436f2ec1f18" />

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/a2f833f0-517c-4758-99f8-c5bbf44a0d85" />


adding clusters in argocd
argocd login 52.66.204.159:30424 --username admin

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/c4ee3267-fc6c-4887-8d19-29688d5bb80d" />

argocd cluster list
<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/ed5ac555-b968-4ea3-90e5-e33e0c00d719" />

kubectl config get-contexts
<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/04ca27ea-fcc8-4cc8-ab43-6af6aa173210" />

argocd cluster add i-0560ef021d79e121d@shopnow-cluster.ap-south-1.eksctl.io --name shopnow-eks-cluster

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/c53a6ae3-f478-4a57-8f64-8d2a821205d9" />
<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/9f6876d2-6fa8-469d-aafe-48de3693761b" />

Step 13 installation of nginx controller
Install ingress-nginx controller (for external access)
# For EKS, other cloud provider will have different file
kubectl apply -f https://raw.githubusercontent.com/kubernetes/ingress-nginx/controller-v1.12.0-beta.0/deploy/static/provider/aws/deploy.yaml

# For local development (minikube/kind/Docker Desktop)
kubectl apply -f https://raw.githubusercontent.com/kubernetes/ingress-nginx/controller-v1.8.1/deploy/static/provider/kind/deploy.yaml

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/80c1c48c-56e5-44b1-81d8-1e069e5cb4be" />

•	kubectl get pods -n kube-system

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/4d027145-24c7-451b-84bb-627222b7108e" />

•	kubectl get pods -n ingress-nginx

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/5ff730c4-408b-41db-bf40-71ec5aa2ff41" />

•	kubectl top nodes  # Should work after metrics server is running

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/0950ab65-7c77-4dcd-bd5b-40b3b85b327f" />

•	kubectl top pods  # Should work after metrics server is running

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/557c0b93-2037-49a4-a930-30ab4401f59c" />

kubectl create namespace shopnow-demo

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/2cb4d661-b7f9-40e2-85f4-20121e319fdc" />

ArgoCD GitOps
Git clone https://github.com/saiyedin786/Hero-capstone-project.git

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/740eb76f-9bdc-4951-a427-22b7f940b9b3" />

Go to Hero-capstone-project/kubrnetes/argocd
# Deploy applications
kubectl apply -f kubernetes/argocd/umbrella-application.yaml
<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/a01ef6a1-06b2-422e-b230-29e73d2894bf" />

kubectl get applications -n argocd

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/33fa40b3-4c87-4a11-a506-ac1f55add2d4" />
 
kubectl get pods -n shopnow-demo
<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/44814506-47db-4b58-b36f-4b26034e83ed" />


User creation in mongodb
•	# Run below commands
•	use admin;
•	db.createUser({
•	  user: 'shopuser',
•	  pwd: 'ShopNowPass123',
•	  roles: [
•	    { role: 'readWrite', db: 'shopnow' },
•	    { role: 'dbAdmin', db: 'shopnow' }
•	  ]
•	});
•	exit


<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/3e77e07f-7d47-4da3-bc20-3308480e2d51" />

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/7a68e6d3-75f2-452c-9a8d-208d22421a73" />

# Restart backend deployment
kubectl rollout restart deploy backend -n shopnow-demo

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/91dd62fd-1e08-4f7f-bc72-da47792998dd" />

kubectl get pods -n shopnow-demo

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/474497c1-02c1-4bad-9b6e-b8f98bf192c4" />


kubectl get deploy -n shopnow-demo
<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/cd272bef-dd45-493f-bb43-ce3fb6d30ae7" />

kubectl get svc -n shopnow-demo

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/bb93d247-70df-4bab-b547-30992714613e" />
 
kubectl get statefulsets -n shopnow-demo
<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/f9ae6d4b-1d02-4f9e-a2bf-1eb03e9b2509" />

kubectl get hpa -n shopnow-demo

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/6353d748-c8a9-42e7-844e-afe686524523" />

kubectl get cm -n shopnow-demo

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/fe260485-4f4d-4b3f-9fbd-5851525f2591" />

kubectl get secrets -n shopnow-demo

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/0ce5660c-e07d-4905-b9d0-6837b6a62b7b" />

kubectl get ing -n shopnow-demo

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/3626f679-0d88-4956-b04f-46006682d86b" />

Step 14: Monitoring using Prometheus and graffana
Install Helm Chart
curl -fsSL -o get_helm.sh https://raw.githubusercontent.com/helm/helm/main/scripts/get-helm-3


chmod 700 get_helm.sh
./get_helm.sh

Add Helm Stable Charts for Your Local Client
helm repo add stable https://charts.helm.sh/stable

Add Prometheus Helm Repository
helm repo add prometheus-community https://prometheus-community.github.io/helm-charts

Create Prometheus Namespace
kubectl create namespace prometheus
kubectl get ns
Install Prometheus using Helm
helm install stable prometheus-community/kube-prometheus-stack -n Prometheus

Verify prometheus installation
kubectl get pods -n Prometheus

Check the services file (svc) of the Prometheus
kubectl get svc -n Prometheus

Expose Prometheus and Grafana to the external world through Node Port
Important

change it from Cluster IP to NodePort after changing make sure you save the file and open the assigned nodeport to the service.

kubectl edit svc stable-kube-prometheus-sta-

Verify service
kubectl get svc -n Prometheus

Now,let’s change the SVC file of the Grafana and expose it to the outer world
kubectl edit svc stable-grafana -n prometheus

Check grafana service
kubectl get svc -n prometheus
Get a password for grafana
kubectl get secret --namespace prometheus stable-grafana -o jsonpath="{.data.admin-password}" | base64 --decode ; echo
Note

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/598e71f4-c70c-4f67-81dd-e9ba36dc1c60" />

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/80f15834-f2f5-4993-af1f-985ad77a5db0" />

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/c9ad5cb1-f68b-4e9e-b15c-d459df4fcef4" />

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/f999b309-3509-4623-9bfb-1d0783f09023" />

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/c820fa74-0b53-456a-9ac4-ddb1c848bbda" />

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/6fdcd02c-e05c-4a19-9d5b-aa86cc5dd865" />
<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/9198f752-884e-41ad-b6ef-9def913227a3" />
<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/cab13903-7e53-4232-b699-674a0b8023f4" />

Username: admin

http://52.66.204.159:30780/query
<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/119f781c-a5a1-485b-bf5e-3f6d78ffcbd2" />

http://52.66.204.159:30727/login

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/cc354ff2-b516-48d3-9307-b1a577b63e6a" />

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/7382fcc0-f74b-40c1-a08f-bc6867988984" />
<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/5c5266ba-5c56-4381-b53f-9e30835c2018" />

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/97399c5e-e766-4827-9a8d-835032c76c8c" />

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/36573059-c0c8-441f-973d-b77007102243" />

Step : 15 : shared Library setup
Shared library github repo: 
https://github.com/saiyedin786/Jenkins_SharedLib.git
Go to manage Jenkins->system
<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/8eb4babf-d3d2-42a9-b8fa-b0553019d622" />


Look for Global Trusted Pipeline Libraries
Fill as given below
<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/e7776ed7-45b8-483a-bc25-c0b350969256" />

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/f0de7920-eb96-452a-a22e-e9cb3352284b" />

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/cc2b9e36-cfc5-4102-b694-12b4627d6314" />


Save

Now usage of shared library
Insert @Library('Shared') _ at the beginning of pipeline








Creating a jenkins job-  capstone-CI
capstone-CI

@Library('Shared') _
pipeline {
    agent any
    
    environment{
        SONAR_HOME = tool "Sonar"
    }
    
    parameters {
        string(name: 'ADMIN_DOCKER_TAG', defaultValue: '', description: 'Setting docker image for latest push')
        string(name: 'FRONTEND_DOCKER_TAG', defaultValue: '', description: 'Setting docker image for latest push')
        string(name: 'BACKEND_DOCKER_TAG', defaultValue: '', description: 'Setting docker image for latest push')
    }
    
    stages {
        stage("Validate Parameters") {
            steps {
                script {
                    if (params.FRONTEND_DOCKER_TAG == '' || params.BACKEND_DOCKER_TAG == '' || params.ADMIN_DOCKER_TAG == '') {
                        error("ADMIN_DOCKER_TAG, FRONTEND_DOCKER_TAG and BACKEND_DOCKER_TAG must be provided.")
                    }
                }
            }
        }
        stage("Workspace cleanup"){
            steps{
                script{
                    cleanWs()
                }
            }
        }
        
        stage('Git: Code Checkout') {
            steps {
                script{
                    code_checkout("https://github.com/saiyedin786/Hero-capstone-project.git","main")
                }
            }
        }
        
        stage("Trivy: Filesystem scan"){
            steps{
                script{
                    trivy_scan()
                }
            }
        }

stage("OWASP: Dependency check"){
            steps{
                script{
                    owasp_dependency()
                }
            }
        }

 
        
        stage("SonarQube: Code Analysis"){
            steps{
                script{
                    sonarqube_analysis("Sonar", "Hero-Capstone-Project", "hero-capstone-project")
                }
            }
        }
        
        stage("SonarQube: Code Quality Gates"){
            steps{
                script{
                    sonarqube_code_quality()
                }
            }
        }
             
            
        
        
        stage("Docker: Build Images"){
            steps{
                script{
                        dir('admin'){
                            docker_build("shopnow-admin","${params.ADMIN_DOCKER_TAG}","saiyedin786")
                        }
                    
                        dir('backend'){
                            docker_build("shopnow-backend","${params.BACKEND_DOCKER_TAG}","saiyedin786")
                        }
                    
                        dir('frontend'){
                            docker_build("shopnow-frontend","${params.FRONTEND_DOCKER_TAG}","saiyedin786")
                        }
                }
            }
        }
        
        stage("Docker: Push to DockerHub"){
            steps{
                script{
                    docker_push("shopnow-admin","${params.ADMIN_DOCKER_TAG}","saiyedin786") 
                    docker_push("shopnow-backend","${params.BACKEND_DOCKER_TAG}","saiyedin786")
                    docker_push("shopnow-frontend","${params.FRONTEND_DOCKER_TAG}","saiyedin786")
                }
            }
        }
    }
    post{
        success{
        
           build job: "capstone-CD",
	   wait: true,
           propagate: false,
           parameters: [
           string(name: 'ADMIN_DOCKER_TAG', value: "${params.ADMIN_DOCKER_TAG}"),
           string(name: 'FRONTEND_DOCKER_TAG', value: "${params.FRONTEND_DOCKER_TAG}"),
           string(name: 'BACKEND_DOCKER_TAG', value: "${params.BACKEND_DOCKER_TAG}")
           ]
        }
    }
}

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/fd573bde-a38d-4520-b4dc-31124d915096" />


Also create another Jenkins job – capstone-CD
capstone-CD
@Library('Shared') _
pipeline {
    agent any
    
    parameters {
        string(name: 'ADMIN_DOCKER_TAG', defaultValue: '', description: 'Admin Docker tag of the image built by the CI job')
        string(name: 'FRONTEND_DOCKER_TAG', defaultValue: '', description: 'Frontend Docker tag of the image built by the CI job')
        string(name: 'BACKEND_DOCKER_TAG', defaultValue: '', description: 'Backend Docker tag of the image built by the CI job')
    }

    stages {
        stage("Workspace cleanup"){
            steps{
                script{
                    cleanWs()
                }
            }
        }
        
        stage('Git: Code Checkout') {
            steps {
                script{
                    code_checkout("https://github.com/saiyedin786/Hero-capstone-project.git","main")
                }
            }
        }
        
        stage('Verify: Docker Image Tags') {
            steps {
                script{
                    echo "ADMIN_DOCKER_TAG: ${params.ADMIN_DOCKER_TAG}"
                    echo "FRONTEND_DOCKER_TAG: ${params.FRONTEND_DOCKER_TAG}"
                    echo "BACKEND_DOCKER_TAG: ${params.BACKEND_DOCKER_TAG}"
                }
            }
        }
        
        
      stage("Update: Helm values.yaml files") {
    steps {
        script {

            dir('kubernetes/helm/charts/admin') {
                sh """
                    sed -i "s/^[[:space:]]*tag:.*/  tag: ${params.ADMIN_DOCKER_TAG}/" values.yaml
                """
            }

            dir('kubernetes/helm/charts/backend') {
                sh """
                    sed -i "s/^[[:space:]]*tag:.*/  tag: ${params.BACKEND_DOCKER_TAG}/" values.yaml
                """
            }

            dir('kubernetes/helm/charts/frontend') {
                sh """
                    sed -i "s/^[[:space:]]*tag:.*/  tag: ${params.FRONTEND_DOCKER_TAG}/" values.yaml
                """
            }
        }
    }
}
        
        stage("Git: Code update and push to GitHub"){
            steps{
                script{
                    withCredentials([gitUsernamePassword(credentialsId: 'Github-cred', gitToolName: 'Default')]) {
                        sh '''
                        echo "Checking repository status: "
                        git status
                    
                        echo "Adding changes to git: "
                        git add .
                        
                        echo "Commiting changes: "
                        git commit -m "Updated environment variables"
                        
                        echo "Pushing changes to github: "
                        git push https://github.com/saiyedin786/Hero-capstone-project.git main
                    '''
                    }
                }
            }
        }
    }
  post {
        success {
            script {
                emailext attachLog: true,
                from: 'saiyedin786@gmail.com',
                subject: "Shopnow Application has been updated and deployed - '${currentBuild.result}'",
                body: """
                    <html>
                    <body>
                        <div style="background-color: #FFA07A; padding: 10px; margin-bottom: 10px;">
                            <p style="color: black; font-weight: bold;">Project: ${env.JOB_NAME}</p>
                        </div>
                        <div style="background-color: #90EE90; padding: 10px; margin-bottom: 10px;">
                            <p style="color: black; font-weight: bold;">Build Number: ${env.BUILD_NUMBER}</p>
                        </div>
                        <div style="background-color: #87CEEB; padding: 10px; margin-bottom: 10px;">
                            <p style="color: black; font-weight: bold;">URL: ${env.BUILD_URL}</p>
                        </div>
                    </body>
                    </html>
            """,
            to: 'saiyedin786@gmail.com',
            mimeType: 'text/html'
            }
        }
      failure {
            script {
                emailext attachLog: true,
                from: 'saiyedin786@gmail.com',
                subject: "Shopnow Application build failed - '${currentBuild.result}'",
                body: """
                    <html>
                    <body>
                        <div style="background-color: #FFA07A; padding: 10px; margin-bottom: 10px;">
                            <p style="color: black; font-weight: bold;">Project: ${env.JOB_NAME}</p>
                        </div>
                        <div style="background-color: #90EE90; padding: 10px; margin-bottom: 10px;">
                            <p style="color: black; font-weight: bold;">Build Number: ${env.BUILD_NUMBER}</p>
                        </div>
                    </body>
                    </html>
            """,
            to: 'saiyedin786@gmail.com',
            mimeType: 'text/html'
            }
        }
    }
}

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/b97353d7-14f7-478b-8516-2135a02eadd5" />

Running Capstone-CI job in Jenkins

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/926e5cbf-07ea-4b94-85db-05d2ec651d8f" />

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/ce36a24e-a831-43bf-b2fc-2e23446cef8f" />

Capstone-CI will automatically trigger capstone-CD

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/f4333d74-ddc7-49df-a0af-191dfc2343c5" />

Image updated in dockerhub.com repo by capstone-CI Jenkins job

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/e8895b3c-e56e-4b0b-9d5b-10a878c99c5f" />

Version updated automatically in github repo at
kubernetes/helm/charts/admin/values.yaml and frontend,backend etc by capstone-CD Jenkins job
<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/baac8bff-7bb4-4bf9-b5fc-8e8b7e6089f9" />

Then argocd will pull the code from github repo and deploy into eks cluster

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/e1071146-65fe-4eca-8ccf-63c8357d20bc" />

Shopnow app frontend will be available at 
http://ac28051b6575f4e289fde2dc87abb669-9807b455609f8957.elb.ap-south-1.amazonaws.com/ismail

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/391138d8-fdfa-4ae1-bdb9-72785981589d" />

Shopnow app admin will be available at 
http://ac28051b6575f4e289fde2dc87abb669-9807b455609f8957.elb.ap-south-1.amazonaws.com/ismail-admin
<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/0f7c0912-4817-40e9-9800-cd1293eb3165" />


Getting success on gmail
<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/f888c801-7111-4b91-a36e-519195118cb6" />


Delete Using kubectl (Recommended)

First list apps:

kubectl get applications -n argocd

Delete all applications:

kubectl delete applications --all -n argocd

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/6677bf51-494c-48b7-8823-355c2abcbc21" />

delete:
eksctl delete nodegroup \
  --cluster=shopnow-cluster \
  --region=ap-south-1 \
  --name=shopnow
<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/115f8b51-f8a0-45d6-8cf1-8d4f8d533b43" />

eksctl delete cluster \
  --name=shopnow-cluster \
  --region=ap-south-1
<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/c4f5e850-95d1-45b0-8ae2-b2ab8b1d8c3c" />

aws eks list-clusters --region ap-south-1

aws ec2 delete-key-pair \
  --key-name eks-nodegroup-key \
  --region ap-south-1

rm eks-nodegroup-key.pem  (local)

aws iam list-open-id-connect-providers

aws iam delete-open-id-connect-provider \
  --open-id-connect-provider-arn <OIDC_ARN>

aws iam delete-open-id-connect-provider \
  --open-id-connect-provider-arn arn:aws:iam::254292659362:oidc-provider/oidc.eks.ap-south-1.amazonaws.com/id/20BC84A3F1FC691114C361B6F1AFA6AD

Terraform destroy
<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/7d6612f3-b10b-4bba-b4de-f5976c419f75" />

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/4e5a32a4-65b0-4630-99e7-a5631d7770a5" />





































