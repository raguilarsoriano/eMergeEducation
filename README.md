# eMergeEducation

The focus of this project is to contribute to the reduction of academic dropout and failure in higher education, by using machine learning techniques to identify students at risk at an early stage of their academic path, so that strategies to support them can be put into place. 

# Content

Within this repository you can find the data source we use to feed the models and make our predictions, which you can also download [here](https://archive.ics.uci.edu/dataset/697/predict+students+dropout+and+academic+success "here")
In addition, you will find a Jupyter notebook where the process that was carried out for the analysis of the dataset and the training of the models and a file containing the dictionary for the features.

# Summary

Education is a vital component for socioeconomic development of the individual, community and the country.Education affects employment  opportunities and ability to face the challenges of society.Education is extremely important for acquiring skills and knowledge essential for surviving in the current society and due to the fact many students who drop out or fail end up earning very low income, limiting their social and economic wellbeing and losing opportunities. Leaving school at an early stage leaves learners unprepared for the life situations making it hard for them to uplift their living conditions.

This project analyses the possible causes and factors responsible for dropout in schools and formulates models for classification and prediction of the students as the potential drop out from the school or not based on these factors.This models uses various  machine learning classification techniques and tries to find out the best possible technique for classification and prediction based on accuracy of results.

### Data Understanding

The dataset contains information gathered from multiple disconnected databases within a higher education institution, focusing on students enrolled in various undergraduate degree programs. The dataset includes information known at the time of student enrollment – academic path, demographics, and social-economic factors. 
The problem is formulated as a three category classification task (dropout, enrolled, and graduate) at the end of the normal duration of the course. 

According to the dataset providers, extensive data preprocessing was conducted to address anomalies, unexplainable outliers, and missing values. Despite this effort, certain transformations are still required to prepare the dataset for the next phase, which involves model-building.

Surprisingly, it was discovered that all columns containing categorical data are encoded using a non-linear scale. While the reason for this unconventional encoding remains unknown, the meanings of the numbers are now understood. Therefore, we have decided to convert the existing non-linear scale into a linear one to ensure better interpretability and compatibility with the upcoming modeling process.

After analyzing the different features we came to the conclusion that they are all important. Below is a table some of the 36 features:

|Name|Type|    
|----|-----|
|Marital status|int64|
|----|-----|
|Application mode|int64|
|----|-----|
|Admission grade|float64|
|----|-----|
|Course|int64|
|----|-----|
|Daytime/evening attendance|int64|
|----|-----|
|Nacionality|int64|
|----|-----|
|Gender|int64|
|----|-----|
|Scholarship holder|int64|
|----|-----|
|Age at enrollment|int64|
|----|-----|
|Unemployment rate|float64|

To have more details of each feature please check the features dictionary [here](link of the csv "here").

###  Data Modelling

There are different types of models for data classification problems. Each model has its own strengths and weaknesses in a given scenario. There is no cut-and-dried flowchart that can be used to determine which model you should use without grossly oversimplifying the considerations. Choosing a data classification model is also closely tied to the business case and a solid understanding of what you are trying to accomplish.

We decided to start with a decision tree, and scale it to XGBoost and end with Histogram-based Gradient Boosting Classification Tree to compare the accuracy score of each model and determine which would be the best for this project.

### Model Evaluation
After training the models we end up with these results for the accuracy score, having greater success with the Histogram-based Gradient Boosting Classification Tree model.

[images are going to be inserted here]