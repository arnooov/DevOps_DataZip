# DataZip Internship Assignment: Deploy ClickHouse & Superset on Minikube

This guide provides instructions to set up Superset with Kubernetes using Minikube and Docker.

## Prerequisites

- **Install Minikube**: Follow the [official Minikube installation guide](https://minikube.sigs.k8s.io/docs/start/) for your operating system.
- **Install Docker**: Follow the [official Docker installation guide](https://docs.docker.com/get-docker/) for your operating system.

## Setup 

### 1. Start Minikube

Open a terminal and run:
```sh
minikube start --driver=docker
```

### 2. Apply Kubernetes Configuration Files

Apply all four YAML configuration files using:
```sh
kubectl apply -f clkhouse-ser.yaml
kubectl apply -f clkhouse-state.yaml
kubectl apply -f superset-conf.yaml
kubectl apply -f superset-deploy.yaml
```

### 3. Chech Pod Status

Verify all pods are running:
```sh
kubectl get pods
```

### 4. Check Services

List all services:
```sh
kubectl get services
```

### 5. Access Superset URL

Obtain the Superset service URL:
List all services:
```sh
minikube service superset
```

### 6. Login to Superset

Open the URL provided in the previous step in your web browser and log in to Superset.

### 7. Add ClickHouse Database

- Navigate to **Settings** -> **Data** -> **Database Connections** -> **Databases** -> **+ Database**.
- Select **ClickHouse** from the database list and choose **ClickHouse Connect (Superset)**.

### 8. Configure ClickHouse Connection

Fill in the following details:
- Host
- Port
- Database name
- Username














