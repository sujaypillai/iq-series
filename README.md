# The IQ Series

![The IQ Series Banner](./images/iq-series-banner.png)

Master Microsoft IQ with The IQ Series! Microsoft IQ is Microsoft's unified intelligence layer for the enterprise, bringing together three core intelligence services:

- **Foundry IQ**: A managed knowledge layer for enterprise data; connecting structured and unstructured data across Azure, SharePoint, OneLake, and the web so agents can access permission-aware knowledge.
- **Work IQ**: The intelligence layer that personalizes Microsoft 365 Copilot; understanding context, relationships, and work patterns so agents can be faster, more accurate, and more secure.
- **Fabric IQ**: Unify business semantics across data, models, and systems to power intelligent agents and decisions grounded in a live, holistic view of the business.

Together, these IQs enable AI agents to reason, retrieve, and act with deep business context going beyond traditional RAG for true enterprise intelligence.

> **Note:** The series kicks off with **Foundry IQ** episodes. Work IQ and Fabric IQ content is coming soon!

📺 Foundry IQ episodes premiere **every Wednesday at 9 AM PT**, starting **March 18, 2026** on [Microsoft Developer YouTube](https://aka.ms/iq-series).

## 📚 Episodes

### Foundry IQ

| **Episode**                                                                                                                          | **Description**                                                                    | **Video**       | **Cookbook**                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|-----------------|-------------------------------------------------------------------------------------| 
| [Foundry IQ: Unlocking Knowledge for your Agents](./1-Foundry-IQ-Unlocking-Knowledge-for-Agents/README.md)                                    | Understand Foundry IQ's core components and how it fits into the agent architecture | [Mar 18, 2026](https://aka.ms/iq-series/episode1)     | [Cookbook](./1-Foundry-IQ-Unlocking-Knowledge-for-Agents/cookbook/)                |
| [Foundry IQ: Building the Data Pipeline with Knowledge Sources](./2-Foundry-IQ-Building-the-Data-Pipeline-with-Knowledge-Sources/README.md)      | Learn how different content enters Foundry IQ from various sources                 | [Mar 25, 2026](https://aka.ms/iq-series/episode2)     | [Cookbook](./2-Foundry-IQ-Building-the-Data-Pipeline-with-Knowledge-Sources/cookbook/) |
| [Foundry IQ: Querying the Multi-Source AI Knowledge Bases](./3-Foundry-IQ-Querying-the-Multi-Source-AI-Knowledge-Bases/README.md)                | Dive into Knowledge Bases and multi-source query paths                             | [Apr 1, 2026](https://aka.ms/iq-series/episode3)     | [Cookbook](./3-Foundry-IQ-Querying-the-Multi-Source-AI-Knowledge-Bases/cookbook/)      |

### Work IQ

Coming soon!

### Fabric IQ

Coming soon!

### Episode Format

Each episode includes:

- **Introduction (1 min)**: Executive speech
- **Tech Talk (15 min)**: Interactive discussion with Product Group + Advocacy
- **Close-out (1 min)**: Doodle summary

Episode folders also include Jupyter notebook cookbooks with hands-on, step-by-step guidance.

## 🚀 Get Started

### Deploy to Azure

Deploy all required Azure resources with one click — this creates AI Search, Azure OpenAI, AI Services, a Foundry project, an AI Search connection, model deployments, and RBAC roles:

[![Deploy to Azure](https://aka.ms/deploytoazurebutton)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fmicrosoft%2Fiq-series%2Fmain%2Finfra%2Fazuredeploy.json)

You'll be prompted for your **User Object ID** (run `az ad signed-in-user show --query id -o tsv` to get it) and can customize the resource prefix, location, and SKUs.

After deployment, create a `.env` file in the repo root with the output values — see the [infra README](./infra/README.md) for details.

> **Prefer the CLI?** You can also deploy via script:
> ```bash
> cd infra
> ./deploy.sh -g "iq-series-rg" -l "eastus2"
> ```
> The script deploys infrastructure and auto-generates the `.env` file. See [infra/](./infra/) for Windows instructions.

### Run the Cookbooks

1. [Fork](https://github.com/microsoft/iq-series/fork) and clone the repository:
   ```bash
   git clone https://github.com/your-org/iq-series.git
   cd iq-series
   ```
2. Navigate to the Episode of your choice and open the cookbook notebook.

## 🙏 Get Involved

We'd love to see you contributing to our repo and engaging with the experts with your questions!

- 🤔 Do you have suggestions or have you found spelling or code errors? [Raise an issue](https://github.com/microsoft/iq-series/issues) or [Create a pull request](https://github.com/microsoft/iq-series/pulls).
- 🚀 If you get stuck or have any questions about Microsoft IQ, join our [Discord](https://aka.ms/iq-series/discord).

## Contributing

This project welcomes contributions and suggestions. Most contributions require you to agree to a Contributor License Agreement (CLA) declaring that you have the right to, and actually do, grant us the rights to use your contribution. For details, visit [https://cla.opensource.microsoft.com](https://cla.opensource.microsoft.com/).

When you submit a pull request, a CLA bot will automatically determine whether you need to provide a CLA and decorate the PR appropriately (e.g., status check, comment). Simply follow the instructions provided by the bot. You will only need to do this once across all repos using our CLA.

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/). For more information, see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.

## Trademarks

This project may contain trademarks or logos for projects, products, or services. Authorized use of Microsoft trademarks or logos is subject to and must follow [Microsoft's Trademark & Brand Guidelines](https://www.microsoft.com/en-us/legal/intellectualproperty/trademarks/usage/general). Use of Microsoft trademarks or logos in modified versions of this project must not cause confusion or imply Microsoft sponsorship. Any use of third-party trademarks or logos is subject to those third parties' policies.
