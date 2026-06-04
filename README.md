# ☁️ AWS Cloud Engineering Portfolio

<p align="center">
  <img src="https://img.shields.io/badge/AWS-Cloud_Engineer-FF9900?style=for-the-badge&logo=amazonaws&logoColor=white" />
  <img src="https://img.shields.io/badge/Terraform-IaC-7B42BC?style=for-the-badge&logo=terraform&logoColor=white" />
  <img src="https://img.shields.io/badge/Docker-Containers-2496ED?style=for-the-badge&logo=docker&logoColor=white" />
  <img src="https://img.shields.io/badge/Kubernetes-Orchestration-326CE5?style=for-the-badge&logo=kubernetes&logoColor=white" />
</p>

<p align="center">
  <strong>A collection of intermediate-level AWS projects demonstrating hands-on cloud engineering skills.</strong><br/>
  Each project is designed to showcase real-world architecture patterns used in production environments.
</p>

---

## 📋 Table of Contents

| # | Project | Key Services | Skills Demonstrated |
|---|---------|-------------|---------------------|
| 1 | [Three-Tier Architecture with Terraform](#project-1-three-tier-architecture-with-terraform) | VPC, EC2, ALB, RDS, Auto Scaling | Infrastructure as Code, Network Design, High Availability |
| 2 | [CI/CD Pipeline to Deploy on ECS Fargate](#project-2-cicd-pipeline-to-deploy-on-ecs-fargate) | ECS Fargate, ECR, CodePipeline, CodeBuild, CodeDeploy | Containerization, CI/CD, Blue/Green Deployments |
| 3 | [Deploy An Application with Kubernetes and EKS](#project-3-deploy-an-application-with-kubernetes-and-eks) | EKS, ECR, Load Balancer, CloudWatch | Container Orchestration, Microservices, Auto-Scaling |

---

## Project 1: Three-Tier Architecture with Terraform

**📂 [View Full Guide →](project-1-three-tier-architecture-with-terraform.md)**

### Overview

Deployed a production-ready three-tier web application on AWS using **Terraform** as Infrastructure as Code. The architecture follows AWS Well-Architected best practices with network isolation, high availability, and auto-scaling.

### Architecture

```
Internet → ALB (Public Subnets) → EC2 Auto Scaling (Private Subnets) → RDS MySQL Multi-AZ (Private Subnets)
```

### Key Highlights

- ✅ **Modular Terraform** — Reusable modules for VPC, ALB, ASG, and RDS
- ✅ **Network Isolation** — Three subnet tiers with least-privilege security groups
- ✅ **High Availability** — Multi-AZ deployment for compute and database layers
- ✅ **Auto-Scaling** — CPU-based scaling policies with CloudWatch alarms
- ✅ **Remote State** — S3 backend for team collaboration

### Tech Stack

`Terraform` `Amazon VPC` `EC2` `ALB` `Auto Scaling` `RDS MySQL` `S3` `IAM`

---

## Project 2: CI/CD Pipeline to Deploy on ECS Fargate

**📂 [View Full Guide →](project-2-cicd-pipeline-ecs-fargate.md)**

### Overview

Built a fully automated CI/CD pipeline that containerizes a Node.js application, pushes it to Amazon ECR, and deploys it to **ECS Fargate** using a Blue/Green deployment strategy for zero-downtime releases.

### Architecture

```
GitHub Push → CodePipeline → CodeBuild (Docker Build) → ECR → CodeDeploy (Blue/Green) → ECS Fargate
```

### Key Highlights

- ✅ **Serverless Containers** — Fargate eliminates server management
- ✅ **Multi-Stage Docker Builds** — Optimized, secure production images
- ✅ **Blue/Green Deployments** — Zero-downtime releases with instant rollback
- ✅ **Automated Pipeline** — Code push triggers full build-test-deploy cycle
- ✅ **Centralized Logging** — CloudWatch Logs for container observability

### Tech Stack

`Docker` `Amazon ECS Fargate` `Amazon ECR` `AWS CodePipeline` `AWS CodeBuild` `AWS CodeDeploy` `ALB` `CloudWatch`

---

## Project 3: Deploy An Application with Kubernetes and EKS

**📂 [View Full Guide →](project-3-deploy-app-kubernetes-eks.md)**

### Overview

Deployed a full-stack microservices application on **Amazon EKS** with a React frontend, Node.js backend API, and MongoDB database. Implemented Horizontal Pod Autoscaler for automatic scaling and exposed the application via AWS Load Balancer.

### Architecture

```
Internet → AWS NLB → Frontend (Nginx/React) → Backend (Node.js) → MongoDB (StatefulSet)
                      Pods: 2, HPA: 2-6         Pods: 3, HPA: 2-10    Pods: 1, PVC: 10Gi
```

### Key Highlights

- ✅ **Managed Kubernetes** — EKS cluster with managed node groups
- ✅ **Microservices Architecture** — Separate frontend, backend, and database services
- ✅ **Auto-Scaling** — Horizontal Pod Autoscaler based on CPU/Memory metrics
- ✅ **Persistent Storage** — StatefulSet with PersistentVolumeClaims for MongoDB
- ✅ **Production Patterns** — Health checks, resource limits, ConfigMaps, Secrets

### Tech Stack

`Kubernetes` `Amazon EKS` `Docker` `eksctl` `kubectl` `Helm` `Amazon ECR` `NLB` `CloudWatch`

---

## 🛠️ Skills Demonstrated

| Category | Technologies |
|----------|-------------|
| **Infrastructure as Code** | Terraform (modules, state management, variables) |
| **Containerization** | Docker (multi-stage builds, optimization, security) |
| **Orchestration** | Kubernetes (Deployments, Services, StatefulSets, HPA) |
| **CI/CD** | AWS CodePipeline, CodeBuild, CodeDeploy, Blue/Green |
| **Networking** | VPC design, subnets, security groups, load balancers |
| **Databases** | RDS MySQL (Multi-AZ), MongoDB on Kubernetes |
| **Monitoring** | CloudWatch Logs, Container Insights, health checks |
| **Security** | IAM roles, least-privilege access, encrypted storage, secrets management |

---

## 🚀 Getting Started

Each project contains a complete step-by-step guide. To get started:

1. **Prerequisites**: AWS account, AWS CLI configured, Docker installed
2. **Choose a project** from the table above
3. **Follow the guide** — each includes all code, configurations, and verification steps
4. **Clean up** — each guide ends with resource cleanup to avoid charges

---

## 📫 About Me

I'm a Cloud Engineer passionate about building scalable, resilient infrastructure on AWS. These projects represent hands-on implementations of production-grade architectures.

- 🔭 Currently focusing on: AWS, Terraform, Kubernetes, CI/CD
- 🌱 Preparing for: AWS Solutions Architect / DevOps Engineer certifications
- 💬 Open to: Cloud Engineer, DevOps Engineer, and Platform Engineer roles

---

<p align="center">
  <em>⭐ If you find these projects helpful, please consider giving a star!</em>
</p>
