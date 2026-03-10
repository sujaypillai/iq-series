# Episode 2 Cookbook: Building the Data Pipeline with Knowledge Sources

This folder contains the hands-on cookbook for Episode 2 of The IQ Series.

> **💡 Tip:** You can deploy all required Azure resources automatically with the **Deploy to Azure** button — see the [Episode 1 README](../../1-Foundry-IQ-Unlocking-Knowledge-for-Agents/README.md#-deploy-azure-resources) for details.

## 📓 Cookbook Notebook

The [**Foundry IQ Cookbook**](./foundry-iq-cookbook.ipynb) walks you through building the data pipeline with Knowledge Sources, step by step:

1. Understanding Knowledge Source types (indexed vs. remote)
2. Creating a search index and uploading sample product data
3. Creating an indexed Knowledge Source (Azure AI Search)
4. Creating a Blob Storage Knowledge Source (automated ingestion pipeline)
5. Creating a Web Knowledge Source (real-time public information)
6. Combining multiple sources in a single Knowledge Base
7. Querying across sources and inspecting the activity log
8. Security and governance considerations

### Quick Start

1. Install dependencies: `pip install -U azure-search-documents==11.7.0b2 azure-identity python-dotenv`
2. Create a `.env` file with your endpoint values (see the notebook for details)
3. Open `foundry-iq-cookbook.ipynb` in VS Code or Jupyter and run the cells

## Additional Resources

- [Episode 2 README](../README.md)
- [Microsoft Foundry Documentation](https://learn.microsoft.com/azure/ai-foundry/)
- [Knowledge Sources Overview](https://learn.microsoft.com/azure/search/agentic-retrieval-how-to-create-knowledge-source)
