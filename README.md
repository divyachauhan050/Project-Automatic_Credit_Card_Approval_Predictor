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

3. The continent-wise breakup for the different industry categories and the earliest year that records their existence is as follows:
<br> </br>
4.



