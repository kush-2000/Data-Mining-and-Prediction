# 🚗 Project 2: Data Mining, Classification, and Prediction

**Author:** Kush Patel (ksp946)  
**Course:** SDS322E  
**Languages:** R, with optional Python integration via `reticulate`  

---

## 📋 Overview

This project analyzes U.S. police-reported car crashes using the `nassCDS` dataset from the `DAAG` package. The dataset includes data from 1997 to 2002 on crashes involving towed vehicles. The project applies various data mining and machine learning techniques to examine relationships between factors such as vehicle year, occupant age, and airbag deployment, and to predict injury severity and deployment likelihood.

---

## 📦 Libraries Used

### R Packages

- `tidyverse` – Data wrangling and visualization  
- `DAAG` – Access to the `nassCDS` dataset  
- `cluster`, `factoextra` – Clustering and silhouette analysis  
- `GGally` – PCA visualization (`ggpairs`)  
- `caret` – Classification models and cross-validation  
- `rpart`, `rpart.plot` – Decision trees and visualization  
- `reticulate` – Python integration within R  
- `stats` – PCA, logistic and linear regression  
- `class`, `MASS` – k-NN and additional statistical models  

### Python (via reticulate)

- `pandas` – Basic data manipulation from within R  

---

## 🔍 Project Highlights

- **Clustering:** Used PAM and K-means to group drivers by age and vehicle year; best silhouette width: 0.52 (2 clusters).
- **Dimensionality Reduction:** Performed PCA; top 2 components captured ~74% of the variance.
- **Classification Models:** 
  - Logistic regression with all numeric variables achieved an AUC of 0.895.
  - k-NN classifier evaluated with 10-fold CV (AUC ≈ 0.779).
- **Regression Models:** Explored linear models and decision trees to predict airbag deployment.
- **Python Interoperability:** Demonstrated cross-language workflows by analyzing R data in Python using `reticulate`.

---

## 📈 Results

- **Best Model:** Logistic regression using all numeric features (AUC = 0.895).
- **Insight:** Airbag deployment was best predicted with a multivariable logistic model rather than simple linear or k-NN approaches.
- **Python Integration:** Enhanced flexibility for analysis with familiar Python tools like `pandas`.

---

## 📂 Dataset

- **Source:** [R Datasets Repository](https://vincentarelbundock.github.io/Rdatasets/datasets.html)  
- **Dataset:** `nassCDS` (from `DAAG` package)  
- **Observations:** ~26,217 original rows  
- **Sample Used:** 150 observations after cleaning

---

## 🧠 Conclusion

This project demonstrates how data mining techniques can uncover patterns in crash data and build predictive models for airbag deployment. By combining R and Python, we created a flexible and extensible analysis pipeline that delivers accurate predictions and interpretable insights.

