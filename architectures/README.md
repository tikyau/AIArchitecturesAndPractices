# AI Reference Architectures
This repository contains the recommended ways to train and deploy machine learning models on Azure. It ranges from running massively parallel [hyperparameter tuning using Hyperdrive](https://github.com/Microsoft/MLHyperparameterTuning) to deploying deep learning models on [Kubernetes](https://github.com/Microsoft/AKSDeploymentTutorialAML). Each [tutorial](#tutorials) takes you step by step through the process to train or deploy your model. If you are confused about what service to use and when look at the [FAQ](#faq) below.  

For further documentation on the reference architectures please look [here](https://docs.microsoft.com/en-us/azure/architecture/reference-architectures/).

# Getting Started
This repository is arranged as submodules and therefore you can either pull all the tutorials or simply the ones you want. 
To pull all the tutorials simply run:

```bash
git clone --recurse-submodules https://github.com/Microsoft/AIReferenceArchitectures.git
```

if you have git older than 2.13 run:

```bash
git clone --recursive https://github.com/Microsoft/AIReferenceArchitectures.git
```

# Architectures <a name="Architectures"></a>
| Architectures                                     | Language | Environment | Design | Description                                                                       | Status                                                                                                                                                                                                                                                                                                              |
|----------------------------------------------|-------------|-------------|-------------|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Deploy Classic ML Model on Kubernetes](https://github.com/Microsoft/MLAKSDeployAML)       						   | Python | CPU  | Real-Time Scoring| Train LightGBM model locally using Azure ML, deploy on Kubernetes or IoT Edge for _real-time_ scoring                         | [![Build Status](https://dev.azure.com/AZGlobal/Azure%20Global%20CAT%20Engineering/_apis/build/status/AI%20CAT/Python-ML-RealTimeServing?branchName=master)](https://dev.azure.com/AZGlobal/Azure%20Global%20CAT%20Engineering/_build/latest?definitionId=21&branchName=master)
| [Deploy Deep Learning Model on Kubernetes](https://github.com/Microsoft/AKSDeploymentTutorialAML)    				   | Python | Keras | Real-Time Scoring| Deploy image classification model on Kubernetes or IoT Edge for _real-time_ scoring using Azure ML             | [![Build Status](https://dev.azure.com/AZGlobal/Azure%20Global%20CAT%20Engineering/_apis/build/status/AI%20CAT/Python-Keras-RealTimeServing?branchName=master)](https://dev.azure.com/AZGlobal/Azure%20Global%20CAT%20Engineering/_build/latest?definitionId=17&branchName=master)


# Requirements
The tutorials have been mainly tested on Linux VMs in Azure. Each tutorial may have slightly different requirements such as GPU for some of the deep learning ones. For more details please consult the readme in each tutorial.

## Reporting Issues
Please report issues with each tutorial in the tutorial's own github page.


# FAQ <a name="faq"></a> 
<details>
<summary><em>What service should I use for deploying models in Python? </em></summary>
<p align="center">
  <img width="800" src="images/decision_python_scoring.png">
</p>

When deploying ML models in Python there are two core questions. The first is will it be real time and whether the model is a deep learning model. For deploying deep learning models that require real time we recommend Azure Kubernetes Services (AKS) with GPUs. For a tutorial on how to do that look at [AKS w/GPU](https://github.com/Microsoft/AKSDeploymentTutorialAML). For deploying deep learning models for batch scoring we recommend using AzureML pipelines with GPUs, for a tutorial on how to do that look [AzureML Pipelines w/GPU](https://github.com/Azure/Batch-Scoring-Deep-Learning-Models-With-AML). For non deep learning models we recommend you use the same services but without GPUs. For a tutorial on deploying classical ML models for real time scoring look [AKS](https://github.com/Microsoft/MLAKSDeployAML) and for batch scoring [AzureML Pipelines](https://github.com/Microsoft/AMLBatchScoringPipeline)

</details>

<details>
<summary><em>What service should I use to train a model in Python? </em></summary>
<p align="center">
  <img width="800" src="images/python_training_diag.png">
</p>

There are many options for training ML models in Python on Azure. The most straight forward way is to train your model on a [DSVM](https://azure.microsoft.com/en-us/services/virtual-machines/data-science-virtual-machines/). You can either do this in local model straight on the VM or through attaching it in AzureML as a compute target. If you want to have AzureML manage the compute for you and scale it up and down based on whether jobs are waiting in the queue then you should AzureML Compute. 

Now if you are going to run multiple jobs for hyperparameter tuning or other purposes then we would recommend using [Hyperdrive](https://docs.microsoft.com/en-us/azure/machine-learning/service/how-to-tune-hyperparameters), [Azure automated ML](https://docs.microsoft.com/en-us/azure/machine-learning/service/concept-automated-ml) or AzureML Compute dependent on your requirements.
For a tutorial on how to use Hyperdrive go [here](https://github.com/Microsoft/MLHyperparameterTuning).

</details>

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
