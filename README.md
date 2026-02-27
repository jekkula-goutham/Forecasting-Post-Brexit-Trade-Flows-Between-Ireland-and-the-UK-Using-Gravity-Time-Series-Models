# Forecasting-Post-Brexit-Trade-Flows-Between-Ireland-and-the-UK-Using-Gravity-Time-Series-Models
## 📌 Project Overview

This thesis develops a hybrid econometric–machine learning framework to forecast Ireland’s merchandise exports to the United Kingdom in the post-Brexit era.

### The framework combines:

📊 Structural Gravity Model (PPML)

📈 Time-Series Models (ARIMA)

🤖 Deep Learning (LSTM, Transformer)

💰 Sector-Level Tariff Integration

📉 Brexit Scenario Simulation

### The goal is to separate:

Long-run structural trade drivers (GDP, distance, RTA, tariffs)
from

Short-run volatility and non-linear dynamics

🧱 Complete Thesis Pipeline

The repository contains three major notebooks, each representing a layer of the modelling architecture.

## 📁 1️⃣ CSO Data Processing

File: CSO.Dataset_Code.ipynb

Purpose:

Clean CSO trade data

Aggregate into 6 Brexit-sensitive sectors

Validate totals

Compute sector shares

Build master export dataset

Final Output:
Export_Master_Dataset_Clean.xlsx


This file becomes the time-series modelling input.

## 📁 2️⃣ Gravity Dataset Preparation

File: Gravity_Dataset_preparation_code.ipynb

Purpose:

Filter IE → UK bilateral trade

Merge GDP data

Integrate sector-level tariffs

Prepare PPML-ready panel dataset

Final Output:
PPML_clean_Dataset.xlsx


This file is used for structural estimation.

## 📁 3️⃣ Thesis Model Calculation

File: Thesis Model calculation code.ipynb

Modelling Sequence:
Step 6 – Pure Time-Series Forecasting

Output:

Time_series_prediction.xlsx

Step 7 – PPML Gravity Estimation

Output:

PPML_Hybrid_prediction.xlsx

Step 8 – Residual Forecasting

Output:

Residual_Forecasts_prediction.xlsx

Step 9 – Hybrid Forecast Construction

Output:

Hybrid_Forecasts_prediction.xlsx

Future Forecasts (2024–2025)
Time_series_forecasts_2024_2025.xlsx
Hybrid_Forecasts_Future.xlsx
Hybrid_WhatIf_Scenarios.xlsx

## 📊 Visual Pipeline Architecture
            
                 CSO Raw Trade Data     
                           ↓
            ┌──────────────────────────┐
            │  Export_Master_Dataset   │
            └──────────────┬───────────┘
                           ↓
            ┌──────────────────────────┐
            │ Gravity + GDP + Tariffs  │
            └──────────────┬───────────┘
                           ↓
            ┌──────────────────────────┐
            │ PPML_clean_Dataset.xlsx  │
            └──────────────┬───────────┘
                           ↓
        ┌──────────────────┴──────────────────┐                                  
    Time-Series Models                    PPML Gravity
    (ARIMA/LSTM/Transformer)               Structural Model
             ↓                                     ↓
    Baseline Forecasts                  Structural Predictions
        ↓                                     ↓
              ┌───────────────────────┐
                 Residual Forecasting  
            
                            ↓
                 Hybrid Forecast Construction
                            ↓
         2024–2025 Forecasts + Brexit Scenarios

## 📘 Executive Summary 

This thesis develops a hybrid forecasting framework to analyse and predict Ireland’s merchandise exports to the UK in the post-Brexit environment.

The project integrates economic theory with machine learning by combining a Poisson Pseudo-Maximum Likelihood (PPML) Gravity model with ARIMA, LSTM, and Transformer time-series models.

The structural Gravity model captures long-run trade drivers such as GDP growth, distance, RTA coverage, and sector-level tariffs. Residuals from this model are then modelled using advanced time-series techniques to capture short-run volatility and non-linear behaviour. The final hybrid forecast adds structural predictions and residual forecasts to improve predictive accuracy.

### The framework enables:

Sector-level tariff impact analysis

Hard vs Soft Brexit scenario simulation

24-month forward forecasts (2024–2025)

Structural vs short-run shock decomposition

Results show that hybrid models outperform standalone econometric or time-series models, demonstrating the value of integrating economic structure with deep learning approaches.

### This work showcases advanced skills in:

Econometrics (PPML)

Time-series modelling

Deep learning architectures

Data engineering

Policy impact simulation
