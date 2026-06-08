# 📊 Prometheus + Grafana Setup on AWS EKS
### 🎯 This guide explains how to install Prometheus and Grafana on an AWS EKS Cluster using Helm.

## 🚀 Architecture
```hcl
AWS EKS Cluster
│
├── 📈 Prometheus
│   ├── 📊 Node Metrics
│   ├── 📦 Pod Metrics
│   ├── 🐳 Container Metrics
│   └── ☸️ Kubernetes Metrics
│
└── 📉 Grafana
    ├── 📋 Dashboards
    ├── 🚨 Alerts
    └── 📊 Visualization
```

## ✅ Step 1: Verify EKS Cluster
* 🔍 Check cluster connectivity:
```hcl
kubectl get nodes
```

## ⚙️ Step 2: Install Helm
```hcl
curl https://raw.githubusercontent.com/helm/helm/main/scripts/get-helm-3 | bash
```

### ✅ Verify:
```hcl
helm version
```

## 📦 Step 3: Add Prometheus Community Repository
```hcl
helm repo add prometheus-community https://prometheus-community.github.io/helm-charts

helm repo update
```

### ✅ Verify:
```hcl
helm search repo prometheus-community
```

## 🏗️ Step 4: Create Monitoring Namespace
```hcl
kubectl create namespace monitoring
```
```hcl
kubectl get ns
```

## 🚀 Step 5: Install Prometheus & Grafana Stack
* 📥 Install kube-prometheus-stack:
```hcl
helm install monitoring prometheus-community/kube-prometheus-stack \
  --namespace monitoring
```

* 🎁 This installs:
  * ✅ Prometheus
  * ✅ Grafana
  * ✅ Alertmanager
  * ✅ Node Exporter
  * ✅ kube-state-metrics
  * ✅ Prometheus Operator

## 🔍 Step 6: Verify Installation
* 📦 Check pods:
```hcl
kubectl get pods -n monitoring
```

## 🌐 Step 7: Check Services
```hcl
kubectl get svc -n monitoring
```

## 📊 Step 8: Expose Grafana via AWS Load Balancer
```hcl
kubectl patch svc monitoring-grafana \
-n monitoring \
-p '{"spec":{"type":"LoadBalancer"}}'
```

* ✅ Check:
```hcl
kubectl get svc monitoring-grafana -n monitoring
```

### 🔐 Get Grafana Login Password

* 👤 Username: `admin`
* 🔑 Password:

```hcl
kubectl get secret monitoring-grafana \
-n monitoring \
-o jsonpath="{.data.admin-password}" | base64 --decode && echo
```
* 📋 Show Generated Password `copy` and `paste`

## 📈 Step 9: Expose Prometheus via LoadBalancer
```hcl
kubectl patch svc monitoring-kube-prometheus-prometheus \
-n monitoring \
-p '{"spec":{"type":"LoadBalancer"}}'
```

* ✅ Check:
```hcl
kubectl get svc monitoring-kube-prometheus-prometheus -n monitoring
```

* 📝 Example:
```hcl
NAME                                    TYPE           EXTERNAL-IP
monitoring-kube-prometheus-prometheus   LoadBalancer   abc123.elb.amazonaws.com
```

* 🌐 Then open:
```hcl
a82f2aa6acee9464aa6d7e061a1ffcc1-1209216230.ap-south-1.elb.amazonaws.com:9090
```
  * ⚠️ `9090` port is must after prometheus loadbalancer DNS name

## 🔗 Step 10: Verify Prometheus Data Source
* 🔐 Login to Grafana.
* 📍 Go to:
```hcl
Connections
    ↓
Data Sources
    ↓
Add new Data Source
```

* ✅ Select: `Prometheus`
* 🌐 URL:
```hcl
http://a82f2aa6acee9464aa6d7e061a1ffcc1-1209216230.ap-south-1.elb.amazonaws.com:9090
```
* ✅ Click: `Save & Test`

## 📋 Step 11: Import Kubernetes Dashboards
* 📍 Navigate:
```hcl
  Dashboards
    ↓
   New
    ↓
  Import
```

### ⭐ Popular dashboard IDs:

| Dashboard                        | ID    |
| -------------------------------- | ----- |
| 📊 Node Exporter Full            | 1860  |
| ☸️ Kubernetes Cluster Monitoring | 7249  |
| 🌍 Kubernetes Views Global       | 15757 |
| 🖥️ Kubernetes Views Nodes       | 15759 |
| 📦 Kubernetes Views Pods         | 15760 |
