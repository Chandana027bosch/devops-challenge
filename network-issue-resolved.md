# 🛠️ Kubernetes Networking Issue - Resolution Report

## 🎯 Objective

Investigate and resolve a networking issue in Azure Kubernetes Service (AKS) where application pods are unable to communicate with **external services** (e.g., public APIs, external databases, internet).

---

## ❗ Issue Summary

### 🔍 Problem Statement:
Pods in the AKS cluster are failing to reach external services. This impacts external API calls and outbound internet connectivity (e.g., `curl` to google.com fails).

### 📌 Symptoms Observed:
- `curl` commands inside pods fail with DNS resolution or timeout errors.
- Logs show errors such as:
  - `dial tcp: lookup <host>: no such host`
  - `connection refused`
  - `i/o timeout`
- Application health probes or readiness checks fail.
- No outbound connectivity from within the pods.

---

## 🧪 Investigation Steps

### ✅ Step 1: Verify Pod DNS Resolution

```bash
kubectl exec -it <pod-name> -- nslookup google.com
