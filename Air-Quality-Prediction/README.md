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

## Conclusion
Random Forest achieved the best R2 score of 0.785,
meaning the model explains 78.5% of CO concentration patterns.

## Tools
- Orange Data Mining
