# Kubernetes NetworkPolicy Example on EKS

This repository contains an example setup to demonstrate **Kubernetes NetworkPolicy** using **AWS VPC CNI**.

## 📌 Overview

# Kubernetes NetworkPolicy Example

In this example, we created 3 deployments:

- **Deployment-1 (nginx-1)** → NetworkPolicy is applied here  
- **Deployment-2 (nginx-2)** → its pods can access pods of `nginx-1`  
- **Deployment-3 (nginx-3)** → its pods **cannot** access pods of `nginx-1`  
