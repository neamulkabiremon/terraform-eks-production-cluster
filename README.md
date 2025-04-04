# 🚀 Amazon EKS Production-Ready: Secure & Scalable Kubernetes Infrastructure with Terraform & Helm

This project provides a **production-grade Amazon EKS setup** built entirely with **Terraform** and **Helm**, following Infrastructure as Code (IaC) best practices.

> ✅ Designed to solve real-world issues: scalability, security, observability, and automation — all in one robust solution.

---

## 📦 Features Overview

This repository includes modular, step-by-step Terraform scripts that provision a fully functional, secure, and scalable EKS cluster with:

- 🧱 **VPC, Subnets, Routes, NAT & IGW**
- 🔐 **RBAC roles & IAM users**
- ☸️ **EKS Cluster & Node Groups**
- 📈 **Horizontal & Cluster Autoscaler**
- 🕵️ **Metrics Server**
- 🛡️ **ALB & NGINX Ingress with HTTPS**
- 🔐 **Secrets Manager + IRSA via CSI Driver**
- 📦 **Persistent Storage: EBS & EFS (ReadWriteMany)**
- 📄 **OIDC provider & Pod Identity Add-ons**
- 📛 **Cert Manager for TLS Certificates**
- ⚙️ **Custom roles: Developer, Manager, Viewer**
- 🧪 Sample Deployments, Services, StatefulSets

---

## 🗂️ Project Structure

```bash
.
├── 0-locals.tf                            # Local variables
├── 1-providers.tf                         # Terraform providers (AWS, Helm, Kubernetes)
├── 2-vpc.tf                               # VPC setup
├── 3-igw.tf                               # Internet Gateway
├── 4-subnets.tf                           # Public & private subnets
├── 5-nat.tf                               # NAT Gateway
├── 6-routes.tf                            # Routing tables
├── 7-eks.tf                               # EKS cluster definition
├── 8-nodes.tf                             # Managed Node Groups
├── 9-add-developer-user.tf               # IAM role for Developer
├── 10-add-manager-role.tf                # IAM role for Manager
├── 10-statefulset-persistent-storage     # EBS-based StatefulSet example
├── 11-efs-shared-volume-readwritemany    # EFS for RWMany access
├── 11-helm-provider.tf                   # Helm provider block
├── 12-aws-secretsmanager-irsa-csi        # Secrets via IRSA & CSI driver
├── 12-metrics-server.tf                  # Metrics Server deployment
├── 13-pod-identity-addon.tf              # Pod Identity Addon
├── 14-cluster-autoscaler.tf              # Cluster Autoscaler setup
├── 15-aws-lbc.tf                         # AWS Load Balancer Controller
├── 16-nginx-ingress.tf                   # Basic NGINX ingress
├── 17-cert-manager.tf                    # TLS management with Cert Manager
├── 18-ebs-csi-driver.tf                  # EBS CSI storage
├── 19-openid-connect-provider.tf         # OIDC provider for IRSA
├── 20-efs.tf                              # EFS volume setup
├── 21-secrets-store-csi-driver.tf        # Secrets Store CSI Driver
├── 01-rbac-viewer-role                   # Read-only viewer access role
├── 02-clusterrolebinding-admin-access    # Cluster-admin binding
├── 03-myapp-deployment-hpa               # Sample app with HPA
├── 04-deployment-scaled-manual-resources # Deployment with manual resources
├── 05-service-with-aws-loadbalancer      # Service with AWS ALB
├── 06-deployment-with-alb-ingress        # ALB Ingress example
├── 07-https-ingress-alb-ssl              # HTTPS with ALB ingress
├── 08-nginx-ingress-basic                # Simple NGINX ingress setup
├── 09-https-cert-manager-nginx-ingress   # HTTPS via NGINX + Cert Manager
├── iam/                                  # IAM role & policy modules
├── values/                               # Helm chart values
```
## 🛠 Tech Stack**
- AWS EKS
- Terraform
- Helm
- Kubernetes
- AWS ALB & NGINX Ingress
- Secrets Manager + CSI Driver
- EBS & EFS CSI Drivers
- Cert Manager
- OIDC + IRSA
- HPA + Cluster Autoscaler

## 📖 Full Tutorial & Article
📚 Read the full 7-Part Series with detailed explanations, screenshots, and GitHub repo: 

👉 [Amazon EKS Production-Ready Series: Build, Secure & Scale Kubernetes](https://medium.com/@neamulkabiremon/amazon-eks-production-ready-series-build-secure-scale-kubernetes-on-aws-with-terraform-helm-26a263d64cfe)

## 💬 Feedback & Contributions
Have ideas to improve this setup? Or did you implement it successfully?
Feel free to:
- ⭐ Star the repo
- 🛠 Suggest improvements
- 🗨️ Reach out with feedback

🔐 License
This project is open-sourced under the MIT License.

