# Kubernetes Go WebAPI Application

This project is a simple demonstration of my learnings from the DevOps Learning Path on KodeKloud.

## Project Contents
This project includes multiple resource manifest files that perform the following tasks:

- The `webapi-deployment` file creates a deployment for the Go WebAPI app, launching 3 replicas.
- The `webapi-svc` file establishes a NodePort service to expose a port, enabling access to the app from the host machine.
- The `mysql-pod` file launches MySQL instances in a pod.
- The `mysql-pvc` file creates a PersistentVolumeClaim, ensuring that MySQL data persists even if the pod is destroyed.
- The `mysql-config` file creates a ConfigMap containing key-value pairs to configure the MySQL instance.
- The `mysql-svc` file creates a service targeting a port on `mysql-pod` so that webapi pods can communicate with `mysql-pod`.

## Usage
Apply the resource manifest files using the following command:

```bash
kubectl apply -f filename
