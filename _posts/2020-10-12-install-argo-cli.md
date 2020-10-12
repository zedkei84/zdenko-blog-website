---
date: 2020-10-12 00:00:00
title: Install Argo CLI
categories:
  - deployment
description: Install Argo CLI on your local PC
type: Document
---
## What is Argo Workflows?

Argo Workflows is an open source container-native workflow engine for orchestrating parallel jobs on Kubernetes. 
Argo Workflows is implemented as a Kubernetes CRD (Custom Resource Definition).

 - Define workflows where each step in the workflow is a container.
 - Model multi-step workflows as a sequence of tasks or capture the dependencies between tasks using a directed acyclic graph (DAG).
 - Easily run compute intensive jobs for machine learning or data processing in a fraction of the time using Argo Workflows on Kubernetes.
 - Run CI/CD pipelines natively on Kubernetes without configuring complex software development products.

## Why Argo Workflows?

 - Designed from the ground up for containers without the overhead and limitations of legacy VM and server-based environments.
 - Cloud agnostic and can run on any Kubernetes cluster.
 - Easily orchestrate highly parallel jobs on Kubernetes.
 - Argo Workflows puts a cloud-scale supercomputer at your fingertips!

## How to install on Linux

~~~ bash
# Download the binary
curl -sLO https://github.com/argoproj/argo/releases/download/v2.11.2/argo-linux-amd64.gz

# Unzip
gunzip argo-linux-amd64.gz

# Make binary executable
chmod +x argo-linux-amd64

# Move binary to path
mv ./argo-linux-amd64 /usr/local/bin/argo

# Test installation
argo version
~~~

## How to install on Mac

~~~ bash
# Download the binary
curl -sLO https://github.com/argoproj/argo/releases/download/v2.11.2/argo-darwin-amd64.gz

# Unzip
gunzip argo-darwin-amd64.gz

# Make binary executable
chmod +x argo-darwin-amd64

# Move binary to path
mv ./argo-darwin-amd64 /usr/local/bin/argo

# Test installation
argo version
~~~
