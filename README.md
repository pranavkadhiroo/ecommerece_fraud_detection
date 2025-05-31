# 🕵️‍♂️ Fraud Detection in E-Commerce Sessions

This project analyzes user behavior data from an e-commerce platform to detect fraudulent sessions using feature engineering, anomaly detection, and machine learning classification. Designed to mimic real-world business analysis tasks, it provides actionable insights to minimize fraud and optimize user conversion.

## 📌 Objective

- Identify high-risk user sessions based on behavioral anomalies.
- Build a machine learning model to predict potential fraudulent activity.
- Extract meaningful business insights and visualize fraud trends over time.

## 📊 Dataset

- Source: [E-Commerce Behavior Data from Multi Category Store — Kaggle](https://www.kaggle.com/datasets/mkechinov/ecommerce-behavior-data-from-multi-category-store)
- Size: ~10 million event-level records.
- Columns: `event_time`, `event_type`, `product_id`, `category_id`, `category_code`, `brand`, `price`, `user_id`, `user_session`.

## 🧪 Key Features Created

- `session_duration_min`: Time spent in a session.
- `total_spent`: Total value of products viewed or bought.
- `num_views`, `num_cart`, `num_purchase`: User engagement metrics.
- `unique_brands`, `unique_categories`: Diversity of interaction.

## 🛠️ Methods Used

### 🧹 Data Preprocessing
- Parsed timestamps and grouped by session.
- Generated session-level behavioral features.
- Normalized numerical features for anomaly detection.

### 🔍 Anomaly Detection
- **Z-Score** based method to flag statistical outliers.
- **Isolation Forest** to detect non-linear anomalies.

### 🧠 Machine Learning
- Built classification model to predict fraud using:
  - Logistic Regression / Random Forest / Gradient Boosting
- Achieved **99%+ accuracy** (validated with data shuffling to avoid overfitting).

### 📈 Trend Analysis
- Time-series plots of fraudulent activity.
- Comparison of high-fraud vs normal user behaviors.

### 📌 Key Business Insights
- High-fraud sessions show 10x longer durations and 5x more product views.
- Fraud tends to cluster around high spenders and frequent cart-adders.
- Anomalous patterns align well with high-fraud labels — validating model effectiveness.

## 🛠 Tech Stack

- Python (Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn)
- SQL (for scalable data storage & querying)
- Jupyter Notebook
- Git/GitHub

## 🧾 How to Use

1. Clone this repository.
2. Download the dataset from Kaggle and place it in the `data/` folder.
3. Run the `fraud_detection.ipynb` notebook step by step.


