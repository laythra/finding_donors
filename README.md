# Machine Learning Nanodegree
## Finding Donors - Supervised Learning Project.
### Please head to the "finding_donors.ipynb" Jupyter Notebook to see the project along with a description of each step.

In this project, i employ several supervised machine learning algorithms to accurately model individuals' income using data collected from the 1994 U.S. Census.
The main goal of this project is to build a model that will be able to efficiently predict whether a person makes more than 50,000 a year or not.

The project consists of several steps:

### Data Exploration
In this very first step, we will explore our data by calculating how many individuals actually make 50,000$ or above and how many individuals make below 50,000$.
Another important aspect we explore is the feature-set, where we examine the features we are given, such as age, workclass, education, etc.

### Preparing the Data

#### logarithmic transformation
In the second step, we prepare our dataset by doing some preprocessing on it, perhaps one of the most common preprocessing steps is removing missing features, however in this dataset
we do not have any missing features whatsoever, but many other preprocessing steps are required such as "logarithmic transformation".
we do this in order to guarantee that very high and very small values some of our features might have won't negatively affect the performance of our predicting model.

#### Normalizing Numerical Features
Normalizing our numerical values is in general a good practice, even in image processing, we usually tend to normalize each pixel the image contains before fitting that image into a model (such as a CNN for example).
Normalization converts each value to a value between 0 and 1, which means all values become in the same range,
which means all features will be treated equally and our model will be less prone to getting negatively affected by outliers.

#### Applying the one-hot encoding scheme
what one-hot encoding basically does is that it converts categorical variables (Which are the non-numerical values) to numerical ones, since
our model will be expecting the input to be numeric.

Here is an example of one-hot encoding
![alt text]()

#### Splitting our data into testing and training sets.
Splitting our data is extremely important, since we need to have a subset of our data that our model has never seen before in order to test the performance of this model seeing how well our model on these never seen before data points, i use the 'train_test_split' function provided by the sklearn module to do this job.

### Evaluating Metrics
In the next step i define some of the evaluating metrics the could be used to evaluate the performance of our model, such as:
- Accuracy
- Precision
- Recall
Or we could use something called the **F-beta score** which takes into consideration both precision and recall.

### Implementing our model

#### Naive Model
The first approach i try is making a naive model that always assumes that a person makes more than 50,000$. after calculating the accuracy and the F-score for this model is get a score of 0.2478 for the accuracy and a score of 0.2917 for the F-score, which is not good at all, hence it's called "naive".

#### Trying out more models
In this step, i start implementing more models, and discuss each model's advantages and disadvantages, the models i will be using are **Decision Tree**, **Support Vector Machine** and **K-nearest neighbors (KNN)**

I trained each model using our training set and tested it using the testing set, after that i did some visualization to get a better grasp of how our models performed
![alt text]()

I ended with the conclusion that Decision Trees would work best for our data as you will be able to see in the project file.

### Model Tuning
After we picked our Decision Tree classifier to be the best model for this data, we started tuning some of its parameters in order to optimize our model more.

Here are the results I ended up with before and after optimizing our model:

Unoptimized model
------
Accuracy score on testing data: 0.8182
F-score on testing data: 0.6272

Optimized Model
------
Final accuracy score on the testing data: 0.8408
Final F-score on the testing data: 0.6792

Which are pretty good, specially if we compare these scored to our first naive model scores.


### Extracting Feature Importance
Using the **feature_importance_** our Decision Tree classifier module has, we can rank the importance of each of our 13 features that we have in our dataset.
![alt text]()

after that we fit our Decision Tree classifier with a subset of our dataset, which contains only the 5 most important features in our dataset as seen in the picture above, then we compare the scores we get from this model with the previous model that was trained using all of the 13 features, here are the results we end up with:


Final Model trained on full data
------
Accuracy on testing data: 0.8408
F-score on testing data: 0.6792

Final Model trained on reduced data
------
Accuracy on testing data: 0.8399
F-score on testing data: 0.6807

























