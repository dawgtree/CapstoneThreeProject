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

Further details of each step I took are listed throughout the notebook.

### 4. Preprocessing and Splitting the Data

### 5. Modeling

### 5. Reporting Data
