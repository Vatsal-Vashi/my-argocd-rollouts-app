# Argo CD and Argo Rollouts Example

This repository provides an example application deployment using Argo CD and Argo Rollouts.

## Deployment Steps

### Step 1: Create an Application in Argo CD

- In the Argo CD UI, click on `New App`.
- Provide the following details:
  - **Application Name:** `myapp`
  - **Project:** `default`
  - **Repository URL:** `https://github.com/YOUR_GITHUB_USERNAME/my-argocd-rollouts-app.git`
  - **Path:** `app`
- Click `Create`.

### Step 2: Sync the Application

- After creating the application, click on `Sync` to deploy the application to your AKS cluster.

### Step 3: Deploy a Progressive Delivery Application with Argo Rollouts

- Apply the rollout manifest:
  ```sh
  kubectl apply -f rollout.yaml
