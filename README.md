# Yes Bank Stock Price Prediction

## Project Overview
This project focuses on the analysis and prediction of Yes Bank's stock prices using historical market data. The project is divided into two main phases: **Exploratory Data Analysis (EDA)** to uncover trends and patterns, and **Machine Learning (ML)** to build a robust predictive regression model for the stock's closing price.

---

## Repository Contents
1. **`YesBank_EDA_Tanim_2.ipynb`**: Contains the complete exploratory analysis, including data cleaning, feature extraction (Year, Month), statistical hypothesis testing, and 15+ comprehensive visualizations to understand stock market behavior[cite: 6].
2. **`YesBank_ML_Tanim_2.ipynb`**: Contains the full machine learning pipeline, including feature engineering, data transformation (Log Transformation), scaling, and the implementation and hyperparameter tuning of multiple regression models (Ridge, Random Forest, Gradient Boosting)[cite: 7].

---

## Project Workflow

### Phase 1: Exploratory Data Analysis (EDA)
* **Data Cleaning:** Handled data formatting (Date conversion) and validated the integrity of the dataset[cite: 6].
* **Visualization (UBM Rule):** 
    * **Univariate:** Analyzed the distribution of closing prices and feature volatility[cite: 6].
    * **Bivariate:** Examined the linear relationship between Open, High, Low, and Close prices[cite: 6].
    * **Multivariate:** Used heatmaps and pairplots to understand multicollinearity among financial features[cite: 6].
* **Hypothesis Testing:** Conducted Pearson Correlation, T-Tests, and ANOVA to validate assumptions about stock price relationships and seasonality[cite: 6].

### Phase 2: Machine Learning (ML)
* **Feature Engineering:** Created a `Volatility` feature (High - Low) to capture intra-month market instability[cite: 7].
* **Data Preprocessing:** Applied Log Transformation to normalize right-skewed price data and `StandardScaler` to normalize feature scales for model stability[cite: 7].
* **Modeling:**
    * **Ridge Regression (Baseline):** Best-performing model due to the linear nature of the financial features[cite: 7].
    * **Random Forest & Gradient Boosting:** Evaluated for non-linear pattern capturing[cite: 7].
* **Model Optimization:** Used `GridSearchCV` with cross-validation to find optimal parameters[cite: 7].
* **Deployment Ready:** The final model is serialized and saved using `joblib` for future integration[cite: 7].

---

## Key Insights
* The stock exhibits an extremely high positive correlation between Open, High, Low, and Close prices ($r \approx 0.99$)[cite: 6].
* Market volatility spiked significantly during the 2018–2020 period, marking the company’s financial crisis[cite: 6].
* The **Ridge Regression** model provided the most reliable predictions, proving that a linear approach best captures Yes Bank's stock price dynamics[cite: 7].

---

## Tech Stack
* **Language:** Python
* **Libraries:** 
    * `pandas`, `numpy` (Data manipulation)
    * `matplotlib`, `seaborn` (Visualization)
    * `scikit-learn` (Machine Learning & Preprocessing)
    * `scipy` (Statistical testing)
    * `joblib` (Model serialization)

---

## How to Use
1. Clone the repository: `git clone https://github.com/tanimnaha/YesBank-Stock-Price-Prediction.git`
2. Ensure you have the required libraries installed:
   `pip install pandas numpy matplotlib seaborn scipy scikit-learn joblib`
3. Open the `.ipynb` files in Jupyter Notebook or Google Colab to run the analysis or the prediction pipeline.

---
**Author:** Tanim Naha  
*Created as part of an Individual Machine Learning Capstone Project.*