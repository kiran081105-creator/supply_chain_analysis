# supply_chain_analysis

📦 Supply Chain Delivery Prediction & Analytics
Late Delivery Classification + Shipping Time Prediction + Power BI Dashboard

This project analyzes a large supply chain dataset and builds two machine learning models:

Late Delivery Prediction (Classification Model)

Shipping Time Prediction (Regression Model)

It also includes an interactive Power BI dashboard for visualization and business insights.

📁 Project Features

🔹 1. Late Delivery Prediction (Classification)

Predicts whether an order will be delivered Late (1) or On-time (0)

Achieved 97.5% accuracy

Perfect recall of 1.00 for late deliveries

Helps logistics teams proactively handle delay-risk orders

🔹 2. Shipping Time Prediction (Regression)

Predicts the number of days taken for shipping

MAE: 0.98 days (avg error ≈ 1 day)

RMSE: 1.26 days

R² Score: 0.38

Useful for improving delivery-time estimation and customer communication

🔹 3. Power BI Dashboard

Interactive visualizations including:

Shipping days distribution

Delay patterns across regions

Shipping mode performance

Predictive insights

KPI summary

📊 Dataset Overview

Columns used:

Logistics variables: Days for shipping, scheduled shipping days, shipping mode

Order details: Sales, item quantity, product price

Location: Order region, order state

Date features: Order month, weekday

Target variables:

Late_delivery_risk (Classification)

Days for shipping (real) (Regression)

Dataset Size: >180,000 rows

🧠 Machine Learning Models
Model 1: Late Delivery Prediction

Algorithm: Random Forest Classifier

Metrics:

Accuracy: 97.54%

Precision (Late = 1): 0.96

Recall (Late = 1): 1.00

F1-Score: 0.98

Key Feature Importances:

Feature	Importance
Days for shipping (real)	31%
shipping_days	26%
Shipping Mode	21%
Days for shipment (scheduled)	20%
Others combined	<2%

Insight:
Delays are driven almost entirely by logistics timing and shipping mode, not customer or product attributes.

Model 2: Shipping Time Prediction

Algorithm: Random Forest Regressor

Performance:

MAE: 0.98

RMSE: 1.26

R²: 0.38

Insight:
Model predicts with ~1 day average error.
More operational features (distance, carrier-level metrics) would improve accuracy.

📈 Power BI Dashboard

The Power BI dashboard includes:

Key Visuals

Distribution of real shipping days

Shipping days comparison by shipping mode

Top regions with highest shipping time

Delay hotspots

Monthly shipping trend analysis

KPI cards (Avg shipping days, Late delivery %, Total orders)

Highlights

📌 Business Insights Summary

Actual shipping duration and shipping mode are the biggest drivers of delays.

Regions such as Central Africa, East Asia, and West Africa experience longer average shipping times.

Standard and Second Class shipping modes have higher variability and more delays.

Same Day and First Class modes provide consistent, fast delivery.

Late delivery prediction model is highly accurate and can be used for real-time risk detection.

Shipping time prediction can improve delivery promise accuracy by about 1 day.

🚀 Future Improvements

Add geolocation/distance-based features

Include carrier-level performance data

Deploy model as API (Flask/FastAPI)

Add a Streamlit dashboard

Enable automated Power BI refresh
Central Africa, Eastern Asia, and West Africa have the longest average shipping times

Same Day and First Class modes are the fastest and most consistent

📦 Supply-Chain-Delivery-Prediction
│
├── data/
│   └── DataCoSupplyChainDataset.csv
│
├── notebooks/
│   ├── Late_Delivery_Prediction.ipynb
│   └── Shipping_Time_Prediction.ipynb
│
├── models/
│   ├── late_delivery_model.pkl
│   └── shipping_time_model.pkl
│
├── powerbi/
│   └── SupplyChain_Dashboard.pbix
│
├── images/
│   ├── confusion_matrix.png
│   ├── feature_importance.png
│   ├── shipping_mode_boxplot.png
│   └── region_shipping_time.png
│
└── README.md

