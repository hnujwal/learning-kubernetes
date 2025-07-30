Instructions
This repository does not have any branches. Download the entire repository, change into the exercise-files directory, and you will have the exercise files in their final state.

Installing
Clone this repository into your local machine using the terminal (Mac), CMD or PowerShell (Windows), or a GUI tool like SourceTree.
You can also download a ZIP file from Github and extract the contents to your machine.
Place the exercise files on your computer when you can easily access them.
To use these exercise files, you must have the following installed:
[Docker](https://docs.docker.com/) 
[minikube](https://minikube.sigs.k8s.io/docs/start/?arch=%2Fwindows%2Fx86-64%2Fstable%2F.exe+download)
# Kubernetes Pod Info App

This repository contains Kubernetes manifests for deploying the Pod Info App.

## Files

- [`namespace.yaml`](namespace.yaml): Defines the `development` namespace.
- [`deployment.yaml`](deployment.yaml): Deploys the Pod Info App with 3 replicas in the `development` namespace.

## Usage

1. Create the namespace:

   ```sh
   kubectl apply -f namespace.yaml
   ```

2. Deploy the application:

   ```sh
   kubectl apply -f deployment.yaml
   ```

3. Check the status:
   ```sh
   kubectl get pods -n development
   ```

## Application Details

- **Image:** `kimschles/pod-info-app:latest`
- **Port:** 3000
- **Environment Variables:**
  - `POD_NAME`: Pod name
  - `POD_NAMESPACE`: Pod namespace
  - `POD_IP`:
