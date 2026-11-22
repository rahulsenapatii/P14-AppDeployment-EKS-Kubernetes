# Project 14: App Deployment using EKS
Author: Rahul Senapati

## Goal
Deploy app on Kubernetes by provisioning an EKS cluster and exposing the service publicly.

## Files
- cluster.yaml: EKS cluster configuration (rahul-senapati-eks-cluster) in ap-south-1.
- deployment.yaml: Kubernetes Deployment running 2 replicas of nginx:alpine.
- service.yaml: Kubernetes LoadBalancer Service exposing port 80 publicly.

## Commands Used
1. Provision EKS:
   eksctl create cluster -f cluster.yaml

2. Deploy App & Expose Publicly:
   kubectl apply -f deployment.yaml
   kubectl apply -f service.yaml

3. Get Public Endpoint:
   kubectl get svc rahul-senapati-service
