# Azure Container Apps Album API

This is the companion repository for the [Azure Container Apps code-to-cloud quickstart](https://docs.microsoft.com/en-us/azure/container-apps/quickstart-code-to-cloud?tabs=bash%2Ccsharp&pivots=acr-remote).

This backend Album API sample is available in other languages:

| [JavaScript](https://github.com/azure-samples/containerapps-albumapi-javascript) | [Go](https://github.com/azure-samples/containerapps-albumapi-go) | [Python](https://github.com/azure-samples/containerapps-albumapi-python) | [Java](https://github.com/azure-samples/containerapps-albumapi-java) |
| -------------------------------------------------------------------------------- | ---------------------------------------------------------------- | ------------------------------------------------------------------------ | ---------------------------------------------------------------- |

### Pre-Demo Tasks
1. Infrastructure developed in Bicep.
2. Empty Dockerfiles, GitHub Actions and K8s manifests files created in their respective locations. 

### Introduction
1. Open VSCode and install GitHub Copilot for Azure extension
2. Login to Azure and GitHub in VSCode
3. Open the GitHub Copilot chat window
4. Use the following prompt: `@azure Tell me about my application`

### Containerization
1. Use the following prompt: `@azure Help me write Dockerfiles for my application.`
2. Use the following prompt: `@azure Use dotnet 5 for the images`
3. Open the respective Dockerfiles. Click the *Apply in Editor* button in Copilot and save the content in each respective file. 

### Deployment (Kubernetes Manifests)
1. Use the following prompt: `@azure Help me write manifests for my application.`
2. Use the following prompt: `@azure Can you add resource limits to the ContainerApp?`
3. Use the following prompt: `@azure Add node tolerations with a key app and value being the name of the app.`
4. Use the following prompt: `@azure I need a deployment for my database`
5. Open the respective manifests. Click the *Apply in Editor* button in Copilot and save the content in each respective file. 

### Deployment (GitHub Actions)
1. Use the following prompt: `@Help me write a GitHub Actions to deploy this application including a Bicep deployment.`
2. Use the following prompt: `@azure Use OIDC for Azure login.`
3. Use the following prompt: `@azure Use the Bicep-deploy action to deploy the Bicep infra.`
4. Use the following prompt: `@azure Split the workflow into three stages: deploy-infra, build-and-push and deploy.`
5. Use the following prompt: `@azure For deploy-infra stage, make the resource group and acr outputs for subsequent jobs.`
6.  Open the workflow file. Click the *Apply in Editor* button in Copilot and save the content in the file. s

### Edits

After using Copilot to generate the structure and some of the functionality for each of these components, edits had to be made to support a successful deployment including:
- Updating resource limits on manifests 
- Adding environment variables to the manifests 
- Update name of placeholder for ACR name 
- Add Docker login to GitHub Actions
- Add install of Kubectl and Kube login to GitHub Actions
- Add a step in GitHub Actions to replace the name of the ACR placeholder dynamically in the manifest. 

## Activities

### Activity One: GitHub Actions

Let's try to generate the GitHub Actions workflow ourselves. We showed some basic steps in the demo, but we had to make a few edits to the workflow and additional commands to make it work. Given the following information, try to use your knowledge and Copilot to generate the GitHub Actions workflow. 

1. Cluster is AAD enabled
2. We need to build and push our container images using Docker and ACR. 

Sample Commands:

`@azure Can you write a Dependabot workflow for me? `

`@azure Can you setup X as an output for X stage?`

`@azure What is the most secure method for logging into ACR in a GitHub Actions workflow?`

