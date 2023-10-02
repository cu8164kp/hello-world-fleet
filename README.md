Hello World Fleet Demo
This repository contains Kubernetes manifests for deploying a simple Nginx web server using Fleet in Rancher. The repository is structured to support different environments: Development (dev) and Production (prod).

Repository Structure
r
Copy code
hello-world-fleet/
|-- dev/                    # Development environment
|   |-- app1.yaml           # Kubernetes manifests for dev
|-- prod/                   # Production environment
|   |-- app1.yaml           # Kubernetes manifests for prod
|-- README.md               # Documentation

How to Use
Label Your Clusters: Label your clusters in Rancher with env=dev for development and env=prod for production.

Fleet Configuration: Create two GitRepo custom resources in Rancher's Continuous Delivery section. Point each to this repository and specify the dev/ or prod/ folder in the Paths field. Use the env=dev or env=prod label in the Cluster Selector.

Deploy: Once the GitRepo custom resources are created, Fleet will automatically deploy the manifests in the respective folders to the clusters that match the labels.

Differences Between Dev and Prod

Replicas: Development uses 1 replica, while Production uses 3.
Service Port: Development exposes the service on port 8080, while Production uses port 80.
Environment Variable: An environment variable ENV_TYPE is set to indicate the environment.
