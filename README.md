]# EKS Deployment Guide

## 📌 Overview
EKS Deployment Guide provides step-by-step instructions on how to deploy applications on an existing Amazon EKS cluster.

## 🚀 Features
- **Step-by-step Kubernetes deployment on EKS**
- **Example Kubernetes manifests for applications**
- **Ingress and Service configurations**
- **Best practices for deploying workloads**

## 📂 Folder Structure
```
eks-deploy-guide/
├── k8s/         # Kubernetes YAML manifests
├── scripts/     # Helper scripts for automation
├── README.md    # Documentation
```

## 🛠 Prerequisites
- AWS CLI configured (`aws configure`)
- kubectl installed (`kubectl version`)
- EKS cluster already running (`aws eks list-clusters`)

## ⚡ Deployment Steps

### **Step 1: Clone the Repository**
```sh
git clone https://github.com/your-org/eks-deploy-guide.git
cd eks-deploy-guide
```

### **Step 2: Configure kubectl for EKS**
```sh
aws eks update-kubeconfig --name my-eks-cluster --region us-east-1
kubectl get nodes
```

### **Step 3: Deploy Application to EKS**
```sh
kubectl apply -f k8s/deployment.yaml
kubectl apply -f k8s/service.yaml
```

### **Step 4: Verify Deployment**
```sh
kubectl get pods
kubectl get services
```

## 🎯 Usage
- Deploy and manage workloads on Amazon EKS
- Use Ingress to expose applications externally

## 🔄 Cleanup
To remove deployed applications:
```sh
kubectl delete -f k8s/deployment.yaml
kubectl delete -f k8s/service.yaml
```

## 📖 Documentation
For more details, refer to [AWS EKS Docs](https://docs.aws.amazon.com/eks/latest/userguide/) and [Kubernetes Docs](https://kubernetes.io/docs/).

## 📌 License
This project is licensed under the MIT License.

