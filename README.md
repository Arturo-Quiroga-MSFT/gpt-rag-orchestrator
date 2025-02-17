# gpt on your data orchestrator

Part of [gpt-rag](https://github.com/Azure/gpt-rag)

## Quick start - Deploy to Azure

**1) Pre-reqs**

- Azure Funcion App
- Azure OpenAI Service*
- Cognitive Search Service**
- Index created by [ingestion](https://github.com/Azure/gpt-rag-ingestion)
- CosmosDB Service
- Python 3.10 and PIP

\* Azure OpenAI Service with the following deployments:  chat (*gpt35-turbo or gpt4 model*) and text-embedding-ada-002 (*text-embedding-ada-002 model*).<br>
\*\* Azure Cognitive Search Service with [Vector Index](https://github.com/Azure/cognitive-search-vector-pr/) feature enabled.

**2) Set Application Settings**

- Rename [local.settings.json.template](local.settings.json.template) to ```local.settings.json``` and update environment variables in this file to run orchestrator locally.
- In Azure Portal > Function App > Configuration > Application Settings: add the same variables you updated in locall.settings.json.

You can add additional variables to application settings if you don't want to use the default values.

**3) Deploy locally** - This is to test the solution and make sure that is working fine, once is tested using Postman, you can proceed with the next step.

With Azure Function extension installed you just need to open ```orc/orchestrator.py``` and "Start Debugging" in VSCode. It will start the server in ```http://localhost:7071/api/orc```.

**4) Deploy to Azure** 

In VSCode with [Azure Function App Extension](https://marketplace.visualstudio.com/items?itemName=ms-azuretools.vscode-azurefunctions) go to the *Azure* Window, reveal your Function App in the resource explorer, right-click it then select *Deploy*.

## Contributing

This project welcomes contributions and suggestions.  Most contributions require you to agree to a
Contributor License Agreement (CLA) declaring that you have the right to, and actually do, grant us
the rights to use your contribution. For details, visit https://cla.opensource.microsoft.com.

When you submit a pull request, a CLA bot will automatically determine whether you need to provide
a CLA and decorate the PR appropriately (e.g., status check, comment). Simply follow the instructions
provided by the bot. You will only need to do this once across all repos using our CLA.

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/).
For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or
contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.

## Trademarks

This project may contain trademarks or logos for projects, products, or services. Authorized use of Microsoft
trademarks or logos is subject to and must follow
[Microsoft's Trademark & Brand Guidelines](https://www.microsoft.com/en-us/legal/intellectualproperty/trademarks/usage/general).
Use of Microsoft trademarks or logos in modified versions of this project must not cause confusion or imply Microsoft sponsorship.
Any use of third-party trademarks or logos are subject to those third-party's policies.
