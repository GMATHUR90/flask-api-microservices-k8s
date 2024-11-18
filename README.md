# flask-api-microservices-k8s

## Introduction
This repository demonstrates how to deploy a Flask-based microservice using Kubernetes. It provides Kubernetes YAML files for managing deployments, services, and persistent storage. This setup is ideal for developers looking to understand how to integrate Flask microservices with Kubernetes for scalable and resilient applications.

## Features
- **Flask API:** A simple RESTful API built with Flask.
- **Kubernetes Manifests:** YAML files for Deployments, Services, and Persistent Volumes.
- **MongoDB Integration:** Configured MongoDB service with persistent storage.
- **Scalability:** Easily scale the Flask service using Kubernetes.

## Architecture
The application consists of two main components:

- **Flask API:** Serves as the backend microservice handling HTTP requests.
- **MongoDB:** Acts as the database for storing and retrieving data.

Kubernetes orchestrates the deployment, scaling, and management of these components, ensuring high availability and resilience.

## Technologies Used
- **Python:** Programming language for the Flask API.
- **Flask:** Web framework for building the API.
- **Kubernetes:** Container orchestration system.
- **MongoDB:** NoSQL database.
- **Helm (optional):** For managing Kubernetes applications.

## Prerequisites
Before proceeding, make sure you have `kubeadm` installed on both the master and worker (slave) nodes. You can follow the installation guide here: [Kubeadm Installation Using Containerd](https://github.com/GMATHUR90/kubestarter/blob/main/Kubeadm_Installation_Using_Containerd.md).

## Installation
### 1. Clone the Repository
```bash
git clone https://github.com/your-username/flask-microservices-k8s.git
cd flask-microservices-k8s
```
### 2.Prepare the Kubernetes Environment
Ensure your Kubernetes cluster is running and kubectl is configured to connect to it.

## Usage
### 1. Deploy to Kubernetes
Apply the Kubernetes manifests to deploy the Flask API and MongoDB.
```bash
kubectl apply -f k8s/mongo-pv.yml
kubectl apply -f k8s/mongo-pvc.yml
kubectl apply -f k8s/mongo-svc.yml
kubectl apply -f k8s/flask-deployment.yml
kubectl apply -f k8s/flask-svc.yml
```
### 2. Access the Flask API
Once deployed, you can access the Flask API using the service's external IP .

Visit http://localhost:5000 in your browser interact with the API.

## Contributing
**This repository is for personal use only, and contributions are not accepted.**

## License
This project is licensed under the MIT License.



