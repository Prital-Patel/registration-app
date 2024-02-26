# Registration-App
End-to-End DevOps Deployment of Java Web Application on EKS

## Requirements
1. Jenkins
2. Maven
3. Ansible
4. Docker Hub
5. EKS

## Overview

# Continuous Integration (CI) Pipeline:
Whenever any changes occur in github repository.

Jenkins pulls code from the GitHub repository and initiates a Maven build process to generate artifacts.

Artifacts are transferred to the Ansible server, where Docker is installed.

Ansible utilizes the artifacts to create Docker images, which are then pushed to Docker Hub.

# Continuous Deployment (CD) Pipeline:
The successful completion of the CI pipeline triggers the CD pipeline.

A bootstrap server facilitates CD operations, interacting with the Kubernetes cluster.

Docker images are pulled from Docker Hub to the bootstrap server.

Using Kubernetes, containers are deployed onto Amazon Elastic Kubernetes Service (EKS), ensuring scalable and resilient deployment.
