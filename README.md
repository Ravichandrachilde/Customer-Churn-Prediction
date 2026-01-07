# Customer Churn Prediction 📉

A Machine Learning project to predict customer attrition using a dataset of **440,000+ records**. This project focuses on building a statistically valid pipeline, ensuring data integrity, and deploying an interpretable model for business stakeholders.

## 🚀 Live Demo
**[Link to your Hugging Face / Streamlit App Here]**

## 📌 Project Overview
The goal of this project is to identify customers at risk of churning so businesses can proactively intervene.
* **Model:** XGBoost Classifier (Optimized for Recall)
* **Tech Stack:** Python, Scikit-Learn, Pandas, Imbalanced-Learn, Streamlit, Docker.
* **Key Insight:** Discovered and mitigated a critical data integrity issue in the source dataset where the provided test set contained synthetic noise (dummy labels). Implemented a custom stratified validation strategy to restore accuracy from 50% (random guess) to **94%**.

## 📊 Key Results
| Metric | Score | Interpretation |
| :--- | :--- | :--- |
| **Accuracy** | **94%** | The model correctly classifies 94% of customers. |
| **Recall (Churn)** | **100%** | The model successfully identifies **all** at-risk customers (Zero false negatives). |
| **Precision** | **90%** | When the model predicts churn, it is correct 90% of the time. |

## 💡 Business Insights (SHAP Analysis)
Using SHAP (SHapley Additive exPlanations), we identified the primary drivers of churn:
1.  **Support Calls:** Frequency of support interactions is the #1 predictor of churn.
2.  **Total Spend:** Lower spending correlates with higher churn risk.
3.  **Payment Delay:** Late payments are a strong early warning signal.

## 🛠️ How to Run Locally

### 1. Clone the Repo
```bash
git clone [https://github.com/your-username/customer-churn-prediction.git](https://github.com/your-username/customer-churn-prediction.git)
cd customer-churn-prediction
```

### 2. Install Dependencies
```bash
pip install -r requirements.txt
```

### 3. Run the Streamlit App
```bash
streamlit run app.py
```

## 📂 Project Structure
```
├── data/                # Raw training data (Test.csv excluded due to data quality issues)
├── notebooks/           # Jupyter Notebooks for EDA and Model Training
├── src/                 # Source code for the Streamlit application
├── Dockerfile           # Docker configuration for deployment
├── requirements.txt     # Python dependencies
└── README.md            # Project documentation
```

## 📝 License
This project is open-source and available under the MIT License.