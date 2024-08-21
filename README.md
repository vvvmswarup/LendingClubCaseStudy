# Lending Club Case Study
case study and analysis on a data set of loans of a biggest customer

## Table of Contents
* [General Info](#general-information)
* [Technologies Used](#technologies-used)
* [Conclusions](#conclusions)
* [Acknowledgements](#acknowledgements)


## General Information
- This company is the largest online loan marketplace, facilitating personal loans, business loans, and financing of medical procedures.
- Borrowers can easily access lower interest rate loans through a fast online interface.
- the company wants to understand the driving factors (or driver variables) behind loan default, i.e. the variables which are strong indicators of default.  The company can utilise this knowledge for its portfolio and risk assessment.


## Technologies Used
- Python
- pandas
- matplotlib
- seaborn

## Conclusions
### Univariate Analysis
- Most loans are within the $5,000 to $15,000 range, with fewer high-value loans.
- Interest rates are generally between 10% and 15%, with a peak around 13%. Higher interest rates may indicate higher-risk borrowers.
- The majority of loans are either fully paid or current, with a smaller but significant number of charged-off (defaulted) loans.
- These distributions provide a solid foundation for understanding the dataset before diving deeper into more complex relationships.

### Bivariate Analysis
- Loan Amount vs Loan Status: Higher loan amounts tend to have a higher risk of being charged off (defaulted).
- Interest Rate vs Loan Status: Charged-off loans generally have higher interest rates, indicating that higher-risk borrowers are charged more.
- Annual Income vs Loan Status: There is a wide range of incomes across all loan statuses, but defaults do not show a clear pattern with income.
- These insights suggest that loan amount and interest rate are important factors in determining loan outcomes.

### Derived Metrics
- We derived the following metrics to gain deeper insights:
- Debt-to-Income Ratio (DTI): Represents the proportion of annual income that goes towards debt payments.
- Credit Utilization Ratio: Indicates the proportion of the revolving credit that is being used by the borrower.
- Loan-to-Income Ratio: Compares the loan amount to the borrower's annual income.
- These metrics provide a more comprehensive view of the borrower's financial health and potential risk.

### Univariate Analysis of Derived Metrics
- DTI: The Debt-to-Income Ratio is skewed, with most borrowers having a lower DTI, indicating they are not over-leveraged.- Credit Utilization Ratio**: The Credit Utilization Ratio varies widely, suggesting different levels of credit use among borrowers.
- Loan-to-Income Ratio: This ratio is mostly low, but some borrowers have taken loans that are significant relative to their income.
- Understanding these distributions helps in assessing the financial stability of the borrowers.

### Bivariate Analysis of Derived Metrics
- DTI vs Loan Status: Borrowers with higher Debt-to-Income Ratios are more likely to default, as indicated by the charged-off loans.
- Credit Utilization vs Loan Status: Higher credit utilization correlates with an increased likelihood of default, suggesting that over-leveraged borrowers are at higher risk.
- Loan-to-Income Ratio vs Loan Status: Loans that represent a significant portion of the borrower's income are more likely to be charged off, indicating that such borrowers might struggle with repayments.
- These derived metrics provide critical insights into the financial behaviors that may contribute to loan defaults.

### Segmented Analysis of Derived Metrics
- DTI by Grade: Higher loan grades (A, B) generally have lower Debt-to-Income Ratios, indicating that higher-grade borrowers are less over-leveraged.
- Loan-to-Income Ratio by Sub-Grade: Within each grade, sub-grades with lower risk (e.g., A1, B1) tend to have lower loan-to-income ratios, indicating more conservative borrowing.
- Credit Utilization by Grade: Higher-grade borrowers tend to have lower credit utilization ratios, suggesting better credit management.
- Segmenting by grade and sub-grade reveals that borrowers with better credit profiles (higher grades) tend to manage their finances more conservatively, which correlates with lower default rates.

## Final Conclusions
- 1. **Loan Amount and Interest Rate**: Higher loan amounts and interest rates are associated with an increased risk of loan defaults. These factors should be carefully considered when approving loans.
- 2. **Derived Metrics**: Metrics like Debt-to-Income Ratio, Credit Utilization Ratio, and Loan-to-Income Ratio provide deeper insights into the financial health of borrowers. High values in these metrics are strong indicators of potential default risk.
- 3. **Segmented Analysis**: Borrowers with higher credit grades (A, B) generally manage their debts better, with lower DTI, credit utilization, and loan-to-income ratios. These segments are less likely to default compared to lower-grade borrowers.
- 4. **Risk Management**: The company should use these insights to refine its lending criteria, focusing on borrowers with lower derived metric values and higher grades to minimize default risks.
