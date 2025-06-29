# Employee Turnover Data Cleaning and Profiling Project

## Overview

In the fast-paced technology industry, employee turnover poses a significant challenge. This project focuses on profiling, cleaning, and preparing a real-world HR dataset for analysis to help organizations identify employees at higher risk of leaving and implement more effective retention strategies.

In this simulated business scenario, I explored the dataset to address data quality issues, standardized inconsistent entries, engineered features, and delivered a clean dataset ready for modeling and dashboarding.

👉 [Click here to download the final cleaned dataset](output/employer_turnover_dataset_clean.csv).


## Project Objectives

The primary goal of this project was to prepare a real-world HR dataset for downstream analysis focused on employee turnover. Specifically, the project aimed to:

- **Profile the dataset** by examining variable types, data subtypes, and value distributions to understand the structure and quality of the data.
- **Identify data quality issues** such as missing values, duplicate records, formatting inconsistencies, outliers, and invalid entries (e.g., negative salaries or commute distances).
- **Apply data cleaning techniques** tailored to the nature of each issue, including:
    - String normalization and categorical value standardization
    - Imputation strategies based on data distribution (mode or median)
    - Outlier detection using z-scores and the IQR method
    - Capping and binning to support downstream modeling and analysis
- **Prepare the cleaned dataset** for future analytical tasks, including turnover prediction and retention strategy design.


## Core Competencies in Data Analytics and Engineering

### Data Analysis
- Conducted comprehensive data profiling to evaluate variable distributions, identify missing values, and generate descriptive statistics.
- Performed visual data exploration using libraries such as `seaborn`, `matplotlib`, and `missingno` to uncover patterns and detect anomalies.
- Applied robust outlier detection techniques, including z-score and interquartile range (IQR) methods, tailored to the underlying data distribution.
- Executed strategic imputation of missing values using mode or median approaches based on data skewness and contextual business considerations.

### Analytics Engineering
- Designed and implemented modular, reproducible data cleaning pipelines to ensure scalability and maintainability.
- Standardized categorical data inconsistencies through string similarity matching leveraging the `recordlinkage` library.
- Engineered features including:
    - Salary recalculation from hourly wage and hours worked.
    - Commute distance binning to enable segmentation and support dashboard creation.
- Enforced schema consistency through explicit data type conversion and validation.

### Data Engineering
- Performed thorough schema validation to align data types with analytical and business requirements.
- Identified and rectified invalid numerical values, including negative salary entries and zero commute distances.
- Utilized efficient, vectorized data transformation methods with `pandas` to optimize data processing performance.
- Delivered a clean, deduplicated, and analysis-ready dataset in CSV format to support downstream modeling and business intelligence activities.


##  Tools & Technologies & Techniques

| Category                                       | Tools / Libraries / Techniques                            |
|:---------------------------------|:--------------------------------------------------- |
| Programming Language      |`Python`                                                                          |
| Development Environment | `Jupyter Notebook` (via `Anaconda`)              |
| Data Handling                            | `pandas`, `numpy`                                               | 
| EDA & Visualization                  | `seaborn`, `matplotlib`, `missingno`                  |
| String Similarity Matching   | `recordlinkage`                                                           |
| Statistical Methods   | `scipy.stats.zscore` (for standardized outlier detection)                           |
| Techniques Applied    | Data profiling, missing value imputation, formatting normalization, z-score  IQR-based outlier detection, feature engineering (e.g., salary calculation, commute binning) |


## Key Highlights

- Aligned data preparation with a real-world HR use case to support employee retention initiatives and turnover prediction.
- Used statistical and visual profiling to uncover hidden quality issues, enabling deeper business insights.
- Resolved common real-world data problems (inconsistent job titles, negative salary values, missing fields) through customized logic and reproducible pipelines.
- Applied robust engineering principles (schema validation, modular logic) to build a solid foundation for analytical workflows.
- Transformed raw data into an analysis-ready format with enhanced variables (e.g., salary and commute bins), ready for modeling or dashboard integration.
- Delivered a high-quality `.csv` dataset suitable for BI tools and predictive models, reducing time-to-insight for decision makers.


## Key Data Cleaning Techniques

- **Missing Value Imputation**:
  - Mode for categorical (e.g., `text_message_optin`)
  - Median for skewed numeric (e.g., `annual_professional_dev_hrs`)
- **Outlier Detection**:
  - Z-score for general detection
  - IQR method for skewed variables like `annual_salary` and `driving_commuter_distance`
- **Standardization**:
  - Replaced inconsistent categorical values using replacement maps
  - Resolved formatting differences using similarity matching
- **Feature Engineering**:
  - Salary recalculated for negative values using `hourly_rate` and `hours_weekly`
  - Commute distance binned into categories for BI visualization
- **Data Validation**:
  - Removed exact duplicates
  - Casted columns to appropriate data types for analysis


## Project Structure

```text
workforce-attrition-data-profiling-cleaning/
├── data/
│   └── raw dataset.csv                            # Raw data
├── docs/
│   └── employee-attrition-scenario-and-data-dictionary.docx  # Business scenario + data dictionary
├── notebooks/
│   └── data-cleaning-and-profiling.ipynb          # Full analysis + cleaning code
├── output/
│   └── employer_turnover_dataset_clean.csv        # Final cleaned dataset
└── README.md                                      # Project overview
```


## Sample Insights Enabled by Clean Data

- Distribution of tenure vs. turnover to assess attrition risk by experience
- Salary trend comparisons across job roles or commute distance bins
- Readiness for machine learning models predicting turnover risk
- Clean dataset suitable for visualization in tools like Power BI


## Outcomes

|Deliverable                                            |Description                                          | 
|:------------------------------------------|:-----------------------------------------------|
| Cleaned Dataset (`CSV`)                       | Free of duplicates, missing values, and invalid entries |
| Data Cleaning Notebook (`.ipynb`)   | Step-by-step documented cleaning process                    |
