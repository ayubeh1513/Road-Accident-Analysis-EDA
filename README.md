# Road Accident Analysis in India – Exploratory Data Analysis

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)
![Seaborn](https://img.shields.io/badge/Seaborn-4C72B0?style=for-the-badge)
![Tableau](https://img.shields.io/badge/Tableau-FF7F0E?style=for-the-badge&logo=tableau&logoColor=white)

A comprehensive Exploratory Data Analysis (EDA) project focused on analyzing road accident patterns in India using Python, statistical techniques, and interactive visualization through Tableau dashboards.

---

## Table of Contents

1. [Introduction](#introduction)
2. [Key Features](#key-features)
3. [Project Workflow](#project-workflow)
4. [Technology Stack](#technology-stack)
5. [Getting Started](#getting-started)
   - [Prerequisites](#prerequisites)
   - [Dataset Setup](#dataset-setup)
   - [Running the Analysis](#running-the-analysis)
6. [Dataset Information](#dataset-information)
7. [Screenshots](#screenshots)
8. [Contributing](#contributing)
9. [License](#license)

---

# Introduction

Road traffic accidents are one of the leading causes of fatalities and injuries in India, causing significant social and economic consequences. Understanding accident patterns and contributing factors such as speed, road type, weather conditions, and lighting conditions is essential for designing effective road safety policies.

This project performs a detailed **Exploratory Data Analysis (EDA)** on Indian road accident data to uncover patterns, trends, and relationships among accident-related variables. Instead of focusing on predictive modeling, the project emphasizes **data understanding, statistical exploration, and visualization**.

The analysis combines **Python-based statistical techniques with visualization libraries such as Matplotlib and Seaborn**, and further extends insights through **interactive Tableau dashboards** to support data-driven decision-making for traffic safety and policy planning.

---

# Key Features

- Comprehensive **Exploratory Data Analysis**
- Data cleaning and preprocessing
- Handling missing values and outliers
- Statistical analysis and inference
- Visualization using Python libraries
- Interactive dashboards using **Tableau**
- Identification of accident severity patterns

---

# Project Workflow

### 1. Data Collection
The dataset containing Indian road accident records is loaded and inspected using Pandas.

### 2. Data Understanding

Initial exploration includes:

```
df.info()
df.describe()
df.shape
```

This step helps understand variable types and summary statistics.

---

### 3. Data Quality Assessment

The dataset is analyzed for:

- Duplicate records
- Missing values
- Data inconsistencies

Missing values are handled using **mean and mode imputation**.

---

### 4. Outlier Detection and Treatment

Outliers are detected using **boxplots and the IQR method**.

Instead of removing extreme values, **capping is applied** to preserve significant accident events while reducing statistical distortion.

---

### 5. Data Standardization

Numerical variables are standardized using **StandardScaler** to normalize features with different measurement scales.

---

### 6. Exploratory Data Analysis

EDA includes multiple types of analysis:

#### Univariate Analysis

- Histograms
- KDE plots
- Violin plots

#### Bivariate Analysis

- Scatter plots
- Boxplots across categories

#### Multivariate Analysis

- Pair plots
- Correlation heatmaps

---

### 7. Statistical Inference

The project demonstrates statistical concepts such as:

- Probability distributions
- Central Limit Theorem
- Confidence intervals
- Hypothesis testing

---

### 8. Interactive Visualization

Insights are presented using **Tableau dashboards**, including:

- State-wise accident distribution
- Accident trends over time
- Weather and lighting impact
- Road type comparison

---

# Technology Stack

### Programming Language
- Python

### Libraries
- Pandas
- NumPy
- Matplotlib
- Seaborn
- SciPy
- Scikit-learn

### Visualization
- Tableau

### Development Environment
- Jupyter Notebook
- VS Code

---

# Getting Started

Follow these instructions to run the project locally.

---

## Prerequisites

Install required Python libraries:

```
pip install pandas numpy matplotlib seaborn scipy scikit-learn
```

---

# Dataset Setup

Place the dataset file in the project directory:

```
indian_road_accidents.csv
```

Load the dataset:

```
import pandas as pd

df = pd.read_csv("indian_road_accidents.csv")
```

---

# Running the Analysis

Run the Jupyter Notebook containing the EDA code.

Example commands:

```
df.info()
df.describe()
df.isnull().sum()
```

Visualization example:

```
import seaborn as sns
import matplotlib.pyplot as plt

sns.histplot(df['speed_limit_kmph'])
plt.show()
```

Correlation heatmap:

```
sns.heatmap(df.corr(), annot=True)
plt.show()
```

---

# Dataset Information

Dataset Characteristics:

| Feature | Description |
|------|------|
| Records | 22,500 accident entries |
| Attributes | 18 variables |
| Data Types | Numerical + Categorical |
| Coverage | Multiple Indian states and cities |

Variables include:

- accident_id
- date
- state
- city
- road_type
- weather
- light_condition
- speed_limit_kmph
- vehicles_involved
- casualties_total
- fatalities
- serious_injuries
- minor_injuries
- alcohol_involved
- damage_cost_inr

---

# Screenshots

| Histogram Analysis | Correlation Heatmap | Tableau Dashboard |
|:---:|:---:|:---:|
| ![Histogram](histogram.png) | ![Heatmap](heatmap.png) | ![Dashboard](dashboard.png) |

---

# Contributing

Contributions are welcome.

Steps to contribute:

1. Fork the repository
2. Create a new branch

```
git checkout -b feature/NewFeature
```

3. Commit your changes

```
git commit -m "Added new feature"
```

4. Push to the branch

```
git push origin feature/NewFeature
```

5. Open a Pull Request

---

# License

This project is licensed under the **MIT License**.
