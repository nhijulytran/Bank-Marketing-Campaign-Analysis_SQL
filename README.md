# Bank Marketing Campaign Analysis (SQL)
# I. Project Information
## 1. Overview
- This project explores a ***Bank Marketing Dataset*** to uncover insights into customer behavior and marketing campaign performance.
- The goal is to identify what factors influence a customer’s decision to open a deposit account — using SQL for analysis in Google BigQuery.

## 2. Dataset
- Dataset Source: [*Bank Marketing Dataset*](https://www.kaggle.com/datasets/janiobachmann/bank-marketing-dataset/data)
- Reference Source: [*Business Case + EDA*](https://www.kaggle.com/code/mlippo/py-business-case-eda/notebook)
- Rows: 11,162 | Columns: 17
- Data Dictionary:
This section describes all variables included in the dataset, along with their data types and meanings.

| Variable Name | Type      | Description                                                               |
| ------------- | --------- | ------------------------------------------------------------------------- |
| **age**       | `INTEGER` | Client's age                                                              |
| **job**       | `STRING`  | Type of job the client has                                                |
| **marital**   | `STRING`  | Marital status                                                            |
| **education** | `STRING`  | Client's education level                                                  |
| **default**   | `BOOLEAN` | Whether the client has credit in default                                  |
| **balance**   | `INTEGER` | Average yearly account balance                                            |
| **housing**   | `BOOLEAN` | Whether the client has a housing loan                                     |
| **loan**      | `BOOLEAN` | Whether the client has a personal loan                                    |
| **contact**   | `STRING`  | Communication type used to contact the client                             |
| **duration**  | `INTEGER` | Duration of the last contact (in seconds)                                 |
| **campaign**  | `INTEGER` | Number of contacts performed during this campaign                         |
| **pdays**     | `INTEGER` | Number of days since the client was last contacted in a previous campaign |
| **previous**  | `INTEGER` | Number of contacts performed before this campaign                         |
| **poutcome**  | `STRING`  | Outcome of the previous marketing campaign                                |
| **deposit**   | `BOOLEAN` | Indicates whether the client subscribed to a term deposit                 |

# II. Data Analysis
## 1. Data Cleaning
During this stage, I performed several SQL cleaning steps to ensure data quality and consistency.

Query results:


Query results:

## 2. Exploratory Data Analysis (EDA)
In this project, I will write 08 queries in BigQuery based on the Kaggle dataset.
- Query 01: Calculate total of customers, average balance, default rate and deposit rate
  SQL code

- Query 02: Calculate average balance on each deposit status

- Query 03: Divide balance into 6 groups and calculate total customers, total customers of having deposit and percentage of total customers of having deposit on total customers of dataset

- Query 04: Calculate average balance based on every job titles, following by total customers having loan and housing debts


- Query 05: Calculate total customers of having deposit and percentage of total customers of having deposit on total customers of dataset based on job titles


- Query 06: Divide age into 3 groups and calculate total customers, total customers of having deposit and percentage of total customers of having deposit on total customers of dataset

- Query 07: Calculate total customers, total customer having deposit and proportion of them on each marital status

- Query 08: Calculate success calling rate by month
# III. Business Insights
- Retired, self_employed customers have the highest average balance (≈2417, ≈1865 respectively) but a moderate deposit rate (4.62%, 1.68% respectively).
- Although students have the smallest customer count, their deposit rate (2.41%) relative to base size is promising — when combined with the Under 30 age group, which has the highest deposit rate (59.83%), it shows strong potential for future long-term customers.
- The largest customer segment falls within the 0–20K balance range, accounting for over 80% of total customers (9,643 out of 11,162).
- The 30–50 age group forms the majority (7140 customers) but has the lowest deposit rate (42.69%) => This indicates a key segment that should be re-targeted with tailored offers or incentives.
- Blue-collar, technician, and admin roles show high housing loan counts, yet lower average balances, implying a strong loan dependency — these customers may prioritize debt repayment over deposits.

# IV. Recommendations
- Target Retired and Over-50 Customers for Premium Deposits
  - Develop specialized “Retirement Savings” or “Wealth Stability” deposit products, leveraging their high balances and financial maturity.
  - Use personalized advisory services to convert savings into deposits.
- Engage the 30–50 Segment with Mid-term Incentives
  - Offer flexible-term deposits or interest bonuses tied to account tenure to re-engage this large but passive group.
  - Use cross-selling (insurance, investment funds) to strengthen their long-term commitment.
- Educate and Nurture Blue-Collar and Technician Segments
  - Launch financial literacy campaigns to increase awareness of deposit benefits.
  - Introduce micro-deposit options or salary-linked savings programs with automatic transfers.
- Capture Young Customer Loyalty Early
  - Design student and young professional deposit accounts with low barriers, gamified savings, and mobile-first onboarding.
  - Encourage early deposit behavior to build long-term brand loyalty.


