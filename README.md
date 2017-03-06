# Introduction to Machine Learning: Supervised learning
This document is a layman's primer on some of the general concepts in
Machine Learning, with an emphasis put on Supervised learning concepts. It
assumes no prior knowledge and is not exhaustive.

## Definition and use 
In 1959, Arthur Samuel defined Machine learning as "the subfield of computer science that gives computers the ability to learn without being explicitly programmed". It utilises algorithms to infer decisions, tasks, outcomes, learnings, and predictions based on data.

Its applications are many, but is most valuable where hard-coded programmatic instructions in explicit form would be impractical or inefficient. A couple of examples of use cases are Email spam filters, Character recognition, Speech detection, and Language translation. In these use cases, the algorithms deployed essentially learn and adapt their behaviour based on data. 

Rather than a programmer having to think of all the ways a potential spammer could write spam, and then define rules to filter these out, the algorithm is able to infer rules to apply by comparing spam and non-spam emails. 

## Terminology

Name | Description
-----|--------
Data | Facts or stats collected, to be used to drive the performance of the algorithm. 
Features | Specific categories of data that you will be used to drive your prediction. If you're constructing an algorithm to predict the selling price of a used car, examples of features to use could be: Make, Model, Model Year, and Engine size.
Output | The prediction of the algorithm based on analysing the data.|

## Types of Machine Learning
### Supervised learning
This is distinguished by feeding the algorithm both _inputs_ (i.e. features) as well as _desired outputs_ (i.e. desired  predictions) by a teacher. In the process, we train the algorithm to determine patterns in the features that drive predictions that correspond to those in the data it had access to. In the example of our house price prediction algorithm, we would include car data that included both the features we had chosen (Make, model, etc) as well as the actual corresponding outputs (i.e. actual prices those cars had sold for). This would then allow the algorithm to make output predictions based on new, previously unseen data with the same features.

#### Logistic regression
A type of supervised learning problem, logistic regression is used to make predictions on a continuous scale. Treating our used car sale prediction algorithm as a logistic regression problem, we would be able to predict the sale price as the output. Another example would be to use previous race data to predict the time it would take for an athlete to run 100m given certain conditions. Since time and money are on a continuous scale, logistic regression is suitable.   
#### Classification
Another type of supervised learning is classification. Here, the algorithm is used to make binary predictions, to label the data. In our car price prediction alogrithm, we could use classification to generate predictions on whether a car would sell above $100k (yes/no). Or the type of animal that is displayed on a photograph (dog/cat/bird/neither). Or to determine whether an email received should be marked as "spam" or "not spam".
### Unsupervised learning
In unsupervised learning, the role of the trainer is removed and you are not labeling the data. The machine learning algorithm is left to best make sense of the data on its own. It can be an end in itself (to understand properties and patterns of a dataset), or it could help achieve a wider goal (by identifiying features to be used in Supervised learning). 
#### Clustering
Similarly to a Classification problem, in Clustering data is sorted into groups. Only here the types of clusters are not known in advance. An example of clustering is news agreggation, identifying patterns of similarity in texts and articles.  
#### Dimension reduction
This technique is used to eliminate random features or variables in a dataset that has little or no impact on the output, at the same time reducing complexity of the model. 
### Reinforcement learning
Here, the algorithm is assigned a deterministic goal, like successfuly driving a car from point A to point B, winning a game of Go, or completing a level in a video game. Based on its perfomance, punishments or rewards are given to incentvize correct actions and thus hone the algorithm's skill over time as it makes many attempts.
## Working with Supervised learning
Here we dive deeper into supervised learning and what is entailed by solving logistic regression and classification problems. 
### Objective: Minimising the cost
Supervised learning is essentially an optimization problem. You have a data set, consisting of different features that, based on their configuration, have produced a specific output. The task of the algorithm is to produce a model based on this data that can make as accurate predictions as possible. These predictions will seldomly be entirely accurate. The _true value_ will differ from the by the model _predicted value_. As the true value is known in the training data, the model can work to minimize the difference between those and its predictions. This difference is referred to as the _Cost_, and the lower the cost, the more inline the predictions are with the actual results.
### An iterative process
There is little point in trying to design the perfect model from the start, and it's hard to predict what will work and what will not before starting to work practically with the data. Improving the performance of a model is an iterative process, and it's better to start somewhere simple, to learn, and refine as needed.
### Selecting an Algorithm
There is a [myriad](https://en.wikipedia.org/wiki/Machine_learning#Approaches) of Machine Learning algorithms, everything from ever so popular Neural Networks to traditional linear regression algorithms like Gradient Descent. It's less important which algorithm you start with, what matters is that you begin the effort and can see how it performs against your dataset. Pick an algorithm that's simple enough for you to be able to implement fast, and then take it from there.
### Working with data 
The fewer features you have to drive a model that produces high accuracy, the better. Naturally, the more sample data you can obtain for these features, the better. In general, the availability of data tends to beat sophisiticated optimization algorithms. The first step once data is obtained will be to clean it, feature scale it, and mean normalise it, in order to imprve the performance. The data is then split into three distinct sets:

1. **Training set**, used to build the model (60-80% of all data)

1. **Cross-validation set**, used to troubleshoot/sanity check the model (10-20% of data)

1. **Test set**, used to test evaluate the model's prediction accuracy (10-20% of data)

This way, the data used to test the model has not been used in any way when the model is built. This eliminates any bias in the model coming from using the data you want to test agains to train your model.

### Troubleshooting & Error analysis
Debugging your model is as important as building it. Comparing the performance of the model applied to the Training set data against when applied to the Cross Validation data gives an idea of how well the model can make predictions and what can be made to improve it further.
#### Overfitting vs Underfitting
When the model is _overfitting_ the data, it fails to produce accruate predictions against data outside of the Training set. It implies that the model is overdesigned to fit that specific data, there is a lot of random noise included, and that the model doesn't generalize well. This can be a sign that too many features are being used and that they do not contribute to accurate predictions outside of the Training set. Conversely, _underfitting_ suggests that the model could be too simple; it does not captue the underlying trend of the data and you do not get accurate predictions at all. It's a sign of a too simple model being used.
Regularization is a mathematical tool that can be used to introduce more data into the model to make it generalise better, and can help to prevent overfitting. 
#### Classification errors
When working on classification errors, you can get insights from understanding the types of errors the model makes, as per below.

 | Actual Spam | Actual Non-Spam
----|-----|--------
**Predicted Spam** | True Positive | False Positive 
**Predicted Non-Spam** | False Negative | True Negative

Using this, you can then determine the _precision_ and _recall_ of the model which is used to understand how accurate the model is in making accurate classification predictions.
