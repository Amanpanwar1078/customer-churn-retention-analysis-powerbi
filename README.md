# customer-churn-retention-analysis-powerbi
🔍 Project Overview

This project analyzes telecom customer churn patterns to identify high-risk segments and quantify the financial impact of customer attrition.

The objective was to move beyond simple churn percentage reporting and build a structured analytical dashboard that enables business stakeholders to prioritize retention strategies based on risk and revenue exposure.

🎯 Business Objective

Identify key drivers of churn

Segment customers by contract type, tenure, and service usage

Quantify lost monthly revenue due to churn

Detect high-risk service combinations

Provide actionable retention recommendations

🛠 Tools & Technologies

Power BI

Power Query (ETL)

DAX

Star Schema Data Modeling

Conditional Formatting for Risk Classification

🔄 Data Preparation (Power Query)

The raw CSV dataset was transformed using Power Query:

Corrected data types (MonthlyCharges → Decimal, handled TotalCharges conversion)

Validated customerID as unique primary key

Created tenure bins (0–12, 12–24, 24–48, 48+ months)

Structured model into:

Fact_Churn (transactional data)

Dim_Services (service attributes)

Cleaned null/duplicate records to ensure data integrity

📐 Data Modeling

Implemented a star schema design to improve analytical clarity and performance:

Fact table containing customer-level churn metrics

Dimension table separating service attributes

Proper relationships configured for filter propagation

📊 Key DAX Measures
Total Customers

Baseline count of active customer base.

Churn Rate %

Calculated using CALCULATE and DIVIDE to dynamically compute churn percentage under different filter contexts.

Lost Monthly Revenue

Aggregated revenue from churned customers to measure financial impact.

Average Tenure

Evaluated customer lifespan trends.

📈 Key Insights

Month-to-month contracts show the highest churn rate (~42%)

Customers with tenure below 12 months exhibit elevated churn risk

Fiber optic customers without security/add-on services show churn rates above 60%

Electronic check payment method correlates with higher churn

Top 3 service combinations contribute ₹87K+ in potential monthly revenue loss

💡 Business Recommendations

Incentivize migration from month-to-month to long-term contracts

Strengthen onboarding and engagement for early-tenure customers

Bundle fiber optic services with protective add-ons

Promote auto-pay payment methods to reduce churn correlation

📊 Dashboard Features

Executive KPI summary

Risk-segmented churn visualization

Conditional formatting (High / Medium / Low risk)

Service combination deep-dive page

Revenue impact quantification

📌 Outcome

Developed a business-ready churn analytics dashboard that enables decision-makers to:

Identify priority retention segments

Quantify revenue risk

Formulate data-driven retention strategies
