# Kubernetes NetworkPolicy Example on EKS

This repository contains an example setup to demonstrate **Kubernetes NetworkPolicy** using **AWS VPC CNI**.

## 📌 Overview

We deploy three `nginx` applications (`nginx-1`, `nginx-2`, `nginx-3`) and apply a `NetworkPolicy` to restrict access:

- `nginx-1` → Protected pod (policy applied here).
- `nginx-2` → Allowed to connect to `nginx-1` on port 80.
- `nginx-3` → Denied access to `nginx-1`.

## 📂 Repository Contents

- `deployment-1.yaml` → Deployment for `nginx-1`.
- `deployment-2.yaml` → Deployment for `nginx-2`.
- `deployment-3.yaml` → Deployment for `nginx-3`.
- `network-policy.yaml` → NetworkPolicy restricting ingress to `nginx-1`.

## 🚀 Apply the Manifests

```bash
kubectl apply -f deployment-1.yaml
kubectl apply -f deployment-2.yaml
kubectl apply -f deployment-3.yaml
kubectl apply -f network-policy.yaml
