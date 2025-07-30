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
