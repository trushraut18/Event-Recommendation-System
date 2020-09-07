# Event Recommendation System

## Files Description
1) EmployeeDataset.csv
=> (Name,Domain,Preference1,Preference2)
=> This csv file is an employee dataset contains 225 rows and 4 columns.Name of the employee starts with Last name followed by First name.
2) code.py
=> This file contain entire code of event recommendation system.
3) events.csv
=> This csv file is an event dataset contains description of 42 rows 
4) results.xlsx
=> This excel file is output file which contains recommended employees with event name.

## Problem Description

 This Recommender System will recommend relevant events to each employee  based 
 on their preference.First it will check for preference1 and then preference2.
 At last employee names with the particular event excel sheet will be autogenerated.

## Tools & Libraries

A machine learning library provides capabilities for completing part of a machine learning
project. For example a library may provide a collection of modeling algorithms.
Features of machine learning libraries are:

1) They provide a specific capability for one or more steps in a machine learning project.
2) The interface is typically an application programming interface requiring programming.
3) They are tailored for a specific use case, problem type or environment.

Scikit-learn (sklearn) is a free software machine learning library for the Python
programming language.It features various classification, regression and clustering algorithms
including support vector machines, random forests, gradient boosting, k-means and DBSCAN,
and is designed to interoperate with the Python numerical and scientific libraries NumPy and
SciPy.

Pandas is a software library written for the Python programming language for data
manipulation and analysis. In particular, it offers data structures and operations for manipulating
numerical tables and time series.

The Natural Language Toolkit, or more commonly NLTK, is a suite of libraries and
programs for symbolic and statistical natural language processing (NLP) for English written in the
Python programming language.

Numpy is a library for the Python programming language, adding support for large,
multi-dimensional arrays and matrices, along with a large collection of high-level mathematical
functions to operate on these arrays.

I have used pandas for reading csv files and managing dataframes. I have used sklearn’s
metrics.pairwise for cosine_similarity and feature_extraction.text for CountVectorizer.Also nltk is
used for stopwords, lemmatization etc.Numpy is used for mathematical computations.

## Methodology
Recommendation Systems can be approached in various ways . It can be implemented
using some machine learning algorithms like K Means Clustering,Random Forest ,etc. But the
problem with these machine learning algorithms is overfitting where the model tries to learn the
data and produce high training accuracy and low test accuracy. And in addition to that, the kind
of problem statement given to us was completely different in context of machine learning
algorithms.
The approach followed in developing this system is Natural Language Processing(NLP).

NLP works better in recommendation systems.It retrieves the information from the dataset and
tries to find similarity between them.Natural language refers to the way we, humans,
communicate with each other.
Also the type of recommendation system applied plays important role.Recommendation
systems can be classified into two broad categories:
- Collaborative filtering
- Content-based filtering

Collaborative filtering takes advantage of a user's past behavior as well as decisions made by
similar users or friends of the user. Content-based filtering concentrates on similarities between
products to make relevant recommendations. In this project, we followed a content-based
filtering approach where we use employee domain info as well as their preferences to
recommend them a choice of events they preferred.

## Data Preprocessing

Data Preprocessing is one of the most important parts in the machine learning pipeline.
Data needs to be converted into a clean dataset so that the machine will be able to do required
computation.Proper structured data helps achieving better accuracy.Also data need not contain
duplicate value and hence complete analysis needs to be done on the dataset.
During preprocessing,one needs to understand the important,not important,dependents
constraints.To increase the model efficiency ,it is always advisable to drop some columns if not
necessary.
The Employee dataset is free from null values but still it needs to be
processed for the future work.And events dataset is prepared for the domain classification.

## Feature Extraction

Data preprocessing and feature extraction is a critical step as it needs to extract the most
important features from a given amount of data. .

Features were self explanatory.First feature was employee’s domain which tells about
which domain employee belongs to,which will apparently tell our model to decide events with
respect to domain too.Next features was Event1 and Event2. Event1 is the first preference type of
employee while Event 2 was the second preference. After evaluation,there were a total 23
employee domains and 13 types of events like certification,internship,etc.
As said earlier, event.csv contains only one column of event details and hence it was only
a feature.Recommendation system was supposed to convert events into various domains it
belongs to and then recommending the names of employees who belong to that domain.
Features were limited and none of them was a factor to skip.I take all features and make a
bag of words which will describe the employee .Bag of words contain merged columns like
domain,Event1,Event2.

## Techniques Used

Cosine Similarity measures the cosine of the angle between two non-zero vectors of an
inner product space. This similarity measurement is particularly concerned with orientation, rather
than magnitude. In short, two cosine vectors that are aligned in the same orientation will have a
similarity measurement of 1, whereas two vectors aligned perpendicularly will have a similarity of
0. In a simple way, if similarity is equal to 1 or near to 1 , they are said to be more. Similarity score
near to zero represents items to be less similar.

Moreover,If two vectors are diametrically opposed, meaning they are oriented in exactly
opposite directions (i.e. back-to-back), then the similarity measurement is -1. Often, however,

Cosine Similarity is used in positive space, between the bounds 0 and 1. Cosine Similarity is not
concerned, and does not measure, differences is magnitude (length), and is only a representation
of similarities in orientation.

Scikit-learn’s CountVectorizer is used to convert a collection of text documents to a
vector of token counts. It also enables the pre-processing of text data prior to generating the
vector representation. This functionality makes it a highly flexible feature representation module
for text.
Count vectorization is used to transform the bag of words into a matrix. I have
implemented cosine similarity using a bag of words which is made up of domains and event
preferences.Then cosine similarity matrix is used by a recommendation function which will
predict the employee names based on employee preferences.

## Conclusion And Future Work

Recommendation Systems have great value in recommending relevant resources to
users. A good recommender system should be able to provide positive and relevant
recommendations from time to time and also provide alternative recommendations to break the
fatigue of the users seeing the same items in the recommendation list.In future ,Recommender
Engines will be more efficient and more likely to adapt human psychology and mentality towards
particular thing.
This Event Recommendation System can be extended by adding more functionalities like
recommending events based on location you’re near to,based on you community or friends.And
according to that,Employee will get an email notification with complete detail of that event.


# Thank You !
