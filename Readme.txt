# 🗽 NYC Yellow Taxi Trip Analysis - A/B Testing & Linear Regression

Analyze, visualize, and model the impact of **payment types** on **fare amount** using the 2017 NYC Yellow Taxi dataset.  
This project is part of the **Google Advanced Data Analytics Professional Certificate** (Course 4: Portfolio Project).

---

## 🎯 Project Goals

- 🔍 Explore the NYC Yellow Taxi dataset (2017)  
- 🧹 Clean and prepare data for analysis  
- 🧪 Conduct an A/B test comparing payment types  
- 📈 Build a Multiple Linear Regression model to predict fare amount  
- 🧠 Draw statistical insights using Python and `statsmodels`  

---

## 📌 Key Features

- ✅ **Exploratory Data Analysis (EDA)**: Descriptive stats, distributions, and correlation matrix  
- ✅ **Data Cleaning**: Removal of outliers, invalid trips, and inconsistent values  
- ✅ **Feature Engineering**: Encoding categorical `payment_type` variables  
- ✅ **A/B Testing**: Statistical comparison of mean fare amount across payment types  
- ✅ **Regression Modeling**: Linear model built with `statsmodels.OLS`  
- ✅ **Interpretation**: Analysis of p-values, confidence intervals, and R² scores  
- ✅ **Data Visualization**: Residual plots, boxplots, and histograms with `matplotlib` and `seaborn`  

---

## 📊 Technologies Used

| Category             | Tools & Libraries                             |
|----------------------|-----------------------------------------------|
| Language             | ![Python](https://img.shields.io/badge/Python-3.10-blue) |
| IDE / Platform       | Jupyter Notebook                              |
| Data Manipulation    | Pandas, NumPy                                 |
| Statistical Modeling | Statsmodels, Scikit-learn                     |
| Visualization        | Matplotlib, Seaborn                           |
| Testing              | SciPy (for t-tests), Statsmodels              |

---

## 📚 Methodology

### 🧹 1. Data Preprocessing
- Removed missing or zero values for `fare_amount`, `trip_distance`, and `passenger_count` to ensure data quality
- Detected and eliminated extreme outliers using the IQR method for robust analysis
- Converted boolean features (e.g., `payment_type_2`, `payment_type_3`) to integer format for modeling

### 📊 2. A/B Testing
- Performed two-sample t-tests to compare mean fare amounts between payment groups (e.g., credit card vs cash)
- Visualized group distributions using boxplots for clear comparison
- **Result:** Payment types showed statistically significant differences in average fare

### 🔢 3. Regression Modeling
- Selected features: `trip_distance`, `passenger_count`, and one-hot encoded `payment_type`
- Built a multiple linear regression model using `statsmodels.OLS` for interpretability
- Included intercept term with `sm.add_constant()`
- Verified model assumptions: linearity, residual normality, and homoscedasticity for reliable inference

---

## 📈 Sample Regression Output

```text
                            OLS Regression Results                            
==============================================================================
Dep. Variable:           fare_amount   R-squared:                       0.623
Model:                            OLS   Adj. R-squared:                  0.620
Method:                 Least Squares   F-statistic:                     112.3
Date:                Sat, 04 May 2025   Prob (F-statistic):           <0.001
==============================================================================
```

> 🔹 **Interpretation**: The model explains ~62% of the variance in fare amount.  
> 🔹 **Significant predictors**: `trip_distance`, `payment_type_2`, `payment_type_3`  
> 🔹 **Most influential variable**: `trip_distance`

---

## 📷 Visualizations

* 📌 **Fare Amount Distribution**  
* 📌 **Trip Distance vs Fare Scatterplot**  
* 📌 **Boxplot of Fare by Payment Type**  
* 📌 **Residual Plot for Regression Model**  
* 📌 **Correlation Heatmap**  


> Boxplot shows that different payment methods result in different median fare amounts.

---

## 🧾 Requirements

```text
pandas  
numpy  
matplotlib  
seaborn  
statsmodels  
scikit-learn  
scipy  
```

---

## 📌 Conclusion

* A/B testing showed significant differences in fare amount across payment methods  
* Linear regression confirmed that **trip distance** is the strongest predictor  
* `statsmodels` provided interpretable outputs with statistical summaries  
* Results help stakeholders (e.g., taxi companies) understand pricing dynamics  

---

## 👤 Author

**Ghulam Mujtaba**  
🎓 BS Software Engineering @ COMSATS Lahore  
🔗 [Portfolio](https://ghulammujtaba.com) • [LinkedIn](https://linkedin.com/in/ghulamujtabaofficial) • [GitHub](https://github.com/ghulam-mujtaba5)

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 🙏 Acknowledgements

* Google Advanced Data Analytics Professional Certificate (Course 4)  
* NYC TLC for providing the open dataset  
* Statsmodels & Seaborn documentation for guidance
