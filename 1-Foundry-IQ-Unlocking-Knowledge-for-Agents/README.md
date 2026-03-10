# Episode 1: Foundry IQ: Unlocking Knowledge for your Agents

<!-- Episode video thumbnail - add your thumbnail here -->
[![Episode 1 video](../images/FIQ_Episode1.jpg)](https://aka.ms/iq-series/episode1)

📅 **March 18, 2026 at 9 AM PT** | 📺 [Watch the session](https://aka.ms/iq-series/episode1) | 📂 [Try the cookbook](./cookbook/)

## 🎥 Session Summary

### 🎬 Executive Introduction

Pablo Castro introduces Foundry IQ and sets the stage for the series.

### 💬 Tech Talk

Ayca Bas and Farzad Sunavala walk through the idea of a unified knowledge layer for agents, explaining:

- Core components of Foundry IQ
- How it fits into the broader agent architecture

### 🖍 Doodle Summary

A visual summary of key takeaways by Tomomi Imura, showing how Foundry IQ fits into the broader agent architecture.

![Doodle summary Episode 1](../images/visuals/E1-recap.png)

## 📋 Prerequisites

- **Azure Subscription** with permissions to create resources and assign roles
- **Azure CLI** installed and configured ([Install guide](https://learn.microsoft.com/cli/azure/install-azure-cli))
- **Python 3.10+** installed
- A region that supports [agentic retrieval](https://learn.microsoft.com/azure/search/search-region-support) (default: `eastus2`)

## 🚀 Deploy Azure Resources

Deploy all required Azure resources with one click — this creates AI Search, Azure OpenAI, AI Services, a Foundry project, an AI Search connection, model deployments, and RBAC roles:

[![Deploy to Azure](https://aka.ms/deploytoazurebutton)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fmicrosoft%2Fiq-series%2Fmain%2Finfra%2Fazuredeploy.json)

You'll be asked to sign in to the Azure Portal if you aren't already. Then, in the deployment form, you'll be prompted to:

- **Create a new resource group** (e.g., `iq-series-rg`) to hold all the deployed resources — click **Create new** under the Resource group field in the portal. If you've already created one for a previous episode, select it instead
- Enter your **User Object ID** (see below)
- Customize the resource prefix, location, and SKUs

**How to get your User Object ID:** Open a terminal and run:

```bash
az login
az ad signed-in-user show --query id -o tsv
```

This returns your Microsoft Entra ID unique identifier — paste it into the deployment form. It's needed to assign proper RBAC roles to your account.

After deployment, create a `.env` file in the `cookbook/` folder with your values from the deployment outputs:

```env
SEARCH_ENDPOINT=https://<your-search-service>.search.windows.net
AOAI_ENDPOINT=https://<your-openai-resource>.openai.azure.com
AOAI_EMBEDDING_MODEL=text-embedding-3-large
AOAI_EMBEDDING_DEPLOYMENT=text-embedding-3-large
AOAI_GPT_MODEL=gpt-4o-mini
AOAI_GPT_DEPLOYMENT=gpt-4o-mini
FOUNDRY_PROJECT_ENDPOINT=https://<your-ai-services>.services.ai.azure.com/api/projects/<your-project>
FOUNDRY_MODEL_DEPLOYMENT_NAME=gpt-4o-mini
AZURE_AI_SEARCH_CONNECTION_NAME=iq-series-search-connection
```

**Where to find these values:** All values are available in the deployment **Outputs** tab in the Azure portal. You can also find them in [Microsoft Foundry](https://ai.azure.com) → your project → **Overview**.

For CLI deployment and cleanup instructions, see the [Infrastructure Guide](../infra/README.md).

> **Note:** This deployment is shared across all Foundry IQ episodes. You only need to deploy once — if you've already deployed for another episode, skip this and reuse your existing resources.

## 📓 Run the Cookbook

Once your Azure resources are deployed, open the [Episode 1 Cookbook](./cookbook/) and follow the step-by-step notebook to get started.

## 🔗 Learn More

- 📖 [What is Foundry IQ?](https://learn.microsoft.com/azure/foundry/agents/concepts/what-is-foundry-iq?tabs=portal)
- 📚 [Azure AI Foundry Documentation](https://learn.microsoft.com/azure/ai-foundry/)

## 💬 Community

- Ask your questions on our [Discord channel](https://discord.gg/REmjGvvFpW)

### 🚀 Next Up: Continue to [Episode 2](../2-Foundry-IQ-Building-the-Data-Pipeline-with-Knowledge-Sources/) for the next step—Building the Data Pipeline with Knowledge Sources!
