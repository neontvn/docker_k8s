Kubernetes Terminology

1. Kubernetes Cluster - collection of nodes
2. Node - Virtual machine that will run code
3. Pods - Running container. Technically a pod can run multiple containers
4. Deployment - Monitors a set of pods, makes sure they are running and restarts if crashed
5. Service - Provides an easy to remember URL to access a running container

Kubernetes Config Files
 - Tells Kubernetes about the Deployments, Pods, Services ( Referred to as Objects )
 - Written in YAML syntax
 - Documentation

Minikube : 

    --> Minikube runs a single-node Kubernetes cluster on your personal computer
    --> A one node cluster, where the master and worker processes are on the same machine.

Commands
    |_ minikube start
    |_ minikube dashboard
___________________________________________________________________________________________

Creating a Pod ( With example and explaination )

File - posts.yaml

apiVersion : v1
kind : Pod              // Type of Object we want to create
metadata :
