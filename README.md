# Instacart Market Basket Analysis

## Introduction
Instacart is an American technology company that operates a same-day grocery delivery and pickup service in the U.S. and Canada. Customers shop for groceries through the Instacart mobile app or Instacart.com from various retailer partners. Each order is shopped and delivered by an Instacart personal shopper.

## Objectives
- Analyze the anonymized data of **3 million** grocery orders from **200,000+** Instacart users open sourced by Instacart.
- Find hidden associations between products for better cross-selling and upselling.
- Perform customer segmentation for targeted marketing and to anticipate customer behavior.
- Build a machine learning model to predict which previously purchased product will be in a user’s next order.

## Project Organization
├── Plots/ : Contains all plots
├── Data Description and Analysis.ipynb : Initial analysis to understand data
├── Exploratory Data Analysis.ipynb : EDA to analyze customer purchase pattern
├── Customers Segmentation.ipynb : Customer Segmentation based on product aisles
├── Market Basket Analysis.ipynb : Market Basket Analysis to find products association
├── Feature Extraction.ipynb : Feature engineering and extraction for a ML model
├── Data Preparation.ipynb : Data preparation for modeling
├── ANN Model.ipynb : Neural Network model for product reorder prediction
├── XGBoost Model.ipynb : XGBoost model for product reorder prediction
├── LICENSE : License
└── README.md : Project Report

## Data Description

### `aisles`
This file lists different aisles; there are **134** unique aisles.

### `departments`
This file lists different departments; there are **21** unique departments.

### `orders`
This file contains all orders made by different users. Key findings:
- There are **3,421,083** orders made by **206,209** users.
- Orders are split into **Prior**, **Train**, and **Test** sets. Train and Test distributions are similar, while Prior differs.
- Total orders per customer range from **0 to 100**.
- From the **Orders vs. Day of Week** plot, we can map **0 → Saturday** and **1 → Sunday**, assuming most grocery shopping happens on weekends.
- The majority of orders are placed **during daytime**.
- Customers typically order **once a week**, supported by peaks at **7, 14, 21, and 30** in the **Orders vs. Days Since Prior Order** graph.
- A **Day of Week × Hour of Day** heatmap shows **Saturday afternoons** and **Sunday mornings** as prime ordering times.
