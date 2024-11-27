# **Short-Term Forecasting of Monthly Fresh Ginger Exports from Peru Using Regression Models and Google Trends Indicators**

**Author**: Humberto Sebastian Turpo Huaman

---

## **Executive Summary**
This project predicts Peru's monthly ginger exports through short-term forecasting methods, combining lag-based regression with Google Trends data. The baseline model uses lagged exports as the sole predictor, while enhanced models integrate Google search trends (Web, YouTube, Image, and News searches) from the previous month. Results show that incorporating Google Trends significantly improves accuracy, with Lasso regression performing best. Future work includes neural networks and dataset expansion using Gaussian noise.

---

## **Rationale**
Peru, a leading global exporter of ginger, faces challenges in accurately forecasting monthly export volumes to optimize supply chain management and meet global demand. Traditional models relying solely on lagged export data often fail to capture dynamic shifts in market interest. Emerging research highlights the predictive power of online search data, particularly Google Trends, in improving trade forecasting. Studies across various industries, such as Brazilian soybean exports and Turkish marble demand, have demonstrated significant R-squared improvements when integrating search indices.







### References



A. **Başyiğit (2021)**  
   *Can Google Trends Improve the Marble Demand Model: A Case Study of USA's Marble Demand from Turkey*.  
   Published in *Resource Policy*.  
   - **Increased R-squared:** From 0.85 to 0.90 when integrating search trends.

B. **Yu et al. (2019)**  
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

- **Exports**: Represents the monthly ginger export volumes from Peru.
- **Exports12**: Refers to lagged data of export volumes, specifically a 12-month lag.
- **Web**: Indicates lagged search interest data from general web searches associated with food and beverage topics, representing the previous month.
- **YouTube**: Refers to lagged search interest data from YouTube, capturing food and beverage-related trends from the prior month.
- **Images**: Represents lagged search interest data from image-based searches related to food and beverage, conducted a month earlier.
- **News**: Refers to lagged search interest data from news-related searches about food and beverage, reflecting public interest from the previous month.


- The **Exports** tag provides the primary dependent variable for forecasting.
- All other tags (Exports12, Web, YouTube, Images, News) are lagged variables, capturing trends from one month prior. These lagged indices specifically track online searches related to food and beverage topics, enabling predictive modeling by aligning consumer search behavior with subsequent export activities.




---

## **Methodology**
1. **Baseline Model**: Linear regression using lagged exports as the sole predictor.  
2. **Enhanced Models**: Linear, Lasso, and Ridge regression incorporating Google Trends indicators.  
3. **Evaluation Metrics**: R-squared, RMSE, MAE, and Explained Variance were used to assess model performance.  
4. **Future Methods**: Neural networks will be applied to improve accuracy, supported by data augmentation techniques like Gaussian noise.

---

## **Results**

### **Baseline Model - Simple Linear Regression (No ML Involved)**
- **R-squared**: 0.7276  
- **Observations**: The baseline model captures general trends but lacks precision in capturing variability, relying solely on lagged exports.

---

### **Enhanced Models with Google Trends Data**

#### **Multiple Linear Regression with Google Trends**
- **R-squared**: 0.7845  
- **RMSE**: 929,083.47  
- **MAE**: 733,865.00  
- **Observations**: Google Trends indicators(except YouTube) provide moderate improvement over the baseline, especially during high-variability months.

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
| **Multiple Linear Regression**  | 0.7845    | 929,083.47   | 733,865.00  | Benefits from additional predictors.           |
| **Lasso Regression**   | 0.8457    | 782,395.13   | 636,855.11  | Most accurate model with effective feature selection. |
| **Ridge Regression**   | 0.8356    | 806,033.33   | 667,165.05  | Only include lags.  |

---

### **Feature Importance**
- **Multiple linear regression**: Web and Images  searches from the previous month dominate as predictive features, reflecting timely shifts in market demand.  
- **Lasso Regression**: Web and YouTube searches from the previous month dominate as predictive features, reflecting timely shifts in market demand.  
- **Ridge Regression**: Only include lags.

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
