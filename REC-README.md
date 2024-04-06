# Project Title: AI-Enhanced Breast Cancer Recurrence Prediction, Metastasis Localization, and Image Interpretation: A Multi-Modal analysis

## Description
Our project aims to develop predictive models for predicting breast cancer recurrence using machine learning techniques. Breast cancer recurrence, where cancer returns after treatment, is a significant concern in patient care and requires timely intervention for better outcomes. Leveraging diverse datasets, including the Metabric Breast Cancer dataset, Duke University Breast Cancer dataset, and MSK Breast Cancer dataset, our models are trained to accurately predict the likelihood of breast cancer recurrence based on various features and characteristics.

## Datasets
### Training Dataset
1. [Metabric Breast Cancer dataset](https://www.kaggle.com/datasets/gunesevitan/breast-cancer-metabric)
2. [Duke University Breast Cancer dataset](https://wiki.cancerimagingarchive.net/pages/viewpage.action?pageId=70226903)
3. [MSK Breast Cancer dataset](https://www.cbioportal.org/study/clinicalData?id=breast_msk_2018)

### Validation Dataset
Real patient data from Baheya hospital

## Preprocessing Details (Part 2)

### Dataset 1: Metabric Breast Cancer Dataset

**Handling Missing Values:**

Missing values are identified in selected columns related to various aspects of breast cancer diagnosis and treatment. Different strategies are applied to handle missing values based on column characteristics and domain knowledge:

- Event and duration columns such as 'Relapse Free Status' and 'Overall Survival Status' are imputed using group-wise mode and mean.
- Categorical columns like 'ER Status' and 'HER2 Status' are imputed with the mode within their respective groups.
- Numerical columns like 'Tumor Size' are imputed with the median within specific groupings.

**Normalization:**

The numerical values in columns like 'Tumor Size' and 'Lymph Node Status' are scaled or normalized to a predefined scale or categories. For example, 'Tumor Size' is categorized into discrete ranges.

### Dataset 2: Duke University Breast Cancer Dataset

**Handling Missing Values:**

Similar to Dataset 1, missing values are identified in specific columns. Strategies for handling missing values are applied, such as imputation with mode or median, based on column characteristics.

**Transformation:**

The dataset is transformed similar to Dataset 1, including mapping categorical variables back to their original strings.

### Merging Datasets and Additional Dataset: Baheya Recurrence Dataset

**Merging Datasets:**

The preprocessed datasets from Metabric and Duke University are merged to create a comprehensive dataset for analysis.

**Handling Missing Values:**

Similar strategies are applied to handle missing values in the merged dataset.

**Exploratory Data Analysis (EDA):**

Basic EDA is conducted to understand the distribution and characteristics of the merged dataset.

**Data Cleaning:**

Data cleaning steps are performed, such as dropping rows with missing values in critical columns and filtering out irrelevant data.

**Saving to CSV:**

The final cleaned and merged dataset is saved to a CSV file named 'merged_data.csv'.

## Requirements
- Python 3.x
- pandas
- matplotlib
- seaborn
- scikit-learn
- Google Colab (for running the code in the provided notebook)

## Installation
Ensure you have Python 3.x installed on your system.

```python
!pip install pandas matplotlib seaborn scikit-learn
