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

- Algorithms used:
  - Random Forest
  - Decision Tree
  - Logistic Regression 

- Histograms and Boxplots for the variables

![plots1](https://github.com/user-attachments/assets/ade4a2fb-aa37-463d-b81c-061069dff0d4)


- Bar Plots

![plots2](https://github.com/user-attachments/assets/374bfb11-c976-42d2-af7c-6ea0432f5eb2)


- Box Plot

![plots3](https://github.com/user-attachments/assets/d60fa3ab-d6fd-4921-b89a-b6e4b36e2ec5)


- Scatter Plots

![plots4](https://github.com/user-attachments/assets/9692c278-fc75-4021-9dd8-91773fea5b05)


- Stacked Bar Plots

![plot5](https://github.com/user-attachments/assets/dd2ed133-2cba-42ca-9f3a-d4ab9a8564ff)


- Correlation Heat Map

![plot6](https://github.com/user-attachments/assets/b50b8f6d-ebda-4d80-9e3f-540f26a9cfec)


- Pair Plot

![plot7](https://github.com/user-attachments/assets/bec8d20d-2b60-4aab-b734-2a54db370cf8)

- Decision Tree Plot

![plot8](https://github.com/user-attachments/assets/cbfe151e-cff6-4df5-9d51-8a04171b601e)

- Random Forest Feature Importances

![plot9](https://github.com/user-attachments/assets/98c7b38c-ddd4-4ee9-bf37-a1f24c9b2e41)

- Model Comparison

![image](https://github.com/user-attachments/assets/9a6c53df-e95d-4e6b-9934-5e9d9f9a7e06)

**Insights**

**1. Comparison of various techniques and their relative performance based on chosen Metric (Measure of success):**

- **Logistic Regression**:
  - **Train Accuracy**: 0.81
  - **Test Accuracy**: 0.78
  - **Train Recall**: 0.03
  - **Test Recall**: 0.04
  - **Train Precision**: 0.57
  - **Test Precision**: 0.71

- **Decision Tree**:
  - **Train Accuracy**: 1.00
  - **Test Accuracy**: 0.88
  - **Train Recall**: 1.00
  - **Test Recall**: 0.67
  - **Train Precision**: 1.00
  - **Test Precision**: 0.74

- **Random Forest**:
  - **Train Accuracy**: 1.00
  - **Test Accuracy**: 0.90
  - **Train Recall**: 1.00
  - **Test Recall**: 0.69
  - **Train Precision**: 1.00
  - **Test Precision**: 0.85

**Performance Analysis**:
- The **Random Forest** model is performing relatively better than the other models with a test accuracy of 0.90, which is higher than Logistic Regression and Decision Tree.
- **Logistic Regression** shows a lower test accuracy and recall compared to the other models, indicating it might not be the best choice for this problem.
- Both **Decision Tree** and **Random Forest** show perfect accuracy, recall, and precision on the training data, indicating they might be overfitting the training data. However, the Random Forest model generalizes better on the test data with higher test accuracy, recall, and precision compared to the Decision Tree.

**Scope for Improvement**:
- There is still scope to improve the recall and precision for the minority class (Class 1). Techniques like **hyperparameter tuning**, **ensemble methods** (like boosting), and **feature engineering** could be explored further.
- **Cross-validation** and **regularization** techniques can be applied to avoid overfitting.

**2. Refined insights:**

- The Random Forest model provides a good balance between recall and precision for both classes, making it suitable for the problem at hand.
- The high training performance of the Decision Tree suggests it might be capturing noise in the training data, leading to overfitting.
- Logistic Regression, while simpler, may not be capturing the complexity of the data, resulting in lower performance metrics.

**3. Proposal for the final solution design:**

**Proposed Model**: **Random Forest**

**Reasons**:
- **Balanced Performance**: The Random Forest model offers a good balance between accuracy, recall, and precision, making it robust for predicting both classes.
- **Better Generalization**: It shows better generalization on test data compared to the Decision Tree, indicating its ability to handle unseen data effectively.
- **Feature Importance**: Random Forest also provides insights into feature importance, which can be useful for understanding the data and making informed decisions.
- **Ensemble Nature**: Being an ensemble method, it reduces the risk of overfitting compared to a single Decision Tree.

In conclusion, the Random Forest model is recommended due to its superior generalization performance, balanced metrics, and ability to handle complex datasets effectively. Further tuning and feature engineering can enhance its performance even more.
