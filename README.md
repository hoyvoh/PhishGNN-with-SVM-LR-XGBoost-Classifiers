# Phishing Detection Project

## [Report](report.com)

## Project Overview
This project aims to develop and analyze models for detecting phishing websites based on a variety of web page characteristics. Using data-driven approaches, the project processes two publicly available datasets to build, train, and evaluate machine learning models that can classify websites as phishing (1) or benign (0).

## Datasets

### 1. [Phishing Dataset by Grega Vrbancic](https://github.com/GregaVrbancic/Phishing-Dataset)
   - This dataset contains 97 features that represent various aspects of websites, including both numerical and categorical data.
   - The dataset includes a target label: `1` for phishing and `0` for benign websites.
   - Features cover attributes like URL length, domain registration details, and content features that help identify phishing behavior.

### 2. [Web Page Phishing Detection Dataset by Shashwatwork](https://www.kaggle.com/datasets/shashwatwork/web-page-phishing-detection-dataset)
   - This dataset includes features that are extracted from web pages to assess their likelihood of being phishing or benign.
   - It also has a binary target label: `1` for phishing and `0` for benign websites.
   - Features in this dataset include aspects of URLs, HTML content, and web page structure.

## Dataset Features
Both datasets contain **97 features**, each representing a unique attribute of the web page that could indicate phishing activity.

The **target label** is a binary classification:
- `1`: Phishing
- `0`: Benign

## Results

| Dataset                                           | Classifier                           | ROC - AUC | F1-Score | Accuracy | AIC     | BIC     |
|---------------------------------------------------|--------------------------------------|-----------|----------|----------|---------|---------|
| **Phishing Dataset from Towards benchmark datasets for machine learning based website phishing detection** | Logistic Regression                  | 0.85      | 0.76     | 0.78     | 1694.57 | 1890.67 |
|                                                   | SVM                                  | 0.85      | 0.74     | 0.77     | 12454.74| 41956.60|
|                                                   | **XGBoost**                              | **0.93**      | **0.84**     | **0.85**     | **1206.12** | **1402.22** |
|                                                   | GCN depth 2 + Logistic Classifier    | 0.88      | 0.80     | 0.80     | 1595.29 | 1949.36 |
|                                                   | GCN depth 2 + SVM Classifier         | 0.88      | 0.80     | 0.80     | 10524.69| 35173.12|
|                                                   | **GCN depth 2 + XGBoost Classifier**     | **0.913**     | **0.82**     | **0.83**     | **1426.12** | **1780.19** |
| **GregaVrbancic/Phishing Dataset**                | Logistic Regression                  | 0.96      | 0.84     | 0.897    | 7082.94 | 6813.1  |
|                                                   | SVM                                  | 0.96      | 0.86     | 0.9      | 6847.78 | 7110.12 |
|                                                   | **XGBoost**                              | **0.98**      | **0.91**     | **0.94**     | **4274.08** | **4536.42** |
|                                                   | GCN depth 2 + Logistic Classifier    | 0.97      | 0.87     | 0.91     | 5779.43 | 6266.63 |
|                                                   | GCN depth 2 + SVM Classifier         | 0.97      | 0.87     | 0.91     | 6046.63 | 6526.33 |
|                                                   | **GCN depth 2 + XGBoost Classifier**     | **0.97**      | **0.88**     | **0.92**     | **5239.03** | **5725.23** |

## Contributors
- Ho Ngoc Tuong Vy | hovyoh |  hntvy23@gmail.com | 21521685
- Nguyen Thi Van Anh |  | 21521835@gm.uit.edu.vn | 21521835
- Ngo Thuan Phat |  | 21522445@gm.uit.edu.vn | 21522445
- Nguyen Toan Khang |  | 21522195@gm.uit.edu.vn | 21522195
