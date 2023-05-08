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

To take a look at everything running on our Minikube - we can run the following command to get a look at all our pods:

	kubectl get pods --all-namespaces
	
The --all-namespaces bit allows us to see pods from ***every namespace***.  In Kubernetes, you can separate pods and run them under different namespaces - perhaps for organization, security, or performance purposes.

## Minikube commands

A few useful commands for Minikube include:

```
minikube start
minikube stop
minikube status
```

Start a new fresh environment with profiles:
```
minikube start -p <name_of_your_profile>
```

See all the profiles created:
```
minikube profile list
```

Delete a profile:
```
minikube delete -p <name_of_your_profile>
```

Connect to minikube:
```
minikube ssh
```

More minikube commands can be found here https://minikube.sigs.k8s.io/docs/commands/



