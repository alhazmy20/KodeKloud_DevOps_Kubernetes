# Kubernetes WebAPI Application   

This is a simple project created to showcase what I've learned while attending the DevOps Learning Path on KodeKloud.

## Contains
- This project contains multiple resource manifest files that do the following:
    - The `webapi-deployment` file is used to create a deployment for the go-webapi app, launching 3 replicas for the app.
    - The `webapi-svc` file creates a NodePort service to expose a port, allowing you to access the app from the host machine.
    - The `mysql-pod` file is used to launch MySQL instances in a pod.
    - The `mysql-pvc` file is used to create a PersistentVolumeClaim so that MySQL data can persist if the pod is destroyed.
    - The `mysql-config` file is used to create a ConfigMap that contains key-value pairs to configure the MySQL instance.
    - The `mysql-svc` file is used to create a service that targets a port on `mysql-pod` so that webapi pods can communicate with `mysql-pod`.

## Usage
Apply the resource manifest files using the following command:
```bash
kubectl apply -f filename
```