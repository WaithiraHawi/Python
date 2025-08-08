# Customer Acquisition Analysis & Predictive Modeling

This project provides a comprehensive analysis of customer acquisition data, exploring marketing channel performance, revenue generation, and customer segmentation. It also includes predictive modeling for revenue forecasting and estimating customer lifetime value (LTV).

<img width="1024" height="1024" alt="Customer Acquisition" src="https://github.com/user-attachments/assets/0f598022-6043-443e-ade8-b11d61f01142" />


## Dataset Overview

* `customer_id`: Unique identifier for each customer
* `channel`: Marketing acquisition channel (e.g., Email, Social Media, Ads)
* `cost`: Cost incurred to acquire the customer
* `conversion_rate`: Probability of converting a lead to a customer
* `revenue`: Revenue generated from the customer

## Project Objectives

* Explore and clean the dataset for quality assurance
* Perform descriptive and visual exploratory data analysis (EDA)
* Implement predictive modeling to forecast customer revenue
* Conduct customer segmentation using clustering algorithms
* Analyze revenue contribution by channel
* Estimate Customer Lifetime Value (LTV)

## Data Preprocessing
* Removed duplicates to ensure data integrity.
* Checked for nulls, there were no missing values.
* Encoded the `channel` feature using `LabelEncoder` for modeling.
* Feature Scaling: Standardized numerical values for clustering.

## Exploratory Data Analysis (EDA)

### Summary Statistics

* Descriptive stats for numerical columns.
* Categorical distribution of acquisition channels.

### Visualizations

* Histograms for distributions (e.g., cost, revenue)
* Boxplots to detect outliers
* Correlation heatmap for numerical relationships
* Count plots for each channel

## Predictive Modeling

### Objective:

Predict customer **revenue** based on:

* Acquisition `cost`
* `conversion_rate`
* Acquisition `channel`

### Model:

* **Model**: Linear Regression
* **Performance**:
  * R² Score: Measures variance explained by the model
  * RMSE: Root Mean Squared Error for accuracy of predictions

## Customer Segmentation

### Objective:

Cluster customers into distinct segments based on:

* `cost`
* `conversion_rate`
* `revenue`

### Method:
* Algorithm: K-Means Clustering
* Number of Clusters: 3
* Dimensionality Reduction: PCA for 2D visualization

### Visualization:
* Scatterplot with clusters using PCA components
* Each color represents a unique customer segment

## Revenue Analysis by Channel
* Grouped data by `channel`
* Aggregated total revenue, average revenue, and customer count
* Visualized using bar charts

## Lifetime Value (LTV) Estimation
### Objective:
Estimate how profitable each channel is over time.

### Metrics:
* Mean LTV per channel
* Total LTV per channel

### Visualization:
* Bar chart of LTV across channels

## Insights
* Some channels generate higher average revenue but have higher acquisition costs.
* Segmentation revealed three distinct customer types with varying conversion and revenue patterns.
* Predictive modeling achieved reasonable accuracy for revenue forecasting.

## Improvements
In future, I will: 
* Add more customer behavior features (e.g., demographics, visit frequency)
* Apply advanced regression models (e.g., XGBoost, Random Forest)
* Implement LTV prediction using survival analysis
* Run clustering optimization (e.g., Silhouette Score)


# Loan Default Risk Analysis & Customer Segmentation

## Project Overview

This project analyzes a **Loan Default dataset** to explore patterns and factors influencing loan default risk.
In addition, it applies **customer segmentation** techniques to group borrowers into meaningful clusters and builds **default risk profiles** for each segment.
The goal is to provide **actionable insights** for credit risk teams and financial institutions to optimize lending decisions.

<img width="1024" height="1024" alt="Loan default" src="https://github.com/user-attachments/assets/756722ab-a6c8-4b2a-a4b9-6636a0d286aa" />

## Dataset

* **File:** `Loan_default.csv`
* **Description:** Contains customer demographic details, loan attributes, and default status.
* **Key Features:**

  * `Customer_ID` – Unique customer identifier
  * `Age` – Age of the borrower
  * `Income` – Monthly/annual income
  * `LoanAmount` – Loan amount approved
  * `Loan_Term` – Duration of the loan
  * `Credit_Score` – Credit score of the customer
  * `Default` – Target variable (1 = default, 0 = no default)
  * Other possible features: Employment type, marital status, purpose of loan, etc.

## Technologies Used

* **Python** (Data Analysis & Machine Learning)
* **Pandas** – Data manipulation
* **NumPy** – Numerical operations
* **Matplotlib** / **Seaborn** – Data visualization
* **Scikit-learn** – Machine learning & clustering
* **Jupyter Notebook** – Analysis environment


## Analysis Workflow

### 1️Data Preprocessing

* Load dataset and inspect structure
* Handle missing values
* Encode categorical variables
* Remove outliers if necessary
* Standardize numerical features for clustering

### Exploratory Data Analysis (EDA)

* Univariate analysis (distribution plots)
* Bivariate analysis (correlation heatmaps, scatter plots)
* Default rate analysis by demographic & loan features
* Feature importance using **Random Forest Classifier**

### Default Risk Profiling

* Identify top predictors of default
* Build profiles for **High**, **Medium**, and **Low** risk borrowers
* Calculate default probability per profile

### Customer Segmentation (K-Means Clustering)

* Normalize features
* Determine optimal number of clusters (Elbow Method & Silhouette Score)
* Apply K-Means clustering
* Visualize customer segments
* Link clusters with default risk to create actionable strategies

## Key Insights 

* Customers with **low credit scores** and **high loan amounts** have the highest default probability
* Younger borrowers tend to have slightly higher risk levels compared to older borrowers
* Three customer segments were identified:

  * **Cluster 1:** High-income, low-risk borrowers
  * **Cluster 2:** Medium-income, moderate-risk borrowers
  * **Cluster 3:** Low-income, high-risk borrowers

## Next Steps

* Incorporate advanced ML models (XGBoost, LightGBM) for better prediction
* Develop an interactive dashboard for risk visualization
* Integrate the model into a loan approval API
