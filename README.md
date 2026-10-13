# 🛒 E-Commerce Conversion Prediction

## 📌 Project Overview
This repository contains a machine learning classification pipeline designed to predict whether a website visitor will convert (make a purchase) during their session. Originally developed to tackle a competitive analytics hackathon challenge, this project leverages customer behavior and session data to identify high-intent users, enabling targeted marketing and optimized user experiences.

## 📂 Repository Contents
* **`notebook (2).ipynb`**: The primary Jupyter Notebook containing the end-to-end workflow, including Exploratory Data Analysis (EDA), feature engineering, classification model training, and performance evaluation.

## 🛠️ Methodology & Tech Stack

### 1. Data Processing & Exploratory Data Analysis (EDA)
Understanding user journey data is critical for conversion prediction. The notebook covers:
* **Handling Missing Data:** Strategies for imputing missing session details or demographic data.
* **Behavioral Analysis:** Visualizing the relationship between session duration, page views, bounce rates, and the target conversion variable.
* **Class Imbalance Handling:** E-commerce datasets typically feature far fewer conversions than non-conversions. Techniques such as SMOTE or class-weight adjustments are utilized to ensure the model doesn't become biased toward the majority class.

### 2. Feature Engineering
Transforming raw session data into actionable predictive signals:
* **Categorical Encoding:** Converting non-numeric features (e.g., device type, traffic source, browser) into machine-readable formats using techniques like One-Hot Encoding or Target Encoding.
* **Time-Based Features:** Extracting day of the week or time of day to capture purchasing patterns.
* **Engagement Metrics:** Creating aggregated interaction scores based on the pages visited and time spent.

### 3. Model Architecture
The project employs robust classification algorithms (such as **XGBoost** or **LightGBM**) utilizing the Python data science stack (`pandas`, `scikit-learn`). 
* **Why Tree-Based Boosters?** These models are highly effective at capturing non-linear relationships in tabular behavioral data and naturally handle feature importance scaling.
* **Hyperparameter Tuning:** Cross-validation and grid search techniques are applied to optimize the model's learning rate, depth, and regularization to maximize predictive accuracy without overfitting.

## 📊 Evaluation & Metrics
To accurately measure success on an imbalanced dataset, the model is evaluated beyond standard accuracy:
* **F1-Score:** Balances precision and recall, ensuring the model effectively identifies true conversions without excessive false positives.
* **ROC-AUC (Area Under the Curve):** Evaluates the model's ability to distinguish between converting and non-converting sessions across different thresholds. *(Note: Update with your final test metrics here!)*
* **Feature Importance Plot:** Highlights the top behavioral drivers (e.g., time on page, cart additions) that lead to a successful checkout.

