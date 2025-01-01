# Loan Default Prediction

## **Problem Definition**

### **The Context:**

 - A major proportion of retail bank profit comes from interests in the form of home loans. These loans
 are borrowed by regular income/high-earning customers. Banks are most fearful of defaulters, as
 bad loans (NPA) usually eat up a major chunk of their profits. Therefore, it is important for banks to
 be judicious while approving loans for their customer base.
 The approval process for the loans is multifaceted. Through this process, the bank tries to check the
 creditworthiness of the applicant on the basis of a manual study of various aspects of the
 application. The entire process is not only effort-intensive but also prone to wrong
 judgment/approval owing to human error and biases. There have been attempts by many banks to automate this process by using heuristics. But with the
 advent of hm_df science and machine learning, the focus has shifted to building machines that can
 learn this approval process and make it free of biases and more efficient. At the same time, one
 important thing to keep in mind is to make sure that the machine does not learn the biases that
 previously crept in because of the human approval process.

### **The objective:**

 - A bank's consumer credit department aims to simplify the decision-making process for home equity
 lines of credit to be accepted. To do this, they will adopt the Equal Credit Opportunity Act's
 guidelines to establish an empirically derived and statistically sound model for credit scoring. The
 model will be based on the hm_df obtained via the existing loan underwriting process from recent
 applicants who have been given credit. The model will be built from predictive modeling techniques,
 but the model created must be interpretable enough to provide a justification for any adverse
 behavior (rejections).

### **The key questions:**

- **What is the likelihood that an applicant will default on their loan?**
  - Predicting the probability of default based on applicant hm_df.

- **Which features are most important in determining an applicant's creditworthiness?**
  - Identifying key factors like income, credit score, and loan amount.

- **How can we ensure that the model’s predictions are free from biases?**
  - Implementing techniques to detect and mitigate biases in historical hm_df.

- **Can the model provide interpretable reasons for each loan approval or rejection?**
  - Ensuring transparency and explainability of model decisions.

- **How can the model's performance be continuously monitored and improved over time?**
  - Establishing a framework for ongoing validation and refinement. 

### **The problem formulation**:

- Develop an interpretable predictive model to evaluate the creditworthiness of applicants for home equity lines of credit. This model should be able to assess the risk of loan default based on a set of features derived from the existing loan underwriting process. It must comply with the Equal Credit Opportunity Act's guidelines to ensure fairness and avoid biases, and it should provide clear justifications for any adverse decisions (i.e., loan rejections).

## **Data Description:**
The Home Equity dataset (HMEQ) contains baseline and loan performance information for 5,960 recent home equity loans. The target (BAD) is a binary variable that indicates whether an applicant has ultimately defaulted or has been severely delinquent. This adverse outcome occurred in 1,189 cases (20 percent). 12 input variables were registered for each applicant.


* **BAD:** 1 = Client defaulted on loan, 0 = loan repaid

* **LOAN:** Amount of loan approved.

* **MORTDUE:** Amount due on the existing mortgage.

* **VALUE:** Current value of the property. 

* **REASON:** Reason for the loan request. (HomeImp = home improvement, DebtCon= debt consolidation which means taking out a new loan to pay off other liabilities and consumer debts) 

* **JOB:** The type of job that loan applicant has such as manager, self, etc.

* **YOJ:** Years at present job.

* **DEROG:** Number of major derogatory reports (which indicates a serious delinquency or late payments). 

* **DELINQ:** Number of delinquent credit lines (a line of credit becomes delinquent when a borrower does not make the minimum required payments 30 to 60 days past the day on which the payments were due). 

* **CLAGE:** Age of the oldest credit line in months. 

* **NINQ:** Number of recent credit inquiries. 

* **CLNO:** Number of existing credit lines.

* **DEBTINC:** Debt-to-income ratio (all your monthly debt payments divided by your gross monthly income. This number is one way lenders measure your ability to manage the monthly payments to repay the money you plan to borrow.


- Histograms and Boxplots for other variables
![bar_plots](https://github.com/user-attachments/assets/4c393d9d-661f-4008-8139-eb56b2b94d56)

