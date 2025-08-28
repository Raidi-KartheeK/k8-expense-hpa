# Kubernetes Expense Tracker with HPA

This repository contains a **Kubernetes deployment** of an Expense Tracker application.  
It includes a **frontend**, **backend**, and **MySQL database**, with configurations for **namespace** and **Horizontal Pod Autoscaler (HPA)**.

## 📂 Project Structure

- **backend/** → Backend service (API layer for expense management)
- **frontend/** → Frontend UI for managing expenses
- **mysql/** → MySQL database deployment and persistent storage
- **namespace.yaml** → Custom namespace definition
- **terraform.tfstate** → Terraform state file (infra management)

## 🚀 Features

- **Frontend + Backend** microservices
- **MySQL Database** integration
- **Horizontal Pod Autoscaler (HPA)** for dynamic scaling
- **Namespace isolation** for resource grouping
- Kubernetes-native deployment manifests

## 🛠️ Deployment

1. Create the namespace:

   kubectl apply -f namespace.yaml

2.Deploy MySQL
   kubectl apply -f mysql/

3.Deploy Backend
   kubectl apply -f frontend/


4.Deploy Frontend
   kubectl apply -f frontend/


5.Enable Horizontal Pod Autoscaler
   kubectl autoscale deployment backend --cpu-percent=50 --min=2 --max=5
