# Loan Customer Segmentation & Targeting

![screenshot-localhost_8888-2025 04 07-10_50_08](https://github.com/user-attachments/assets/724d3f12-63f6-46f6-ac3a-b4346493b7c9)

### Overview

This project leverages machine learning clustering techniques to segment loan applicants into distinct groups based on financial profiles, demographics, and loan behavior. The goal is to optimize marketing strategies, improve approval rates, and mitigate risk by tailoring loan products to each segment.

### Dataset

#### Columns
- Demographics: Gender, Married, Dependents, Education, Self_Employed
- Financials: ApplicantIncome, CoapplicantIncome, LoanAmount, Loan_Amount_Term, Credit_History
- Property: Property_Area (Urban/Rural/Semiurban)
- Target: Loan_Status (Y/N)

### Key Steps

1. Data Preprocessing
- Handled missing values (median for numerical, mode for categorical).
- Engineered features:
- Income_to_Loan_Ratio, EMI, EMI_to_Income_Ratio.
- Log-transformed skewed features (LoanAmount, Total_Income).
- Encoded categorical variables (One-Hot Encoding).

2. Clustering (K-Means)
- Optimal Clusters: Determined via the Elbow Method (k=5) and Silhouette Score (best: 0.747 for k=3).
- Final Model: Used k=5 for granular segmentation.

3. Visualization & Analysis
- PCA: Reduced dimensions to 2 components for cluster visualization.
- Radar Charts: Compared clusters across key metrics (income, loan size, approval rate).
- Value Score: Ranked segments by profitability and risk (Value_Score = 0.4*Income + 0.4*Approval_Rate + 0.2*Low_EMI_Burden).

### Key Results

1	High-Income Elite	$50,223	$383k	71.4%	Premium loans, wealth management
3	Affluent Professionals	$13,824	$249k	66.7%	Business loans, real estate focus
0	Urban Moderate-Income	$6,286	$117k	74.4%	Starter loans, digital engagement
4	High-Risk Borrowers	$5,482	$133k	50.0%	Debt counseling, strict eligibility

#### Marketing Strategies
- High-Value Segments (1, 3): Targeted upsell (e.g., jumbo mortgages, investment services).
- Moderate Segments (0, 2): Financial education and growth-focused products.
- High-Risk (4): Restructure debt or decline with guidance.

### Conclusion

This segmentation empowers lenders to make data-driven decisions, balancing risk and opportunity while enhancing customer satisfaction. By tailoring strategies to each segment, financial institutions can boost approvals, reduce defaults, and drive growth.

### Source

[Loan Application Data from Kaggle](https://www.kaggle.com/datasets/vipin20/loan-application-data)

