# Project - Automatic Credit Card Approval Predictor

Commercial banks receive a lot of applications for credit cards. Many of them get rejected for many reasons, like high loan balances, low income levels, or too many inquiries on an individual's credit report, for example. Manually analyzing these applications is mundane, error-prone, and time-consuming (and time is money!). Luckily, this task can be automated with the power of machine learning and pretty much every commercial bank does so nowadays.

In this project, I built an automatic credit card approval predictor using machine learning techniques, just like real banks do.

## About the Datasets
I have used the [Credit Card Approval dataset](http://archive.ics.uci.edu/ml/datasets/credit+approval) from the UCI Machine Learning Repository. The notebook follows this structure:

* First, I started off by loading and viewing the dataset.
* I saw that the dataset has a mixture of both numerical and non-numerical features, that it contains values from different ranges, plus that it contains a number of missing entries.
* I had to preprocess the dataset to ensure the machine learning model I choose can make good predictions.
* After the data is in good shape, I did some exploratory data analysis to build our intuitions.
* Finally, I built a machine learning model that can predict if an individual's application for a credit card will be accepted.

## Key Findings

**Business Question that I try to answer: "Predicting if a credit card application will be approved or not?"**

These are some of the key findings for this project:
1. The features of this dataset had been anonymized to protect the privacy, so determining the exact features was challenging. But [this blog](http://rstudio-pubs-static.s3.amazonaws.com/73039_9946de135c0a49daa7a0a9eda4a67a72.html) gives us a pretty good overview of the probable features.

2. The probable features in a typical credit card application are **Gender**, **Age**, **Debt**, **Married**, **BankCustomer**, **EducationLevel**, **Ethnicity**, **YearsEmployed**, **PriorDefault**, **Employed**, **CreditScore**, **DriversLicense**, **Citizen**, **ZipCode**, **Income** and finally the **ApprovalStatus**.

3. Features like **DriversLicense** and **ZipCode** are not as important as the other features in the dataset for predicting credit card approvals, so they are dropped to obtain a more streamlined training data.
 
4. Our dataset contains both numeric and non-numeric data (specifically data that are of **float64**, **int64**, and **object** types). Specifically, the features **2, 7, 10** and **14** contain numeric values (of types **float64, float64, int64** and **int64** respectively) and **all the other features** contain **non-numeric values**.

5. The dataset also contains values from several ranges. Some features have a *value range of 0 - 28*, some have a *range of 2 - 67*, and some have a *range of 1017 - 100000*. Apart from these, we can get useful statistical information (like **mean**, **max**, and **min**) about the features that have numerical values.

6. Finally, the dataset has missing values, which we'll take care of in this task. The missing values in the dataset are labeled with '?', which can be seen in the last cell's output of the second task. I replaced all the question marks with NaNs.

7. An important question that gets raised here is *why are we giving so much importance to missing values*? Can't they be just ignored? Ignoring missing values can affect the performance of a machine learning model heavily. While ignoring the missing values our machine learning model may miss out on information about the dataset that may be useful for its training. Then, there are many models which cannot handle missing values implicitly such as Linear Discriminant Analysis (LDA). So, to avoid this problem, I imputed the missing values with a strategy called **mean imputation**.

8. This is to 



