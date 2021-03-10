##### CapstoneThreeProject
![alt text](https://medcitynews.com/uploads/2020/07/GettyImages-1165309517-600x400.jpg)
# Breast Cancer Prediction

One in eight women in the United States will get breast cancer in their lifetime. Thankfully, advancements in medicine and technology have made treatments safer and more effective than ever before, but the diagnosis is still scary.  If a tumor is found, it is important to find out as quickly as possible if the tumor is benign or if it malignant and spreading.  In this project, I used the [Wisconsin Breast Cancer Dataset](https://www.kaggle.com/uciml/breast-cancer-wisconsin-data) from kaggle that took the characteristics of tumors found, and I want to use it to predict the likelihood of future tumors being benign or malignant.

### 1. Project Proposal

I wanted to model this project as if I were in a business setting and proposing the idea to a company.  [This proposal](https://github.com/dawgtree/CapstoneThreeProject/blob/main/Capstone%203%20Project%20Proposal.pdf) explains my goals and the steps that I plan on taking to complete them.

### 2. Data Wrangling and Cleaning

In [this notebook](https://github.com/dawgtree/CapstoneThreeProject/blob/main/Cancer%20Diagnosis%20Capstone%20Project%20Data%20Wrangling.ipynb), I inspected the data and cleaned it.  Fortunately the data was already very neat when I began, so the process was not extensive.  Further details of each step I took are listed throughout the notebook.

### 3. Exploratory Data Analysis

In [this notebook](https://github.com/dawgtree/CapstoneThreeProject/blob/main/Cancer%20Diagnosis%20Capstone%20Project%20EDA.ipynb), I began exploring the data by visualizing the values and how they varied based on whether the tumor was benign or malignant.  I also did hypothesis testing to see if the difference in values were significant.  While most of the determining variables were significant, when I tested for correlation, I found that most of the variables had a very high correlation, which led to the removal of most of them for modeling since I did not want to have multicollinearity.  I ended up with five remaining variables out of the thirty that I started with:\
Radius mean\
Texture mean\
Smoothness mean\
Area standard error\
Concavity standard error\

* [Look here](https://public.tableau.com/profile/jonathan.daughtry#!/vizhome/BreastCancerCapstoneProjectEDA/BreastCancerEDA) to see how I further visualized the EDA on Tableau

Further details of each step I took are listed throughout the notebook.

### 4. Preprocessing, Splitting the Data, and Creating a Baseline Model
In [this notebook](https://github.com/dawgtree/CapstoneThreeProject/blob/main/Cancer%20Diagnosis%20Capstone%20Project%20Baseline%20Model.ipynb), I decided to model the data with all of the variables and also model the data with just the five remaining variables.  I first split the data into training and testing sets, and then I used Logistic Regression as a baseline model in which I will compare future models. 

The full dataset consisted of 28 determining variables and was split into a training set of 455 samples and a test (holdout) set of 144 samples.
The partial dataset consisted of 5 determining variables and was split into a training set of 455 samples and a test (holdout) set of 144 samples.

Obtained results are:

For the full dataset\
a. Accuracy of 97.37%\
b. 3 out of 114 (1.75%) false negatives\
c. A recall (when positive diagnoses are collectly predicted) of 95%\
d. AUC of 99.5%

For the partial dataset\
a. Accuracy of 92.98%\
b. 3 out of 114 (2.6%) false negatives\
c. A recall of 92%\
d. AUC of 97.64%\

I determined that my targeted metrics are going to be:\
Accuracy of at least 97%\
Less than 2% false negatives\
A recall of at least 95%\
AUC of at least 99%

### 5. Modeling
In [this notebook](https://github.com/dawgtree/CapstoneThreeProject/blob/main/Cancer%20Diagnosis%20Capstone%20Project%20Modeling.ipynb), I used three different modeling methods for classification on the data: K-Nearest Neighbors (KNN), Random Forest Classification, and XGBoost Classification.  For each model, I determined the accuracy, looked at the confusion matrix, plotted the ROC curve, calculated the area under the curve (AUC), and got the classification report and compared it to the baseline Logistic Regression Model.  The XGBoost model performed the best, scoring on par with the Logistic Regression and being the only model that met all the metrics that I set. Further details of each step I took are listed throughout the notebook.\
The XGBoost Performance Metrics:\
a. Accuracy of 97.37%\
b. 2 out of 114 (1.8%) false negatives\
c. A recall of 95%\
d. AUC of 99.28%\

### 5. Reporting Data
