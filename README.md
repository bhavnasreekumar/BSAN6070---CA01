# BSAN6070---CA01
Computer Assignment 1 Submission

CA01 – Exploratory Data Analysis & Data Quality Assessment (House Prices)

**Project Overview:**

This project is part of CA01 for the course Intro to Machine Learning. The objective is to explore the house price dataset through exploratory data analysis (EDA) and data quality assessment, with a focus on understanding feature distributions, missing values, and potential collinearity prior to any modeling.
The analysis emphasizes justification of cleaning decisions rather than building predictive models.

**Tools & Libraries:**

This project was completed using Python in a Jupyter Notebook environment.

Libraries used:
- pandas – data manipulation and cleaning
- numpy – numerical operations
- matplotlib – data visualization
- seaborn – statistical visualizations

**Dataset:**

- Dataset: House Prices training dataset
- Source: Provided by the course instructor
- Target Variable: SalePrice

**Analysis Workflow:**

*1. Data Exploration (EDA)*
- Reviewed dataset structure, data types, and summary statistics
- Visualized distributions of key numerical variables using histograms
- Used scatterplots to examine relationships between SalePrice and size/quality-related features
- Identified skewness and potential outliers through visual inspection

Each visualization includes a brief interpretation describing what the chart shows and why it matters.

*2. Data Quality & Missingness Assessment*
- Created a data quality summary to quantify missing values across features
- Identified variables with high missingness
- Interpreted missingness in context using the data description

Many variables with high missing values represent optional amenities (e.g., pools, alleys, fences, garage and basement features). In these cases, missing values likely indicate feature absence rather than data errors.

*3. Data Cleaning Decisions*
- Cleaning was performed on a copy of the original dataset
- Categorical features representing absent amenities were filled with "None"
- Numeric features where missingness implied absence were filled with 0
- LotFrontage was treated as true missing numeric data and imputed using the median within each neighborhood
  
No features were dropped based solely on missingness thresholds. All cleaning decisions are justified based on feature meaning.

*4. Collinearity Analysis*
- Computed a correlation matrix using numeric features only
- Visualized correlations using heatmaps
- Identified highly correlated feature pairs (|r| > 0.6)
- Interpreted what these correlations imply about feature redundancy
  
Highly correlated variables were not automatically dropped, as no modeling was required for this assignment. The analysis focuses on identification and interpretation rather than feature selection.

**Key Takeaways:**

- Housing prices are right-skewed, which is typical for real estate data
- Many missing values reflect optional amenities rather than poor data quality
- Several size-related features are strongly correlated, indicating potential redundancy in future modeling steps

**Notes:**

This project focuses strictly on EDA, data quality assessment, and collinearity analysis.
No machine learning models (e.g., decision trees, regression) were implemented as they were outside the scope of CA01.

