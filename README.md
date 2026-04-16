🚀 EKS 3-Tier Infrastructure (Terraform | AWS | Kubernetes)

This project demonstrates a **production-oriented 3-tier architecture deployed on AWS using Terraform and Amazon EKS**.
It follows a **clean, minimal, and scalable Infrastructure as Code (IaC)** approach suitable for real-world DevOps workflows.

---

## 📦 Project Overview

This repository provisions a complete **Kubernetes-based 3-tier architecture**, including:

* 🌐 VPC (Networking Layer)
* ☸️ EKS Cluster (Container Orchestration)
* 💻 Compute Resources (Worker Nodes)
* 🔐 IAM & Security Configuration

The design focuses on:

* Simplicity (single-layer Terraform structure)
* Scalability (Kubernetes-based workloads)
* Maintainability (clean IaC setup)
* Cloud-native architecture

---

## 🏗️ Architecture Structure

```
EKS_3_tier/
│
├── main.tf          # Core infrastructure (VPC, EKS, resources)
├── variable.tf      # Input variables
├── output.tf        # Outputs (cluster details, endpoints)
├── provider.tf      # AWS provider configuration
└── README.md
```

---

## 🧠 Architecture Breakdown

### 🔹 Core Infrastructure (main.tf)

Handles provisioning of:

* VPC and networking components
* Amazon EKS Cluster
* Node groups (worker nodes)
* Required AWS resources

---

### 🔹 Variables (variable.tf)

Defines configurable inputs such as:

* Region
* Cluster name
* Instance types
* Networking CIDR blocks

---

### 🔹 Outputs (output.tf)

Exports useful values like:

* EKS Cluster Name
* Endpoint URL
* Cluster access details

---

### 🔹 Provider (provider.tf)

Configures AWS provider:

* Region setup
* Authentication via AWS CLI

---

## ☸️ 3-Tier Application Flow

```
Client → Frontend → Backend → Database
```

### 🔸 Frontend Tier

* UI Layer (React / Static App)
* Exposed via LoadBalancer / Ingress

### 🔸 Backend Tier

* API Layer (Node.js / Spring Boot)
* Handles business logic

### 🔸 Database Tier

* External DB (RDS / managed service)
* Secured and isolated

---

## ⚙️ Prerequisites

Ensure the following tools are installed:

* Terraform >= 1.x
* AWS CLI
* kubectl

Configure AWS:

```bash
aws configure
```

---

## 🚀 Deployment Steps

### 1. Initialize Terraform

```bash
terraform init
```

---

### 2. Validate Configuration

```bash
terraform validate
```

---

### 3. Plan Infrastructure

```bash
terraform plan
```

---

### 4. Apply Infrastructure

```bash
terraform apply
```

---

### 5. Configure Kubernetes Access

```bash
aws eks --region ap-south-1 update-kubeconfig --name <cluster-name>
```

---

## 🔐 Security & Best Practices

* IAM roles for EKS access control
* Secure VPC networking
* Separation of application tiers
* Infrastructure managed via code

---

## 📌 DevOps Practices Implemented

* Infrastructure as Code (Terraform)
* Cloud-native architecture (EKS)
* Clean and minimal project structure
* Scalable container-based deployment
* Version-controlled infrastructure

---

## 🧪 Future Enhancements

* Add Kubernetes manifests (Deployments & Services)
* Integrate CI/CD (GitHub Actions / Jenkins)
* Add monitoring (Prometheus + Grafana)
* Logging (CloudWatch / ELK Stack)
* Auto-scaling for workloads

---

## 👨‍💻 Developer Notes

* Always review `terraform plan` before apply
* Avoid hardcoding sensitive values
* Use variables for flexibility
* Keep infrastructure version controlled

---

## 📢 Summary

This project showcases a **real-world DevOps use case** of:

* Deploying Kubernetes (EKS) using Terraform
* Implementing a 3-tier architecture
* Building scalable, production-ready infrastructure

---



