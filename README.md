# Spatio-Temporal Graph Learning for Hourly Demand Forecasting in Public BRT Systems

## Overview
This repository contains the implementation of a Spatio-Temporal Graph Neural Network (ST-GNN) designed to forecast station-level hourly passenger demand across a 30-station Bus Rapid Transit (BRT) corridor.

## Model Architecture
* **Dual-Layer GCN:** Captures multi-hop spatial dependencies and downstream ripple effects across connected stations.
* **LSTM Module:** Models temporal sequence patterns over a 6-hour historical window ($T=6$).
* **Data Normalization:** Employs Min-Max scaling to stabilize high-variance passenger counts during peak hours.

## Key Results
* **$R^2$ Score:** 0.7210 (Captures 72.1% of demand variance)
* **RMSE:** 2952.25 (Outperforms ARIMA, Random Forest, XGBoost, and standard LSTM)
* **Ablation Insight:** Removing spatial graph convolutions causes temporal-only models to collapse ($R^2 = -2.7475$), proving spatial connectivity is critical.
