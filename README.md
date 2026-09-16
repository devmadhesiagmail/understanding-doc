# understanding-doc

====
**GitHub Codespaces** is a cloud-based development environment that lets you write, build, test, and debug code directly from GitHub without installing all project dependencies on your local machine. Each codespace runs in a container on a cloud-hosted virtual machine and can be accessed from a browser, Visual Studio Code, or supported IDEs.

In simple terms

Instead of spending hours setting up:

VS Code extensions
SDKs and runtimes
Databases
Docker containers
Environment variables

You click"Create Codespace" and GitHub creates a ready-to-use development environment for the repository.

Key Benefits
Instant onboarding for new developers
Consistent development environment across the team
Access from any device with internet access
Eliminates "works on my machine" problems
Scalable cloud compute for large projects
Can run multiple isolated development environments simultaneously
========

[ Practice 1 ] 

sample web app link after deployed - https://ca-api-ztvvllot3fqc6.yellowcliff-68479396.eastus2.azurecontainerapps.io/
web app - based on react JS, fluent to create chat like UI, prompt etc..
backend API - based on python, fast API
bicep - for environment and resource creation 

"@fluentui-copilot/react-copilot": "0.23.3",
    "@fluentui-copilot/react-copilot-chat": "0.9.6",
    "@fluentui-copilot/react-feedback-buttons": "0.9.6",
then using docker to make it container

Created resource in my azure portal 
create foundry project => created model gpt 4.1 min inside foundry, no agent etc...
Tokens per Minute Rate Limit
80000
Requests per Minute Rate Limit
80
Model guardrails
Name
DefaultV2

aoai-ztvvllot3fqc6
Foundry
East US 2
proj-ztvvllot3fqc6 (aoai-ztvvllot3fqc6/proj-ztvvllot3fqc6)
Foundry project
East US 2
appi-ztvvllot3fqc6
Application Insights
East US 2
ca-api-ztvvllot3fqc6
Container App
East US 2
containerapps-env-ztvvllot3fqc6
Container Apps Environment
East US 2
crztvvllot3fqc6
Container registry
East US 2
id-api-ztvvllot3fqc6
Managed Identity
East US 2
log-ztvvllot3fqc6
Log Analytics workspace
East US 2
stztvvllot3fqc6
Storage account
East US 2

===

AI bases project
sample available in MS Foundry portal
https://github.com/devmadhesiagmail/get-started-with-ai-chat/blob/main/docs/sample_questions.md

https://github.com/devmadhesiagmail/get-started-with-ai-chat/blob/main/README.md
Solution Overview
This solution deploys a web-based chat application with AI capabilities running in Azure Container App.

The application leverages Microsoft Foundry projects and Foundry Tools to provide intelligent chat functionality. It supports both direct AI model interaction and Retrieval-Augmented Generation (RAG) using Azure AI Search for knowledge retrieval from uploaded files, enabling it to generate responses with citations. The solution also includes built-in monitoring capabilities with tracing to ensure easier troubleshooting and optimized performance.

This solution creates an Microsoft Foundry project and Foundry Tools. More details about the resources can be found in the resources documentation. There are options to enable RAG, logging, tracing, and monitoring.

Instructions are provided for deployment through GitHub Codespaces, VS Code Dev Containers, and your local development environment.

**Solution Architecture
**Architecture diagram showing that user input is provided to the Azure Container App, which contains the app code. With user identity and resource access through managed identity, the input is used to form a response. The input and the Azure monitor are able to use the Azure resources deployed in the solution: Application Insights, Azure AI Project, Foundry Tools, Azure AI Hub, Storage account, Azure Container App, Container Registry, Key Vault, Log Analytics Workspace, and Search Service.

<img width="2454" height="655" alt="image" src="https://github.com/user-attachments/assets/b94c5045-1d8a-4aae-9f58-4fda830d53b2" />


The app code runs in Azure Container Apps to process the user input and generate a response to the user. It leverages Azure AI projects and Foundry Tools, including the model and search service.

Key Features
• Knowledge Retrieval: The AI chat application supports Retrieval-Augmented Generation (RAG) using Azure AI Search to retrieve knowledge from uploaded files, enabling contextual responses with citations.

• Customizable AI Model Deployment: The solution allows users to configure and deploy AI models, such as gpt-4o-mini, with options to adjust model capacity, deployment configurations, and knowledge retrieval methods.

• Built-in Monitoring and Tracing: Integrated monitoring capabilities, including Azure Monitor and Application Insights, enable tracing and logging for easier troubleshooting and performance optimization.

• Flexible Deployment Options: The solution supports deployment through GitHub Codespaces, VS Code Dev Containers, or local environments, providing flexibility for different development workflows.

Here is a screenshot showing the chatting web application with requests and responses between the system and the user:

Screenshot of chatting web application showing requests and responses between assistants and the user.

===
I was able to succesfully run this app 
Click Open in GitHub Codespaces or Dev Containers button above

Wait for the environment to load

Deploy to Azure — choose one of the options below:

Option A: azd up (5–20 minutes)
If you have experience with azd templates, run directly in the terminal:

azd up

Found model unsupported eror which I fixed with help from github copilot 
===
