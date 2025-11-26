# Telco Customer Churn Prediction with Feast Feature Store

A production-ready machine learning pipeline demonstrating customer churn prediction using Feast feature store for consistent feature management across training and serving environments.

## 🎯 Overview

This project implements an end-to-end ML system for predicting customer churn in the telecom industry. It showcases modern MLOps practices including feature store implementation, point-in-time correct feature retrieval, and online/offline feature serving using [Feast](https://feast.dev/).

## 📊 Dataset

We use the popular [Telco Customer Churn dataset](https://github.com/aiplanethub/Datasets/blob/master/WA_Fn-UseC_-Telco-Customer-Churn.csv) containing:
- **7,043 customer records** with 20 features
- Features include demographic info, services subscribed, account information
- Target variable: Customer churn (binary classification)

## 🏗️ Architecture

### Core Components
- **Feast Feature Store**: Manages feature storage and serving
- **Offline Store**: Parquet files for historical feature retrieval
- **Online Store**: SQLite for low-latency feature serving
- **ML Pipeline**: Scikit-learn with preprocessing and logistic regression
- **Time-aware Splitting**: Prevents data leakage using temporal validation

### Data Flow
1. **Raw Data** → Cleaning & preprocessing
2. **Feature Engineering** → Stored in Feast with timestamps
3. **Training** → Point-in-time correct feature retrieval
4. **Serving** → Online feature lookup for real-time predictions



