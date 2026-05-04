# Customer Churn Prediction using Artificial Neural Networks

## Overview

This project builds a neural network model to predict customer churn in a telecommunications dataset.

The objective is to understand customer behaviour, identify churn patterns, and use deep learning to predict whether a customer is likely to leave the service.

This project was completed as part of the Artificial Neural Networks course at BITS Pilani.

---

## Problem Statement

Customer churn is a critical challenge for telecom companies.

Losing customers directly impacts revenue, and identifying customers likely to churn allows businesses to take preventive action.

The goal is to build a model that predicts whether a customer will churn based on their demographic, service, and billing data.

---

## Dataset

The dataset contains 7000+ customer records with features such as:

- demographics (gender, senior citizen)
- subscription details (internet, streaming services)
- contract type
- billing information
- payment methods

Target variable:
- 0 = No churn
- 1 = Churn :contentReference[oaicite:2]{index=2}  

---

## Data Preprocessing

- removed customerID (not useful for prediction)
- converted TotalCharges to numeric
- removed rows with missing values
- encoded categorical variables using one-hot encoding
- applied standard scaling
- split dataset into train and test sets :contentReference[oaicite:3]{index=3}  

Final dataset:
- ~7032 records
- ~30 features :contentReference[oaicite:4]{index=4}  

---

## Exploratory Insights

### Contract Type Impact
- customers with month-to-month contracts have higher churn rates

### Tenure Effect
- customers with shorter tenure churn more frequently

### Monthly Charges
- higher charges are associated with higher churn probability :contentReference[oaicite:5]{index=5}  

---

## Model Architecture

A feedforward neural network was used:

- input layer with all features
- hidden layer 1 → 16 neurons (ReLU)
- hidden layer 2 → 8 neurons (ReLU)
- output layer → 1 neuron (Sigmoid)

Loss function:
- Binary Cross-Entropy

Optimizer:
- Adam :contentReference[oaicite:6]{index=6}  

---

## Model Performance

- Accuracy ≈ 79%
- Precision (churn) ≈ 0.64
- Recall (churn) ≈ 0.49
- F1 Score ≈ 0.55 :contentReference[oaicite:7]{index=7}  

### Key Observation

- model performs well for non-churn customers
- struggles more to identify churn cases (false negatives)

---

## Business Insights

- month-to-month customers are high-risk
- early-stage customers are more likely to churn
- high-paying customers need better value perception

---

## Business Recommendations

### 1. Encourage Long-Term Contracts
- offer discounts for yearly plans
- increase customer commitment

### 2. Improve Value for High-Paying Customers
- targeted offers
- better support
- premium services :contentReference[oaicite:8]{index=8}  

---

## Risks

- model may miss actual churn cases (false negatives)
- dataset may not represent all customer types
- predictions should support, not replace decision-making :contentReference[oaicite:9]{index=9}  

---

## Why This Project Matters

This project demonstrates:

- neural network modelling
- data preprocessing for deep learning
- translating predictions into business decisions
- balancing performance and real-world usability

---

## Repository Structure
telco-churn-ann-model/

├── README.md
├── src/
│ └── telco_churn_ann_model.ipynb
├── docs/
│ ├── project_report.pdf
│ └── data_dictionary.pdf
├── assets/
│ └── (charts and outputs)


---

## How to Run

Clone repository:
git clone https://github.com/chetanpant/telco-churn-ann-model.git


Install dependencies:
pip install pandas numpy scikit-learn matplotlib seaborn tensorflow


Run notebook:

Open `.ipynb` file in Jupyter or Google Colab.

---

## Project Context

This project was developed as part of the Artificial Neural Networks course.

It covers:
- deep learning basics
- classification using neural networks
- model evaluation
- business interpretation
