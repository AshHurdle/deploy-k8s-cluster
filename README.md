# deploy-k8s-cluster
Instructions to Deploy a one-node K8s cluster using Minikube

The below document contains instructions on deploying a K8s cluster to your local machine using Minikube - and then installing Datadog on that cluster.

This documentation assumes the following are installed on your machine:
	
	Brew
	
	Docker Desktop - installation instructions for Mac here https://docs.docker.com/desktop/install/mac-install/
		Docker Desktop will function as the VM Driver for Minikube
	
	
# Setup Minikube

1.  Install kubectl client to interact with your Kubernetes cluster:

	```
	brew install kubernetes-cli
	```
2.  Install Minikube - https://minikube.sigs.k8s.io/docs/start/
	```
	brew install minikube
	```
3.  Start Minikube with default parameters
	```
	minikube start
	```
## Minikube installed - What now?






