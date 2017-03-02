# Introduction to Machine Learning: Supervised learning
This document is a layman's primer on some of the general concepts in
Machine Learning, with an emphasis put on Supervised learning. It
assumes no prior knowledge and is not exhaustive.

## Definition and use 
In 1959, Arthur Samuel defined Machine learning as "the subfield of computer science that gives computers the ability to learn without being explicitly programmed". It utilises algorithms to infer decisions, tasks, outcomes, learnings, and predictions based on data.

Its applications are many, but is most valuable where hard-coded programmatic instructions in explicit form would be impractical or inefficient. A couple of examples of use cases are Email spam filters, Character recognition, Speech detection, and Language translation. In these use cases, the algorithms deployed essentially learn and adapt their behaviour based on data. 

Rather than a programmer having to think of all the ways a potential spammer could write spam, and then define rules to filter these out, the algorithm is able to infer rules to apply by comparing spam and non-spam emails. 

## Terminology and use

Name | Description
-----|--------
Data | Facts or stats collected, to be used to drive the performance of the algorithm. 
Features | Specific categories of data that you will be used to drive your prediction. If you're constructing an algorithm to predict the selling price of a house, examples of features to use could be: Number of bedrooms, Property construction year, and Size of interior.
Output | The prediction of the algorithm based on analysing the data.|

## Types of Machine Learning
### Supervised learning
This is distinguished by feeding the algorithm both _inputs_ (i.e. features) as well as _desired outputs_ (i.e. desired  predictions) by a teacher. In the process, we train the algorithm to determine patterns in the features that drive predictions that correspond to those in the data it had access to. In the example of our house price prediction algorithm, we would include housing data that included both the features we had chosen (number of bedrooms, construction year, etc) as well as the actual corresponding outputs (i.e. actual prices the houses sold for). This would then allow the algorithm to make output predictions based on new, previously unseen data of the same features.

#### Logistic regression
#### 
#### Classification
#### 
### Unsupervised learning
### 
#### Clustering
#### 
#### Dimension reduction
#### 
### Reinforcement learning
### 

## A deeper dive into Supervised learning

Features
Cost function
Minimise 

## Basic work process
Iterative and experimental. Determine features. Source data. Clean data.
Divide into buckets. Pick an algorithm. Pick a hypothesis.  
