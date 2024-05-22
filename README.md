# Lending Club Case Study - Exploratory Data Analysis

## Table of Contents
* [Objectives](#objectives)
* [Problem Statement](#problem-statement)
* [Technologies Used](#technologies-used)
* [Approach for EDA](#approach-for-eda)
* [Analysis Outcome](#analysis-outcome)
* [Conclusion](#conclusion)
* [Acknowledgements](#acknowledgements)

## Objectives

**Exploratory Data Analysis (EDA)** is a technique by which analysis of data is done in an unconstrained free-floating manner to discover the relationships among various variables so that those relationships can be leveraged in risk analysis, predictions, fraud detection etc.

EDA has been utilized in this case study in a systematic manner to analyse the data provided for the analysis. The approach described here can be utilised for similar exercises in professional organisations.


## Problem Statement

Lending Club (LC) is a fictitious NBFC which is in the business of providing loans to consumers and gain from the interest earned.

* It competes with other heavyweights in a very competitive environment
* It needs to attract customers with low interest rates while ensuring minimal defaults
* It loses business if it rejects loan applications due to conservative credit assessments
* It makes losses if customer defaults
* LC is looking to understand the driving factors behind loan defaults so that they can effectively use those factors to determine risky customers

The objective of this exercise is to analyse the available data regarding past loans and identify those factors or variables which are strong indicators of default


## Technologies Used

Python Jupyter Notebook with Numpy, Pandas, Matplotlib, Seaborn and other relevant libraries are used to prepare, analyse and visualise data


## Approach for EDA

A six-step approach is used for to analyse the data for this exercise:

* Import Data
* Clean & Transform Data
* Perform Univariate Analysis
* Perform Bivariate Analysis
* Perform Multivariate Analysis
* Create Report

Going into some more details,

- Data in .csv-form is **imported** into Python Notebook
- Columns with missing (null) data are either **imputed or removed**
- Some of the columns (variables) are **converted** from object-type to float-type
- Variables are divided into buckets of **numerical** and **categorical** data types
- **Univariate** analysis of numerical **(histplot/ boxplot)** and categorical **(countplot)** variable is done
- **Bivariate** analysis of numerical **(boxplot)** and categorical **(barplot)** variables is done against target variable i.e. Loan Status
- **Multi-variate** analysis is done on numerical variables using **Heatmap**
- Finally, conclusions are drawn, and report is made

## Analysis Outcome
Based on analysis of 53 variables (58 variables dropped due to null values), the following factors are identified to be of interest to Lending Club team:

Driving Factors with **high** influence on loan default:

* *Revolving Line Utilization Rate*  - Avoid customers having more than 80% utilization rate
* *No. of Enquiries* - Avoid customers with more than 1 enquiries in past 6 months
* *Longer Term Loan* - Avoid giving 60-months loans as much as possible

Driving Factors with **moderate** influence on loan default:

* *Loans for Small Business* - Keep such loans to less than 5% of portfolio 
* *Lower Graded Loans* - Such loans should be provided with caution
* *Debt-to-Income Ratio* - Keep DTI below 20% as much as possible

## Conclusion

* The exercise produced a set of variables which can help LC to determine potential defaulting customers in advance
* Exploratory Data Analysis technique was adequate to identify relationships within variables
* More than 50% columns had no data. More analysis can be possible if data are made available for those columns
* More advanced data models can be built as next steps that can be used by LC for risk assessment


## Acknowledgements

This case study has been developed as part of Post Graduate Diploma Program on Machine Learning and AI, offered jointly by Indian Institute of Information Technology, Bangalore (IIIT-B) and upGrad.

