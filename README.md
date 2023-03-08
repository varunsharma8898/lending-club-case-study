# Lending Club Case Study
> This case study is aimed at solving real business problems using EDA. The aim is to develop a basic understanding of risk analytics in banking and financial services and to understand how data is used to minimise the risk of losing money while lending to customers.


## Table of Contents
* [General Info](#general-information)
* [Technologies Used](#technologies-used)
* [Conclusions](#conclusions)


## General Information

### Business Understanding

You work for a consumer finance company which specialises in lending various types of loans to urban customers. When the company receives a loan application, the company has to make a decision for loan approval based on the applicant’s profile. Two types of risks are associated with the bank’s decision:
- If the applicant is likely to repay the loan, then not approving the loan results in a loss of business to the company
- If the applicant is not likely to repay the loan, i.e. he/she is likely to default, then approving the loan may lead to a financial loss for the company

The data given below contains information about past loan applicants and whether they ‘defaulted’ or not. The aim is to identify patterns which indicate if a person is likely to default, which may be used for taking actions such as denying the loan, reducing the amount of loan, lending (to risky applicants) at a higher interest rate, etc.

In this case study, you will use EDA to understand how consumer attributes and loan attributes influence the tendency of default.

When a person applies for a loan, there are two types of decisions that could be taken by the company:
- Loan accepted: If the company approves the loan, there are 3 possible scenarios described below:
  - Fully paid: Applicant has fully paid the loan (the principal and the interest rate)
  - Current: Applicant is in the process of paying the instalments, i.e. the tenure of the loan is not yet completed. These candidates are not labelled as 'defaulted'.
  - Charged-off: Applicant has not paid the instalments in due time for a long period of time, i.e. he/she has defaulted on the loan
- Loan rejected: The company had rejected the loan (because the candidate does not meet their requirements etc.). Since the loan was rejected, there is no transactional history of those applicants with the company and so this data is not available with the company (and thus in this dataset)

### Business Objectives

This company is the largest online loan marketplace, facilitating personal loans, business loans, and financing of medical procedures. Borrowers can easily access lower interest rate loans through a fast online interface.

Like most other lending companies, lending loans to ‘risky’ applicants is the largest source of financial loss (called credit loss). Credit loss is the amount of money lost by the lender when the borrower refuses to pay or runs away with the money owed. In other words, borrowers who default cause the largest amount of loss to the lenders. In this case, the customers labelled as 'charged-off' are the 'defaulters'.

If one is able to identify these risky loan applicants, then such loans can be reduced thereby cutting down the amount of credit loss. Identification of such applicants using EDA is the aim of this case study.

In other words, the company wants to understand the driving factors (or driver variables) behind loan default, i.e. the variables which are strong indicators of default. The company can utilise this knowledge for its portfolio and risk assessment.

To develop your understanding of the domain, you are advised to independently research a little about risk analytics (understanding the types of variables and their significance should be enough).

### Data set
A loan.csv was provided that had the complete loan data for all loans issued through the time period 2007 to 2011.

A data dictionary was also provided as Data_Dictionary.xlsx that described the meaning of the variables in loan.csv dataset.


## Conclusions
As per the analysis done for this case study, there are 5 variables that define defaulter behaviour.
1. dti:
   - The average dti for defaulters is higher than non-defaulters across all purposes, except wedding and medical and across all home ownership types.
   - If the dti of an applicant is greater than the average dti for non-defaulters for a certain category, the applicant is more likely to default on the loan.
   - Similarly, if the dti of an applicant is greater than average dti for a non-defaulter for any type of home ownership, the applicant is more likely to default on the loan.

2. Loan Amount:
   - Across all purposes (except house, moving and renewable_enery), the average loan amount is larger for defaulters compared to non-defaulters.
   - If the loan amount of an applicant is larger than average loan amount of non-defaulters for most of the purposes, the applicant is more likely to default on the loan.

3. Annual Income:
   - The average annual income of defaulters is lower than that of non-defaulters across different grades.
   - People with annual income lower than the average annual income of non-defaulters are more likely to default.

4. Grade:
   - With poorer grades, interest rates increase. With increase in interest rates, the number of defaulters also increase.
   - People with poorer grades are more likely to default.

5. Interest Rate:
   - With increase in interest rates, the number of defaulters also increase.
   - People with higher interest rates are more likely to default compared to those with lower interest rates.


## Technologies Used
- pandas - version 1.4.4
- numpy - version 1.21.5
- seaborn - version 0.11.2
- matplotlib - version 3.5.2


## Contact
Created by [@varunsharma8898] - feel free to contact me!
