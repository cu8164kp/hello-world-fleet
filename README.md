# Hello World Fleet Demo

## Overview

This repository contains Kubernetes manifests for deploying a simple Nginx web server using Fleet in Rancher. It is structured to support different environments: Development (`dev`) and Production (`prod`).

## Repository Structure

```plaintext
hello-world-fleet/
|-- dev/             # Development environment
|   |-- app1.yaml    # Kubernetes manifests for dev
|-- prod/            # Production environment
|   |-- app1.yaml    # Kubernetes manifests for prod
|-- README.md        # Documentation

