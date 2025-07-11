

# Machine Learning-Driven Diabetes Classification Using Genetic Programming

## Overview

This project implements an interpretable machine learning approach for diabetes prediction using **Genetic Programming (GP)**. By evolving symbolic mathematical expressions, we create a transparent classifier that predicts the presence or absence of diabetes from health and demographic data. Our solution consistently ranked in the top 10 throughout the competition phase.

---

## Table of Contents

- [Project Motivation](#project-motivation)
- [Dataset](#dataset)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Preprocessing](#preprocessing)
- [Machine Learning Approach](#machine-learning-approach)
- [Results](#results)
- [Strengths & Limitations](#strengths--limitations)
- [Future Work](#future-work)
- [How to Run](#how-to-run)
- [Team](#team)
- [References](#references)

---

## Project Motivation

The primary objective was to design an interpretable and robust machine learning classifier using evolutionary algorithms, specifically Genetic Programming, to predict diabetes based on health and demographic features. This approach allows us to:

- Create transparent models that can be inspected and understood by healthcare professionals
- Discover non-linear relationships between health indicators and diabetes risk
- Demonstrate the effectiveness of evolutionary computation in solving real-world classification problems

---

## Dataset

- **Source:** Modified version of the Diabetes dataset
- **Size:** 5,042 samples
- **Features:** 22 health and demographic indicators including:
  - HighBP, HighChol, CholCheck, BMI, Smoker, Stroke, HeartDiseaseorAttack, PhysActivity, Fruits, Veggies, HvyAlcoholConsump, AnyHealthcare, NoDocbcCost, GenHlth, MentHlth, PhysHlth, DiffWalk, Sex, Age, Education, Income
- **Target:** `output` column (0: absence of diabetes, 1: presence of diabetes)

---

## Exploratory Data Analysis

A thorough Exploratory Data Analysis (EDA) was performed to understand the dataset’s structure, identify key patterns, and inform modeling decisions.

### Statistical Analysis
- Computed descriptive statistics (mean, median, standard deviation) for all features
- Identified outliers and examined their potential impact on model performance
- Analyzed class distribution to address potential imbalance issues

### Data Visualization
- Generated histograms and density plots to visualize feature distributions
- Created correlation matrices to identify relationships between features
- Produced scatter plots to examine feature interactions and their relationship with the target variable

### Key Insights
- Identified the most predictive features for diabetes classification
- Discovered non-linear relationships between certain health indicators and diabetes presence
- Detected potential data quality issues and addressed them in preprocessing
- Informed feature selection and engineering decisions for the GP framework

---

## Preprocessing

### Standardization
- Features were standardized to have zero mean and unit variance using `StandardScaler`
- This normalization prevents features with larger scales from disproportionately influencing the model

### Safe Mathematical Operations
To handle edge cases during evolution, we implemented custom safe functions:
