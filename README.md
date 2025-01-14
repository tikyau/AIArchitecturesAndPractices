# Azure AI Reference Architectures & Best Practices
Official Azure Reference Architectures and Best Practices for AI workloads 

# Getting Started
This repository is arranged as submodules and therefore you can either pull all the tutorials or simply the ones you want. 
To pull all the tutorials simply run:

```bash
git clone --recurse-submodules https://github.com/dciborow/AIArchitecturesAndPractices.git
```

if you have git older than 2.13 run:

```bash
git clone --recursive https://github.com/dciborow/AIArchitecturesAndPractices.git
```

# Best Practices <a name="Best Practices"></a>
| Title | Description | 
|-------|-------------|
|[Computer Vision](https://github.com/microsoft/computervision)| Accelerate the development of computer vision applications with examples and best practice guidelines for building computer vision systems
|[Naturel Language Processing](https://github.com/microsoft/nlp)|State-of-the-art methods and common scenarios that are popular among researchers and practitioners working on problems involving text and language.|
|[Recommenders](github.com/microsoft/recommenders)| Examples and best practices for building recommendation systems, provided as Jupyter notebooks.| 

# Reference Architectures <a name="Reference Architectures"></a>
| Title                                     | Language | Environment | Design | Description                                                                       | Status                                                                                                                                                                                                                                                                                                              |
|----------------------------------------------|-------------|-------------|-------------|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Deploy Classic ML Model on Kubernetes](https://github.com/dciborow/AIArchitecturesAndPractices/tree/master/architectures/Python-ML-RealTimeServing)       						   | Python | CPU  | Real-Time Scoring| Train LightGBM model locally using Azure ML, deploy on Kubernetes or IoT Edge for _real-time_ scoring                         | [![Build Status](https://dev.azure.com/AZGlobal/Azure%20Global%20CAT%20Engineering/_apis/build/status/AI%20CAT/Python-ML-RealTimeServing?branchName=master)](https://dev.azure.com/AZGlobal/Azure%20Global%20CAT%20Engineering/_build/latest?definitionId=21&branchName=master)
| [Deploy Deep Learning Model on Kubernetes](https://github.com/dciborow/AIArchitecturesAndPractices/tree/master/architectures/Python-Keras-RealTimeServing)    				   | Python | Keras | Real-Time Scoring| Deploy image classification model on Kubernetes or IoT Edge for _real-time_ scoring using Azure ML             | [![Build Status](https://dev.azure.com/AZGlobal/Azure%20Global%20CAT%20Engineering/_apis/build/status/AI%20CAT/Python-Keras-RealTimeServing?branchName=master)](https://dev.azure.com/AZGlobal/Azure%20Global%20CAT%20Engineering/_build/latest?definitionId=17&branchName=master)

# Best Practices with Reference Architectures <a name="Architectures"></a>
| Title                                     | Practice | Language | Environment | Design | Description                                                                       | Status                                                                                                                                                                                                                                                                                                              |
|-------------------------------------------|----------|----------|-------------|-------------|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Building a Real-time Recommendation API](https://github.com/microsoft/recommenders/blob/master/notebooks/05_operationalize/als_movie_o16n.ipynb)       						   | Recommenders | PySpark | CPU  | Real-Time Scoring| Walks through the creation of appropriate azure resources, training a recommendation model using Azure Databricks and deploying it as an API.|


## Recommend a Scenario
If there is a particular scenario you are interested in seeing a tutorial for please fill in a [scenario suggestion](https://github.com/Microsoft/AIReferenceArchitectures/issues/new?assignees=&labels=&template=scenario_request.md&title=%5BSCENARIO%5D)

## Ongoing Work
We are constantly developing interesting AI reference architectures using Microsoft AI Platform. Some of the ongoing projects include IoT Edge scenarios, model scoring on mobile devices, add more... To follow the progress and any new reference architectures, please go to the AI section of this [link](https://docs.microsoft.com/en-us/azure/architecture/reference-architectures/).

# Contributing

This project welcomes contributions and suggestions.  Most contributions require you to agree to a
Contributor License Agreement (CLA) declaring that you have the right to, and actually do, grant us
the rights to use your contribution. For details, visit https://cla.microsoft.com.

When you submit a pull request, a CLA-bot will automatically determine whether you need to provide
a CLA and decorate the PR appropriately (e.g., label, comment). Simply follow the instructions
provided by the bot. You will only need to do this once across all repos using our CLA.

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/).
For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or
contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.
