===
https://github.com/devmadhesiagmail/get-started-with-ai-agents

I was able to successfuly provision and run this code base
Click Open in GitHub Codespaces or Dev Containers button above

By default, agents use OpenAI's file search capability with the documents in the src/files folder. To enable Azure AI Search instead, set the environment variable before the first time of provision and deployment:

azd env set USE_AZURE_AI_SEARCH_SERVICE true

azd up
====


user guide readme
https://github.com/devmadhesiagmail/get-started-with-ai-agents

Solution Overview
This solution deploys a web-based chat application with an AI agent running in Azure Container App.

The agent leverages the Foundry Agent Service and utilizes Azure AI Search for knowledge retrieval from uploaded files, enabling it to generate responses with citations. The solution also includes built-in monitoring capabilities with tracing to ensure easier troubleshooting and optimized performance.

This solution creates a Microsoft Foundry project and Foundry Tools. More details about the resources can be found in the resources documentation. There are options to enable logging, tracing, and monitoring.

Instructions are provided for deployment through GitHub Codespaces, VS Code Dev Containers, and your local development environment.

**Solution Architecture
**Architecture diagram showing that user input is provided to the Azure Container App, which contains the app code. With user identity and resource access through managed identity, the input is used to form a response. The input and the Azure monitor are able to use the Azure resources deployed in the solution: Application Insights, Microsoft Foundry Project, Foundry Tools, 
Storage account, Azure Container App, and Log Analytics Workspace.

===
The app code runs in an Azure Container App to process user input and generate a response to the user. It leverages Microsoft Foundry projects and Foundry Tools, including the model and agent.

Key Features
Knowledge Retrieval
The AI agent uses file search or Azure AI Search to retrieve knowledge from uploaded files.

Customizable AI Model Deployment
The solution allows users to configure and deploy AI models, defaulting to gpt-5-mini, with options to adjust model capacity and knowledge retrieval methods.

Built-in Monitoring and Tracing
Integrated monitoring capabilities, including Azure Monitor and Application Insights, enable tracing and logging for easier troubleshooting and performance optimization.

Flexible Deployment Options
The solution supports deployment through GitHub Codespaces, VS Code Dev Containers, or local environments, providing flexibility for different development workflows.

Continuous Evaluation
Proactively monitor and assess your agent's performance over time with continuous evaluation that automatically checks real-world interactions to identify potential issues before they impact users.

Agent Evaluation
This solution demonstrates how you can evaluate your agent's performance and quality through Pytest.

AI Red Teaming Agent
Facilitates the creation of an AI Red Teaming Agent through Pytest that can run batch automated scans for safety and security on your Agent solution to check your risk posture before deploying it into production.
