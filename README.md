# k8s-jenkins-connection
# Set 1: Jenkins Integration with Kubernetes

## Aim
To configure Jenkins to connect to a Kubernetes cluster and verify the connection.

## Tools Required
- Jenkins
- Docker Desktop
- Kubernetes
- kubectl
- GitHub

## Description
This experiment connects Jenkins with a local Kubernetes cluster running through Docker Desktop. A Jenkins Pipeline is used to check the Kubernetes context, verify cluster connectivity, and display the available nodes and Pods.

## Procedure
1. Start Docker Desktop and ensure the Kubernetes cluster is running.
2. Verify the cluster connection using `kubectl`.
3. Create a Jenkins Pipeline job.
4. Configure the Pipeline to retrieve the required files from this GitHub repository.
5. Execute Kubernetes commands through Jenkins.
6. Verify the connection through the Jenkins Console Output.

## Verification Commands
```bash
kubectl config current-context
kubectl cluster-info
kubectl get nodes
kubectl get pods -A
```

## Expected Result
Jenkins successfully executes Kubernetes commands and displays the cluster information, nodes, and Pods.

## Status
Experiment in progress.
