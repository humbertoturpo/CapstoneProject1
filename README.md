# **Short-Term Forecasting of Monthly Fresh Ginger Exports from Peru Using Regression Models and Google Trends Indicators**

**Author**: Humberto Sebastian Turpo Huaman

---

## **Executive Summary**
This project predicts Peru's monthly ginger exports through short-term forecasting methods, combining lag-based regression with Google Trends data. The baseline model uses lagged exports as the sole predictor, while enhanced models integrate Google search trends (Web, YouTube, Image, and News searches) from the previous month. Results show that incorporating Google Trends significantly improves accuracy, with Lasso regression performing best. Future work includes neural networks and dataset expansion using Gaussian noise.

---

## **Rationale**
Peru, as a global leader in ginger exports, requires accurate short-term forecasting tools to manage supply chains and anticipate demand. Integrating search behavior from the prior month offers timely, actionable insights to enhance trade decisions.

### References


1. **Collison (2020)**  
   *Performance Assessment of Google Trend Index in Forecasting Car Sales in Argentina*.  
   Published on *SSRN*.  
   - **Enhanced R-squared:** From 0.283 to 0.495 by incorporating Google Trends data.

2. **Başyiğit (2021)**  
   *Can Google Trends Improve the Marble Demand Model: A Case Study of USA's Marble Demand from Turkey*.  
   Published in *Resource Policy*.  
   - **Increased R-squared:** From 0.85 to 0.90 when integrating search trends.

3. **Yu et al. (2019)**  
   *Online Big Data-Driven Oil Consumption Forecasting with Google Trends*.  
   Published in *International Journal of Forecasting*.  
   - **Improvement in R-squared:** Up to 4% with advanced machine learning techniques like Extreme Machine Learning.



---

## **Research Question**
**Can the inclusion of Google Trends indicators improve the accuracy of a lag-based regression model in predicting Peru’s monthly ginger exports?**

---

## **Data Sources**
1. **Export Data**: Monthly export volumes sourced from TradeMap.  
2. **Google Trends Indicators**: Search interest data (Web, YouTube, Image, and News searches) retrieved from Google Trends.
   - **Temporal Alignment**: Search data corresponds to the month prior to the export period, ensuring alignment with lagged market behavior.

---

## **Methodology**
1. **Baseline Model**: Linear regression using lagged exports as the sole predictor.  
2. **Enhanced Models**: Linear, Lasso, and Ridge regression incorporating Google Trends indicators.  
3. **Evaluation Metrics**: R-squared, RMSE, MAE, and Explained Variance were used to assess model performance.  
4. **Future Methods**: Neural networks will be applied to improve accuracy, supported by data augmentation techniques like Gaussian noise.

---

## **Results**

### **Baseline Model**
- **R-squared**: 0.7276  
- **Observations**: The baseline model captures general trends but lacks precision in capturing variability, relying solely on lagged exports.

---

### **Enhanced Models with Google Trends Data**

#### **Linear Regression with Google Trends**
- **R-squared**: 0.7845  
- **RMSE**: 929,083.47  
- **MAE**: 733,865.00  
- **Observations**: Google Trends indicators provide moderate improvement over the baseline, especially during high-variability months.

#### **Lasso Regression**
- **R-squared**: 0.8457  
- **RMSE**: 782,395.13  
- **MAE**: 636,855.11  
- **Key Features**: Web and YouTube searches from the prior month emerged as the most significant predictors, strongly correlating with export trends.  
- **Observations**: Lasso regression achieves the best overall performance, demonstrating the value of feature selection.

#### **Ridge Regression**
- **R-squared**: 0.8356  
- **RMSE**: 806,033.33  
- **MAE**: 667,165.05  
- **Observations**: Ridge regression balances feature contributions and mitigates multicollinearity, though slightly underperforming compared to Lasso.

---

### **Key Comparisons**
| Model                | R-squared | RMSE         | MAE         | Observations                                    |
|----------------------|-----------|--------------|-------------|------------------------------------------------|
| **Baseline (Lag Only)** | 0.7276    | -            | -           | Relies solely on lagged data, missing variability. |
| **Linear Regression**  | 0.7845    | 929,083.47   | 733,865.00  | Benefits from additional predictors.           |
| **Lasso Regression**   | 0.8457    | 782,395.13   | 636,855.11  | Most accurate model with effective feature selection. |
| **Ridge Regression**   | 0.8356    | 806,033.33   | 667,165.05  | Stable performance, slightly less accurate than Lasso. |

---

### **Feature Importance**
- **Lasso Regression**: Web and YouTube searches from the previous month dominate as predictive features, reflecting timely shifts in market demand.  
- **Ridge Regression**: More balanced feature contributions capture secondary trends from Image and News searches.

---


---

## **Next Steps**
1. **Neural Networks**: Explore advanced architectures, such as recurrent neural networks (RNNs) or long short-term memory (LSTM) networks, to model non-linear relationships.  
2. **Dataset Expansion**: Apply Gaussian noise to augment the dataset, creating diverse scenarios for better generalization and robustness.  
3. **Model Optimization**: Focus on hyperparameter tuning for both regression and neural network models to maximize performance.

---

## **Outline of Project**
[Dataset](https://github.com/humbertoturpo/CapstoneProject1/blob/main/data/gingerperu2.xlsx)

[Notebook](https://github.com/humbertoturpo/CapstoneProject1/blob/main/GingerGoogleTrendsPeru.ipynb)






## **Contact and Further Information**
**Humberto Sebastian Turpo Huaman**  
[sebastian.turpo@gmail.com]  

---
