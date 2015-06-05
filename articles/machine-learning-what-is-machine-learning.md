<properties
    pageTitle="What is Azure Machine Learning? | Microsoft Azure"
    description="Explains basic concepts of the fully-managed Machine Learning service on Microsoft Azure you can use to create, operationalize, and monetize solutions."
    services="machine-learning"
    documentationCenter=""
    authors="cjgronlund"
    manager="neerajkh"
    editor="cgronlun"/>

<tags
    ms.service="machine-learning"
    ms.workload="data-services"
    ms.tgt_pltfrm="na"
    ms.devlang="na"
    ms.topic="article"
    ms.date="06/02/2015"
    ms.author="cgronlun;tedway;olgali"/>


# Introduction to machine learning on Microsoft Azure

## What is machine learning?
Machine learning is at work all around you. When you shop online, machine learning helps recommend other products based on what you've purchased. When your credit card is swiped, machine learning helps the bank do fraud detection and notify you if the transaction seems suspicious.

Machine learning is the process of building predictive models that learn from existing data in order to forecast future behaviors, outcomes, and trends.

## What is Machine Learning on Microsoft Azure?

Azure Machine Learning is a powerful cloud-based predictive analytics service that makes it possible to quickly create and deploy analytics solutions.

Azure Machine Learning not only provides tools to model predictive analytics, but also provides a fully-managed service you can use to to publish your predictive models as ready-to-consume web services. Azure Machine Learning provides tools for creating complete predictive analytics solutions in the cloud: Quickly create, test, operationalize, and manage predictive models. You do not need to buy any hardware nor manually manage virtual machines.

[AZURE.INCLUDE [machine-learning-free-trial](../includes/machine-learning-free-trial.md)]

## Build complete machine learning solutions in the cloud

Azure Machine Learning has everything you need to create predictive analytics solutions in the cloud.

### Machine Learning Studio: Create predictive models

Create predictive models in [Machine Learning Studio](machine-learning-what-is-ml-studio.md), a browser-based tool, by dragging, dropping, and connecting modules.

![Predictive analytics experiments in the cloud with Azure Machine Learning Studio](./media/machine-learning-what-is-machine-learning/AzureMLStudio.png)

* Use a large library of [Machine Learning algorithms and modules](https://msdn.microsoft.com/library/azure/f5c746fd-dcea-4929-ba50-2a79c4c067d7) in Machine Learning Studio to jump-start your predictive models. Choose from a library of sample experiments, R and Python packages, and best-in-class algorithms from Microsoft businesses like Xbox and Bing. Extend Studio modules with your own custom  [R](machine-learning-r-quickstart.md) and [Python](machine-learning-execute-python-scripts.md) scripts.
* In [Machine Learning Community Gallery](machine-learning-gallery-how-to-use-contribute-publish.md), you can get started with Azure Machine Learning and learn from others in the community. Try experiments authored by others, ask questions or post comments about experiments, or publish your own experiments. You can also share links to experiments via social networks such as LinkedIn and Twitter.  

	![Try predictive experiment samples or contribute your own in Azure Machine Learning Gallery](./media/machine-learning-what-is-machine-learning/AzureMLGallery.png)

### Operationalize predictive analytics solutions: Purchase web services or publish your own

* Purchase ready-to-consume web services from [Mirosoft Azure Marketplace](https://datamarket.azure.com/browse?query=machine+learning), such as Recommendations, Text Analytics, and Anomaly Detection.

* Operationalize your predictive analytics models:
    * [Publish web services](machine-learning-publish-a-machine-learning-web-service.md).
    * [Train and retrain models through APIs](machine-learning-retrain-models-programmatically.md).
    * [Manage web service endpoints](machine-learning-create-endpoint.md).
    * [Scale web services](machine-learning-scaling-endpoints.md).

## Key machine learning terminology and concepts
### Data exploration, descriptive analytics, and predictive analytics

**Data exploration** is the process of gathering information about a large and often unstructured data set in order find characteristics for focused analysis. **Data mining** refers to automated data exploration.

**Descriptive analytics** is the process of analyzing a data set in order to summarize what happened. The vast majority of business analytics - such as sales reports, web metrics, and social networks analysis - are descriptive.

**Predictive analytics** is the process of building models from historical or current data in order to forecast future outcomes.


### Supervised and unsupervised learning
 **Supervised learning** algorithms are trained with labeled data - in other words, data comprised of examples of the answers wanted. For instance, a model that identifies fraudulent credit card use would be trained from a data set in which data points indicating known fraudulent and valid charges were labeled. Most machine learning is supervised.

 **Unsupervised learning** is used on data with no labels, and the goal is to find relationships in the data. For instance, you might want to find groupings of customer demographics with similar buying habits.

### Model training and evaluation
A machine learning model is an abstraction of the question you are trying to answer or the outcome you want to predict.

#### Training from data
In Azure Machine Learning, a model is the combined product of training data fed through an algorithm module and functional modules, such as a scoring module.

In supervised learning, training a model involves using data for which you know the outcomes. If you're training a fraud detection model, you'll use a set of transactions that are labeled as fraudulent or valid. You'll split your data set randomly, and use part to train the model and part to test or evaluate the model.

#### Evaluation data
Once you have a trained model, evaluate the model using the remaining test data. You use data you already know the outcomes for, so that you can tell whether your model predicts accurately.

### Other common machine learning terms

* **algorithm**: A self-contained set of rules used to solve problems through data processing, calculation, or automated reasoning.
* **categorical data**: Data that is organized by categories and that can be divided into groups. For example a categorical data set for autos could specify year, make, model, and price.
* **classification**: A model for organizing data points into categories based on a data set for which category groupings are already known.
* **feature engineering**: The process of extracting or selecting features related to a data set in order to enhance the data set and improve outcomes. For instance, airfare data could be enhanced by days of the week and holidays. See [Feature selection and engineering in Azure Machine Learning](machine-learning-feature-selection-and-engineering.md).
* **module**: A functional element in a Machine Learning Studio model, such as the Enter Data module which enables entering and editing small data sets. An algorithm is also a type of module in Machine Learning Studio.
* **model**: For supervised learning, a model is the product of a machine learning experiment comprised of a training data set, an algorithm module, and functional modules, such as a Score Model module.
* **numerical data**: Data that has meaning as measurements (continuous data) or counts (discrete data). Also referred to as *quantitative data*.
* **partition**: The method by which you divide data into samples. See [Partition and Sample](https://msdn.microsoft.com/library/azure/dn905960.aspx) for more information.
* **prediction**: A prediction is a forecast of a value or values from a machine learning model. You might also see the term "predicted score"; however, predicted scores are not the final output of a model. An evaluation of the model follows the score.
* **regression**: A model for predicting a continuous value based on independent variables, such as predicting the price of a car based on its year and make.
* **score**: A predicted value generated from a trained classification or regression model, using the [Score Model module](https://msdn.microsoft.com/library/azure/dn905995.aspx) in Machine Learning Studio. Classification models also return a score for the probability of the predicted value. Once you've generated scores from a model, you can evaluate the model's accuracy using the [Evaluate Model module](https://msdn.microsoft.com/library/azure/dn905915.aspx).
* **sample**: A part of a data set intended to be representative of the whole. Samples can be selected randomly or based on specific features of the data set.



## Next steps
You can learn the basics of predictive analytics and machine learning using a [step-by-step tutorial](machine-learning-create-experiment.md) and by [building on samples](machine-learning-sample-experiments.md).  


<!-- Module References -->
[learning-with-counts]: https://msdn.microsoft.com/library/azure/81c457af-f5c0-4b2d-922c-fdef2274413c/
