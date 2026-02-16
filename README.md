# Sampling Techniques for Imbalanced Data & Model Comparison

_This repository contains the solution for **Assignment-2** on Sampling Techniques._

_Submitted by: **Dhruv Sethi**  
Roll No: **102303785**  
Subgroup: **3C54**_

---

## 📌 Assignment Description

This  assignment focuses on handling **imbalanced datasets** using different sampling techniques and evaluating their impact on various machine learning classification models.  
The dataset used is a **credit card fraud detection dataset**, where fraudulent transactions are extremely rare compared to legitimate ones.

The objective is to study how classical sampling methods and **SMOTE-based oversampling** affect model accuracy.

---

## 🎯 Objectives

- To analyze the problem of **class imbalance** in real-world datasets  
- To apply multiple **sampling techniques** on imbalanced data  
- To train different **machine learning models** on sampled data  
- To compare the **accuracy** of models across sampling methods  
- To understand why advanced techniques like **SMOTE** are preferred  

---

## 📊 Dataset Information

- **Dataset Name**: Creditcard_data.csv  
- **Problem Type**: Binary Classification (Fraud Detection)  
- **Class Distribution**:
  - `Class 0`: Normal transactions (Majority class)
  - `Class 1`: Fraudulent transactions (Minority class)

Due to the highly imbalanced nature of the dataset, direct training leads to biased models. Hence, sampling techniques are required.

---

## 🛠️ Sampling Techniques Used

### 1️⃣ Original Data
- Dataset used without any sampling
- Serves as a **baseline** for comparison

### 2️⃣ Random Sampling
- Random selection of samples from the dataset
- Simple and fast
- Does not guarantee class balance

### 3️⃣ Stratified Sampling
- Ensures proportional representation of each class
- Maintains class distribution
- Suitable for imbalanced datasets

### 4️⃣ Cluster Sampling
- Treats each class as a cluster
- Samples data from each cluster
- Useful when data can be grouped logically

### 5️⃣ Bootstrap Sampling
- Sampling with replacement
- Commonly used in ensemble methods
- Helps estimate model stability

### 6️⃣ SMOTE Oversampling
- **Synthetic Minority Over-sampling Technique**
- Generates synthetic data points for the minority class
- Reduces bias towards the majority class
- Discussed in classroom lectures and used as the primary imbalance-handling method

---

## 🤖 Machine Learning Models Implemented

The following models were trained on each sampled dataset:

1. Logistic Regression  
2. Random Forest  
3. Support Vector Machine (SVM)  
4. K-Nearest Neighbors (KNN)  
5. Decision Tree  

---

## 📈 Evaluation Metric

- **Metric Used**: Accuracy  
- **Reason**: Accuracy was used as per assignment guidelines  


---

## Results Summary
| Model                  | Original Data | Random Sampling | Stratified Sampling | Cluster Sampling | Bootstrap Sampling | SMOTE Oversampling |
| ---------------------- | ------------- | --------------- | ------------------- | ---------------- | ------------------ | ------------------ |
| Logistic Regression    | 0.9871        | 0.9828          | 0.9871              | 0.9871           | 0.9871             | 0.9397             |
| Random Forest          | 0.9871        | 0.9871          | 0.9871              | 0.9871           | 0.9871             | 0.9914             |
| Support Vector Machine | 0.9871        | 0.9871          | 0.9871              | 0.9871           | 0.9871             | 0.9655             |
| K-Nearest Neighbors    | 0.9871        | 0.9871          | 0.9871              | 0.9871           | 0.9871             | 0.9483             |
| Decision Tree          | 0.9741        | 0.9655          | 0.9828              | 0.9784           | 0.9871             | 0.9784             |

