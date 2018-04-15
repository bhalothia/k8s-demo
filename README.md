# Problem Statement
Provide an Service as Docker Container fulfilling the following criteria:

- Create a Docker Image from scratch or from docker hub (e.g. hashicorp/http-echo)
- Self-healing and fail-proof
1. Implement in Kubernetes
2. Describe for AWS
- Automated deployment
1. Implement in Kubernetes OR
2. Implement with Vagrant & Ansible
- Simple scaling of instances / containers
1. Implement in Kubernetes
2. Describe for AWS

====


# Kubernetes setup on Amazon AWS using Kops and Ansible

This repository contains tooling for deploying Kubernetes cluster in Amazon AWS using the [Kops](https://github.com/kubernetes/kops) tool. Kops is a great tool if you want to setup HA cluster and don't require too much flexibility.

# Demonstrating a sample deployment on K8s cluster (Minikube)

Here's a screencast demonstrating a sample [deployment](https://www.youtube.com/watch?v=Y88o-wYmuos) on K8s cluster (Minikube). 
