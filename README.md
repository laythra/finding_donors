# Machine Learning Nanodegree
## Finding Donors - Supervised Learning Project.

In this project,  i employ several supervised algorithms to accurately model individuals' income using data collected from the 1994 U.S. Census.

The main goal of this project is build a model that will be able to effiecently predict whether a person makes more than 50,000 a year or not.

The project consists of several steps as follows:
### Data Exploration
In this very first step, we will explore our data by calculating how many individuals actually make 50,000$ or above and how many individuals make below 50,000$.
Another important aspect we explore is the featureset, where we examine the features we are given, such as age, workclass, education, etc.

### Preparing the Data


#### logarithmic transformation
In the second step, we prepare our dataset by doing some preprocessing on it, perhaps one of the most common preprossing steps is removing missing features, however in this dataset
we do not have any missing features whatsoever, but many other preprocessing steps are required such as "logarithmic transformation".
we do this in order to gurantee that very high and very small values some of our features might have won't negatively affect the performace of our predicting model.

#### Normalizing Numerical Features
Normalizing our numerical values is in general a good practice, even in image processing, we usually tend to normalize each pixle the image contains.
Normalization convert each value to a value between 0 and 1, which means all values become in the same range, 
which means all features will be treated equally and our model will be less prone to getting negatively affected by outliers.

#### Applying the one-hot encoding scheme
what one-hot encoding bascially does is that it converts categorical variables (Which are the non-numerical values) to numerical ones, since 
our model will be expecting the input to be numeric,

Here is an example of one-hot encoding
![alt text]()





