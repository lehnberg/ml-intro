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

## A closer look at Supervised learning
Here we dive deeper into supervised learning and what is entailed by solving logistic regression and classification problems. Consider the following two examples:


### Objective

Features
Cost function
Minimise 

Algorithms

## Basic work process
Iterative and experimental. Determine features. Source data. Clean data.
Divide into buckets. Pick an algorithm. Pick a hypothesis.  
