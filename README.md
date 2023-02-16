# Student-Performance prediction

## Purpose of the project:

Almost all performance prediction models foucus on predicting how well the student will perform at the end of the year/semester in terms of grades. Using the past students' grades, they predict the upcoming students grades. However, this model is a bit different. Its purpose is to predict whether a student will pass/fail the course during the semester based on his/her grades during two stages: 20% and 50% of the course work. This can help the student to decide whether to compelete or withdraw the course in order not to deduct his/her GPA.

##Project data:

In this project, we used the [Student-Performance-and-Engagement](https://github.com/Western-OC2-Lab/Student-Performance-and-Engagement-Prediction-eLearning-datasets) dataset offered by Western-OC2 lab. We used the binary-Student-Performance dataset and Muliclass-Student-Performance datasets only.

The data consists of the following features:
|Feature|	Description|	Type |	Value/s |
|:--- |:--- |:--- |:---|
|Student Id	| Student identifier |	Nominal |	std000, …, std485|
|Quiz01|	Quiz1 Mark	| Numeric |	0,…,100 |
| Assign.01|	Assign.01 Mark|	Numeric|	0,…,100|
|Midterm|	Midterm Mark|	Numeric|	0,…,100|
|Assign.02|	Assign.02 Mark|	Numeric|	0,…,100|
|Assign.03|	Assign.03 Mark|	Numeric|	0,…,100|
|Final Exam|	Final Exam Mark|	Numeric|	0,…,100|
|Final Grade|	Total Final Mark|	Numeric|	0,…,100|
|Student Category|	Final Grade|	Nominal|	G,W|

## Project steps:
During building this project, we followed a scientific paper which addressed the same issue. All out hyperparameters are taken from this paper. The paper can be found [here](https://www.sciencedirect.com/science/article/abs/pii/S0950705120302999).

  * Data analysis steps:
      
      * There were not many steps during our data analysis step as the data was already clean and normalized. However, we performed 4 steps:
          
          * We drew the histograms of all our attributes to get an insight about their distributons.
          * We performed PCA (Principal components analysis) to reduce the features to only 2 features for data plotting and to decide which features contribute the 
              most to the data or which features holds the greater variance in our data.
          
          * We noticed that our target feature (Final Grade) is not balanced, so we cannot use accuracy as our model performance metric. So, we decided to deal with 
            issue in two ways:
              
              * We used oversampling using SMOTE and ADASYN in order to balance the categories and then use accuracy as performance metric.
              * Leave the categories as they are ans use recall, percision, F1, and ROC-AUC scores as performance metices as they can deal with skewe categories.
  
  * Training steps:
    
    * We used five learning methods to train out model: 
      
      * Support-Vector-Machine
      * Random Forest
      * K-nearest neighbors.
      * Multiple layer perceptron.
      * Naive Bayes.
      
    * All of the hyperprameters can be found in the paper as mentioned above.

## Installation:

Just download the notebook, import it in Jupyter or Colab and run it!
  
              


