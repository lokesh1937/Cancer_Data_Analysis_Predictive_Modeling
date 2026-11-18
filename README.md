# Cancer Data Analysis & Predictive Modeling

## Overview

This project performs exploratory data analysis, statistical hypothesis testing, and machine learning on a dataset containing **50,000 cancer patient records**.

The analysis focuses on understanding relationships between patient risk factors, cancer characteristics, treatment costs, survival outcomes, and cancer severity.

The project combines descriptive statistics, correlation analysis, non-parametric hypothesis testing, and predictive modeling to extract meaningful insights from patient-level data.

## Dataset

The dataset contains **50,000 patient records** with 15 features, including:

* Patient ID
* Age
* Gender
* Country/Region
* Year
* Genetic Risk
* Air Pollution
* Alcohol Use
* Smoking
* Obesity Level
* Cancer Type
* Cancer Stage
* Treatment Cost (USD)
* Survival Years
* Target Severity Score

## Objectives

* Explore demographic and cancer-related patterns in the dataset.
* Analyze relationships between risk factors, treatment costs, survival, and cancer severity.
* Perform statistical hypothesis tests to evaluate relationships between variables.
* Build a machine learning model for predicting cancer severity.
* Identify important predictors using model feature importance.

## Project Workflow

```text
Raw Cancer Dataset
        ↓
Data Loading
        ↓
Data Cleaning & Inspection
        ↓
Exploratory Data Analysis
        ↓
Descriptive Statistics
        ↓
Correlation Analysis
        ↓
Hypothesis Testing
   ├── Pearson Correlation
   ├── Spearman Correlation
   └── Kruskal–Wallis Test
        ↓
Feature Preparation
        ↓
Random Forest Regression
        ↓
Model Evaluation
        ↓
Feature Importance Analysis
        ↓
Interpretation of Results
```

## Exploratory Data Analysis

The project explores:

* Distribution of patient age
* Gender distribution
* Cancer types
* Cancer stages
* Risk factors
* Treatment costs
* Survival years
* Target severity scores
* Relationships between numerical variables

Visualizations are created using Matplotlib and Seaborn.

## Statistical Analysis

### Pearson Correlation

Pearson correlation was used to examine the linear relationship between **Treatment Cost** and **Survival Years**.

The analysis produced a p-value greater than 0.92, indicating that the observed linear correlation was not statistically significant.

### Spearman Correlation

Spearman correlation was used to examine the monotonic relationship between **Treatment Cost** and **Survival Years** using ranked data.

The resulting p-value was also greater than 0.92, providing no statistically significant evidence of a monotonic association.

### Kruskal–Wallis Test

The Kruskal–Wallis test was used to compare:

* Treatment Cost across different Cancer Stages
* Survival Years across different Cancer Stages

Both tests produced p-values greater than 0.42, so the analysis did not find statistically significant differences across cancer-stage groups.

> A non-significant result does not prove that no relationship exists; it means the analysis did not find sufficient statistical evidence of a relationship at the chosen significance level.

## Machine Learning

A **Random Forest Regression** model was developed to predict the `Target_Severity_Score`.

### Model Evaluation

The Random Forest model achieved approximately:

**Test R²: 0.775**

This indicates that the model explained approximately 77.5% of the variance in the target severity score on the test set.

### Feature Importance

Feature importance analysis was used to understand which variables contributed most to the Random Forest predictions.

The most influential features included:

* Smoking
* Genetic Risk
* Treatment Cost
* Alcohol Use
* Air Pollution
* Obesity Level

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* SciPy
* Jupyter Notebook

## Repository Structure

```text
Cancer-Data-Analysis/
│
├── Cancer data Analysis.ipynb
├── README.md
├── requirements.txt
│
└── data/
    └── global_cancer_patients_2015_2024.csv
```

## Installation

Clone the repository:

```bash
git clone <your-github-repository-url>
cd Cancer-Data-Analysis
```

Create a virtual environment:

```bash
python -m venv venv
```

Activate it:

### Windows

```bash
venv\Scripts\activate
```

### macOS/Linux

```bash
source venv/bin/activate
```

Install the dependencies:

```bash
pip install -r requirements.txt
```

## Running the Project

Start Jupyter Notebook:

```bash
jupyter notebook
```

Open:

```text
Cancer data Analysis.ipynb
```

and run the notebook cells sequentially.

## Key Takeaways

* The dataset contains 50,000 cancer patient records.
* Pearson and Spearman tests found no statistically significant association between treatment cost and survival.
* Kruskal–Wallis tests found no statistically significant stage-wise differences in treatment cost or survival.
* Random Forest regression achieved a test R² of approximately 0.775 for predicting cancer severity.
* Feature importance analysis highlighted smoking, genetic risk, and treatment cost among the important predictors.

## Disclaimer

This project is intended for educational and data-science analysis purposes. The predictive results should not be interpreted as medical advice or used for clinical decision-making.
