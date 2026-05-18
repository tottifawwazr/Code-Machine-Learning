# Gold Price Forecasting Using Stacking GRU–CNN and Macroeconomic Indicators

## 1. Title

**Project Name:** Gold Price Forecasting Using Stacking GRU–CNN and Macroeconomic Indicators
**Research Domain:** Financial Time-Series Forecasting
**Forecasting Target:** Daily Gold Prices / Gold Returns
**Period Covered:** 1990–2025

---

# 2. Project Description

This project develops machine learning and deep learning models for forecasting gold prices using financial market indicators and macroeconomic variables. The study evaluates several baseline and tuned forecasting models, including:

* XGBoost
* Random Forest
* GRU
* LSTM
* CNN
* Stacking GRU–CNN Ensemble

The framework incorporates feature engineering, rolling forecasting evaluation, ensemble learning, and explainable AI analysis using SHAP.

---

# 3. Dataset Information

The dataset combines daily gold prices with macroeconomic and financial indicators commonly associated with gold market dynamics.

## Variables Used

### Financial Market Variables

* GOLD_CLOSE
* SILVER_CLOSE
* SP500
* VIX
* WTI
* COPPER

### Macroeconomic Variables

* FED_FUNDS
* CPI_ACTUAL
* TREASURY_10Y
* REAL_YIELD
* REAL_INTEREST_RATE
* M2

### Engineered Features

* RET_PAST_1
* RET_PAST_3
* RET_PAST_5
* VOL_5
* VOL_20
* MONTH
* DAY
* DAY_OF_WEEK
* IS_WEEKEND

---

# 4. Project Structure

```text
Gold-Price-Forecasting/
│
├── Code/
│   ├── ML_4_Desember.ipynb
│   └── Supporting Scripts
│
├── Dataset/
│   └── Gold_Silver_Forecasting.xlsx
│
├── Figures/
│   ├── Figure_1_Research_Pipeline.pdf
│   ├── Figure_2_Data_Gathering_Stage.pdf
│   ├── Figure_3_Data_Preprocessing_Stage.pdf
│   ├── Figure_4_Baseline_GRU_and_CNN_Predictions_vs_Actual_Prices_Full_Range_2020_2025.png
│   ├── Figure_5_Zoomed_in_Baseline_Predictions_2024_2025.png
│   ├── Figure_6_Tuned_Model_Predictions_vs_Actual_Test_Set.png
│   ├── Figure_7_Zoom_in_View_2024_2025_Start.png
│   ├── Figure_8_Stacking_GRU_CNN_Tuned_Actual_vs_Predicted_Test_Set.png
│   ├── Figure_9_Zoom_In_Stacking_GRU_CNN_Tuned_2024_2025_Start.png
│   ├── Figure_10_Rolling_Forecast_Stacking_GRU_CNN_Tuned_vs_Actual_Full_Period.png
│   ├── Figure_11_Rolling_Forecast_Zoom_In_2024_2025.png
│   ├── Figure_12_Meta_Learner_Weight_Bar_Plot.png
│   ├── Figure_13_SHAP_Feature_Importance_Bar_Plot.png
│   ├── Figure_14_Residuals_Over_Time_Stacking_GRU_CNN_Test_Set.png
│   ├── Figure_15_Residual_Distribution.png
│   ├── Figure_16_Q_Q_Plot_of_Residuals.png
│   └── Figure_17_Residual_Autocorrelation_Function_ACF.png
│
├── Tables/
│   ├── Table_1_Baseline_Model_Performance_Test_Set.docx
│   ├── Table_2_Qualitative_Assessment_of_Baseline_Models.docx
│   ├── Table_3_Tuned_Model_Performance_Test_Set.docx
│   ├── Table_4_Qualitative_Assessment_of_Tuned_Models.docx
│   ├── Table_5_Stacking_GRU_CNN_Performance_Test_Set.docx
│   ├── Table_6_Stacking_GRU_CNN_Tuned_Rolling.docx
│   ├── Table_7_Diebold_Mariano_Test_Results_Test_Set.docx
│   ├── Table_8_Diebold_Mariano_Significance_Test_Summary.docx
│   ├── Table_9_Meta_Learner_Coefficients_for_GRU_and_CNN.docx
│   ├── Table_10_SHAP_Global_Feature_Importance.docx
│   └── Table_11_Residual_Summary_Statistics_Stacking_GRU_CNN_Test_Set.docx
│
├── Paper/
│   └── Final_Paper.docx
│
├── README.md
└── requirements.txt
```

---

# 5. Methodology

## Data Gathering

Financial and macroeconomic datasets were collected from publicly available financial databases covering the period 1990–2025.

## Data Preprocessing

* Missing value removal
* Gold return transformation
* Feature scaling
* Feature engineering
* Chronological train-validation-test split

## Feature Engineering

Several temporal and statistical features were generated:

* Lag returns
* Rolling volatility
* Calendar-based features

## Forecasting Models

### Baseline Models

* XGBoost
* Random Forest
* GRU
* LSTM
* CNN

### Tuned Models

Hyperparameter optimization was applied to improve forecasting performance.

### Ensemble Learning

A stacking framework combining GRU and CNN predictions was developed using a meta-learner.

---

# 6. Evaluation Metrics

The forecasting models were evaluated using:

* RMSE (Root Mean Squared Error)
* MAE (Mean Absolute Error)
* MAPE (Mean Absolute Percentage Error)
* Diebold–Mariano Statistical Test
* Residual Analysis
* SHAP Explainability Analysis

---

# 7. Key Findings

* Tuned GRU and CNN models outperformed several baseline approaches.
* The stacking GRU–CNN ensemble achieved improved forecasting accuracy.
* GOLD_CLOSE and SP500 were identified as the most influential variables in the surrogate explainability analysis.
* Residual analysis indicated relatively stable forecasting behavior across the test period.

---

# 8. Requirements

Install the required Python libraries:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn tensorflow xgboost shap statsmodels
```

Additional libraries:

* scipy
* joblib
* openpyxl

---

# 9. Usage Instructions

## Step 1 — Load Dataset

Load the gold price and macroeconomic datasets.

## Step 2 — Run Preprocessing

Perform feature engineering and scaling.

## Step 3 — Train Models

Train baseline and tuned forecasting models.

## Step 4 — Run Stacking Ensemble

Generate ensemble predictions using GRU and CNN outputs.

## Step 5 — Evaluate Performance

Compute RMSE, MAE, MAPE, and statistical evaluation metrics.

## Step 6 — Generate Explainability Analysis

Run SHAP-based feature importance analysis.

---

# 10. Explainability and Statistical Analysis

This project includes:

* SHAP global feature importance analysis
* Residual diagnostics
* Residual autocorrelation analysis
* Q–Q plot analysis
* Diebold–Mariano significance testing

---

# 11. Research Contribution

This study demonstrates the effectiveness of combining deep learning architectures and ensemble learning strategies for financial time-series forecasting using macroeconomic indicators.

---

# 12. Citation

If you use this project, please cite the corresponding research paper.

---

# 13. License

This project is intended for academic and research purposes.

---

# 14. Repository and DOI

## GitHub Repository

Add your GitHub repository link here.

## DOI

Add your Zenodo DOI here after publication.
