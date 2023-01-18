# User-level analysis for eCommerce Business

### Skills
- SQL
- Data Wrangling
- Data Analysis
- AB Testing

Description
---
AB Testing is an application of Hypothesis Testing aimed at improving business metrics like revenue, including other explanatory metrics. It is an important final step in the algorithm development process, where verification is performed on whether a new iteration is an improvement on the existing version. 

The project is an excerpt from Coursera's ***Data Wrangling, Analysis and AB Testing*** applied for user-level analysis. The [Mode Analytics](https://mode.com/) platform is used to extract data from their public warehouse and perform analysis. The database corresponds to a hypothetical eCommerce platform, wherein an AB test is performed on two groups: 

- **Eligibility**
    - users who created an account with a valid email address
- **Control Group**
    - users receive a regular welcome email upon account creation
- **Treatment Group**
    - users who receive an updated welcome email with links and images to top-selling items
- **Divergence Point**
    - timestamp when the automated welcome email is scheduled to be sent

The results of four such concurrent tests are analysed based on metrics tied to business value aimed at measuring a change in user experience:

Engagement Metrics:
- **Orders after assignment (binary)**
    - assumes value 1 if an order is placed after assignment, else 0
- **Order Count after assignment**
    - total orders placed after assignment
- **Item Count after assignment**
    - number of items within an order after assignment
- **Item Count after assignment**
    - number of items within an order after assignment
- **Webpage views after assignment**
    - number of webpage views after assignment

Business Metric:
- **Revenue**
    - total revenue generated after assignment
    
Tables used
---
- Events
- Orders

Summary
---
Tables extracted are pivoted to obtain relevant columns and checks for missing data are performed. A usable table is designed for AB testing to determine if each test yielded statistically significant improvement in the number of orders and webpage views after assignment.  

The results are
- a **2.77%** improvement in **ORDERS** for treatment group from baseline (control group) with a 93.3% confidence level for test_id 5
- a **1.40%** improvement in **WEBPAGE VIEWS** for treatment group from baseline (control group) with over 95% significance for test_id 5


