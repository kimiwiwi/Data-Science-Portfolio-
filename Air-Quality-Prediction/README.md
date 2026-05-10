# Air Quality Prediction

## Overview
This project predicts CO (Carbon Monoxide) concentration in the air
using machine learning regression models.

## Dataset
- Source: UCI Air Quality Dataset
- Total data: 9358 rows
- Target variable: CO(GT)

## Features Used
| Feature | Description |
|---------|-------------|
| PT08.S1(CO) | CO sensor response |
| C6H6(GT) | Benzene concentration |
| PT08.S4(NO2) | NO2 sensor response |
| PT08.S5(O3) | O3 sensor response |
| T | Temperature |
| RH | Relative Humidity |
| AH | Absolute Humidity |

## Models & Results
| Model | R2 | RMSE | MAE |
|-------|----|------|-----|
| Linear Regression | 0.058 | 77.890 | 58.092 |
| Tree | 0.715 | 42.876 | 10.637 |
| AdaBoost | 0.758 | 39.485 | 8.008 |
| Random Forest | 0.785 | 37.240 | 14.127 |

## Analysis & Findings
Based on the Explain Model (SHAP), the most influential features
for predicting CO concentration are:

1. **C6H6(GT)** - Benzene has the highest impact on CO prediction,
   both are produced by incomplete combustion from vehicle emissions.

2. **PT08.S1(CO)** - The CO sensor reading directly correlates
   with actual CO concentration as expected.

3. **T (Temperature)** - Higher temperatures affect pollutant
   dispersion in the atmosphere.

## Conclusion
Linear Regression performed poorly (R2=0.058) because the
relationship between air quality variables is non-linear.

Random Forest achieved the best performance (R2=0.785),
successfully explaining 78.5% of CO concentration patterns,
making it the most suitable model for this dataset.

## Tools
- Orange Data Mining
