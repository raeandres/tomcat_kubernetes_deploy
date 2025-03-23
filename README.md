# tomcat_kubernetes_deploy

A simple tomcat deployment showcasing containerization deployments using kubernetes

# Deployment Pre-requisites

- minikube
  - installation via homebrew:
  - brew install minikube
- docker distribution mac os
  - https://www.docker.com/products/personal/

## Starting Minikube

    - Docker desktop must be opened before staring minikube
    - minikube start —driver docker  >> starting minikube
    - minikube status                >> check minikube status

## Starting Deployment yaml

    - kubectl apply -f <Deployment-file>.yaml
    - kubectl apply -f <Service-file>.yaml

## Checking deployment status

    - kubectl get pods              >> get the resources information
    - kubectl get pods -o wide      >> get the pods information along with other resource information
    - kubectl get deploy -o wide    >> get the deployment name, status, instance count, containers, images, and SELECTOR
    - kubectl get service -o wide   >> get the service information along with ports, type, clusterIP, AGE and EXTERNAL-IP, SELECTOR

## Note:

    - SELECTOR must be defined in service as it is very vital when working with Loadbalancers as the LB will match the name provided in the matchLabels. It will be helpful to map the needed service for routing.
