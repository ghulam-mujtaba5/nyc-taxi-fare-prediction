# 🗽 NYC Yellow Taxi Trip Analysis — A/B Testing & Linear Regression

Analyze, visualize, and model the impact of payment types on fare amount using the 2017 NYC Yellow Taxi dataset.

<p align="left">
  <img alt="Python" src="https://img.shields.io/badge/Python-3.9%2B-3776AB?logo=python&logoColor=white" />
  <img alt="Jupyter" src="https://img.shields.io/badge/Made%20with-Jupyter-F37626?logo=jupyter&logoColor=white" />
  <img alt="License" src="https://img.shields.io/badge/License-MIT-0A66C2" />
  <img alt="Status" src="https://img.shields.io/badge/Status-Active-22c55e" />
</p>

---

## 📌 Contents
- [Overview](#-overview)
- [Dataset](#-dataset)
- [Project Structure](#-project-structure)
- [Setup](#-setup)
- [Usage](#-usage)
- [Methodology](#-methodology)
- [Results](#-results)
- [Requirements](#-requirements)
- [License](#-license)
- [Author](#-author)

---

## 🎯 Overview
This repo explores the 2017 NYC Yellow Taxi trips to study how different payment methods relate to fare amounts. It includes EDA, an A/B test across payment types, and a multiple linear regression model using statsmodels for interpretability.

---

## 🗂️ Dataset
- Local file: `2017_Yellow_Taxi_Trip_Data.csv`
- Source: NYC TLC (2017 Yellow Taxi Trip Records)

Tip: If the CSV is large, consider sampling for faster experimentation.

---

## 🧭 Project Structure
```
nyc-taxi-fare-prediction/
├─ 2017_Yellow_Taxi_Trip_Data.csv       # dataset (2017)
├─ project.ipynb                         # main analysis notebook (v1)
├─ project1.2.ipynb                      # updated/extended analysis (v1.2)
├─ README.md                             # this file
└─ requirements.txt                      # Python dependencies
```

---

## ⚙️ Setup
```bash
# 1) create & activate a virtual environment (recommended)
python -m venv .venv
# Windows PowerShell
. .venv\Scripts\Activate.ps1

# 2) install dependencies
pip install -r requirements.txt

# 3) start Jupyter
jupyter notebook
```

---

## ▶️ Usage
Open one of the notebooks and run cells top-to-bottom:
- `project.ipynb`
- `project1.2.ipynb`

Key steps covered in notebooks:
- Load and clean the dataset
- Exploratory data analysis (EDA)
- A/B testing across payment types
- Regression modeling (`statsmodels.OLS`)
- Interpretation and visualizations

---

## 📚 Methodology
1) Data Preprocessing
- Drop invalid values for `fare_amount`, `trip_distance`, `passenger_count`
- Remove outliers (IQR)
- One-hot encode `payment_type`

2) A/B Testing
- Two-sample t-tests (e.g., credit vs cash)
- Visualize distributions (boxplots)

3) Regression Modeling
- Features: `trip_distance`, `passenger_count`, one-hot `payment_type`
- Model: `statsmodels.OLS` with intercept (`sm.add_constant`)
- Assumptions: linearity, residual normality, homoscedasticity

---

## 📈 Results
Example OLS summary indicates ~62% variance explained (R² ≈ 0.62). The strongest predictor is typically `trip_distance`; payment indicators can be statistically significant.

Add plots/screens here for better presentation:
- Fare distribution, boxplots by payment type
- Residual diagnostics
- Correlation heatmap

---

## 🧾 Requirements
See `requirements.txt`. Core stack:
- pandas, numpy, scipy
- matplotlib, seaborn
- statsmodels, scikit-learn
- jupyter

---

## 📄 License
MIT — see `LICENSE` (add one if missing).

---

## 👤 Author
**Ghulam Mujtaba**  
Portfolio: https://ghulammujtaba.com  
LinkedIn: https://linkedin.com/in/ghulamujtabaofficial  
GitHub: https://github.com/ghulam-mujtaba5
