# Customer_Segmentation_in_Retail_Banking: Apex_Trust_Bank
This project develops a machine learning-based customer segmentation system that transforms transactional data into actionable insights using RFM analysis and clustering techniques. 


## Customer Value Segmentation for ApexTrust Bank

### Project Overview

This project develops a data-driven customer segmentation system for ApexTrust Bank, leveraging transactional data to uncover behavioral patterns and classify customers into meaningful segments.

The solution uses RFM (Recency, Frequency, Monetary) analysis combined with machine learning (K-Means clustering) to transform raw banking transactions into actionable business insights that support personalization, retention, and revenue optimization.

### Business Problem

ApexTrust Bank currently relies on basic demographic and account-based segmentation, which fails to capture real customer behavior. This leads to:

- Poor targeting of marketing campaigns
- Difficulty identifying high-value customers
- Lack of proactive churn detection
- Underutilization of transactional data

### Project Objectives

- Build a scalable data pipeline for transaction data
- Perform exploratory data analysis (EDA)
- Engineer behavioral features (RFM + additional metrics)
- Apply K-Means clustering for segmentation
- Profile customer segments and generate insights
- Develop interactive dashboards
- Deploy model via FastAPI + Streamlit
- Ensure reproducibility with Docker & CI/CD

### Dataset Description

Database: SQLite3 / MongoDB
Table: Customer_Transactions

### Key Features:

- CustomerID – Unique customer identifier
- TransactionDate, TransactionTime – Time-based behavior
- TransactionAmount – Monetary value
- CustAccountBalance – Financial health indicator
- CustomerDOB, CustGender, CustLocation – Demographics

Each customer has multiple transactions (one-to-many relationship), enabling behavioral analysis.

### Project Workflow

1. Data Acquisition

Extract data from SQLite3,
Load into Pandas for analysis.

2. Data Cleaning & Preprocessing

Handle missing values,
Convert data types,
Remove duplicates and outliers.

3. Exploratory Data Analysis (EDA)

Analyze distributions and trends,
Identify anomalies and patterns.

4. Feature Engineering

Compute RFM metrics:
Recency,
Frequency,
Monetary.

Additional features:
Average transaction value,
Transaction timing patterns,
Customer age.

5. Machine Learning (Segmentation)

Apply K-Means clustering,
Determine optimal clusters:Elbow Method, Silhouette Score.

6. Segment Profiling

Label segments (e.g., Champions, Loyal, At-Risk),
Analyze behavior and value contribution.

7. Deployment

FastAPI (backend API),
Streamlit (dashboard UI),
Docker (containerization),
Render / AWS EC2 (cloud deployment).

### Tech Stack

- Data & Analysis
- Python (Pandas, NumPy)
- SQL (SQLite3)
- Visualization
- Matplotlib, Seaborn
- Streamlit
- Machine Learning
- Scikit-learn (K-Means)
- Backend & Deployment
- FastAPI
- Docker
- Render / AWS EC2
- DevOps & Tracking
- Git & GitHub
- MLflow (experiment tracking)
 
### Key Results & Insights

#### Identified distinct customer segments, including:

- High-value customers
- Loyal users
- Occasional users
- At-risk customers

#### Improved understanding of:

- Customer engagement patterns
- Spending behavior
- Revenue contribution

#### This will Enable:

- Targeted marketing strategies
- Personalized financial services
- Early churn detection

### Business Impact

- Increased marketing efficiency and conversion rates
- Better identification of high-value customers
- Reduced customer churn through early intervention
- Personalized product recommendations
- Faster, data-driven decision-making
- System Architecture

Database → Data Processing → Feature Engineering → ML Model → API → Dashboard

Data stored in SQLite/MongoDB

Processed with Python

Model served via FastAPI

Visualized with Streamlit

Deployed using Docker + Cloud

### Project Structure

customer-segmentation/
│
├── data/                   # Raw & processed data
├── notebooks/              # EDA & analysis notebooks
├── src/                    # Core scripts (preprocessing, modeling)
├── models/                 # Saved models
├── api/                    # FastAPI backend
├── dashboard/              # Streamlit app
├── docker/                 # Docker configuration
├── tests/                  # Unit tests
├── requirements.txt        # Dependencies
├── README.md               # Project documentation
└── .github/workflows/      # CI/CD pipelines

### How to Run the Project

1. Clone the Repository
git clone https://github.com/isiakpereaghogho/customer-segmentation.git
cd customer-segmentation
2. Create Virtual Environment
python -m venv apexbank_env apexbank_env\Scripts\activate   # Windows
3. Install Dependencies
pip install -r requirements.txt
4. Run the API
uvicorn api.main:app --reload
5. Run Dashboard
streamlit run dashboard/app.py

### Future Improvements

Real-time segmentation system
Integration with CRM tools
Advanced clustering techniques (DBSCAN, hierarchical)
Predictive churn modeling
Recommendation engine


### CONCLUSION

This project demonstrates how data science can transform raw transactional data into strategic business insights, enabling financial institutions to deliver personalized, efficient, and competitive services in a digital-first world.