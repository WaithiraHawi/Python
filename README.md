# Customer Acquisition Analysis & Predictive Modeling

This project provides a comprehensive analysis of customer acquisition data, exploring marketing channel performance, revenue generation, and customer segmentation. It also includes predictive modeling for revenue forecasting and estimating customer lifetime value (LTV).

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
