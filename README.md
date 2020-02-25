# Devops-pipelines
Warehouse of notebooks for producing root-cause analysis of Azure DevOps pipeline delays.

Uses both [azure data explorer](https://docs.microsoft.com/en-us/azure/data-explorer/), and [azure notebooks](https://docs.microsoft.com/en-us/azure/notebooks/).

# Usage
## Commands
test
```
# Initialize
!pip install --upgrade pip Kqlmagic nimport azure.kusto.data[pandas]
%load_ext nimport
```

```
# Let's clone our repo, path is not relevant here, this just clones the whole repo
%nimport container="microsoft/devops-pipelines" path="delays.ipynb" provider="github" providerOptions={"clone":"true"}
```

```
# If you have a URL where you want to parse parameters...
from nimport.utils import open_nb, parse_params
params = parse_params(currentUrl)
display(params)
```

```
# Open the notebook by replacing the parameters
open_nb("devops-pipelines/delays.ipynb", params)
```

# Contributing

## Requirements
- Commands

    `pip install pre-commit`

    `pre-commit install`

- Open PRs'!

## Notice

This project welcomes contributions and suggestions.  Most contributions require you to agree to a
Contributor License Agreement (CLA) declaring that you have the right to, and actually do, grant us
the rights to use your contribution. For details, visit https://cla.opensource.microsoft.com.

When you submit a pull request, a CLA bot will automatically determine whether you need to provide
a CLA and decorate the PR appropriately (e.g., status check, comment). Simply follow the instructions
provided by the bot. You will only need to do this once across all repos using our CLA.

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/).
For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or
contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.
