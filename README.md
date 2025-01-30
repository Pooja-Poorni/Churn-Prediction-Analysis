# Credit Card Churn Prediction Analysis

![image](https://github.com/user-attachments/assets/278f198d-d5bf-4348-93db-0fcb645d2ba7)



# 1. Description
This is an end-to-end machine learning project that utilizes LightGBM to predict customer's probability of churning in a bank's credit card service. It involves supervised learning (using a labeled training set) for classification, where the target is 1 if the customer attrited, else 0.
I implemented this project following some CI/CD principles and using modular coding. First, I developed my entire analysis (from EDA to modeling) in notebooks. Then, I divided the project development into components responsible for data ingestion, transformation, and model training, following the same steps as in the notebooks. Once I had done this, I created scripts for automating the training and prediction pipelines using these components. The training pipeline executes them and obtains all the machine learning model artifacts, while the prediction pipeline makes predictions by consuming the obtained artifacts. All of this was made with good practices like virtual environment use (isolating dependencies), exception handling, loggings, documentation (every script/function/class purposes and definitions are defined inside the files), etc. Afterward, I built a web app API in Flask, integrating everything mentioned above. My objective with this was to get closer to a real data science project workflow by packaging my entire project as a package.
# 2. Technologies and tools
The technologies and tools used were Python (Pandas, Numpy, Matplotlib, Seaborn, Scikit-Learn, optuna, LightGBM, Shap, Flask), Jupyter Notebook, Git and Github (version control), machine learning classification algorithms, statistics, Anaconda (terminal) and Visual Studio Code (project development environment).

# 3. Business problem and project objective

**3.1 What is the business problem?**

A manager at the bank is disturbed with more and more customers leaving their credit card services. They would really appreciate if one could predict for them how likely is a customer to churn so they can proactively go to the customers to provide them better services and turn their decisions in the opposite direction.

**3.2 What is the context?**

When a bank acquires a customer for its credit card service, three essential Key Performance Indicators (KPIs) to consider include:
Customer Acquisition Cost (CAC): This measures the expenses associated with acquiring each credit card customer, encompassing marketing, sales, and related costs. Lower CAC reflects efficient customer acquisition.
Customer Lifetime Value (CLV): CLV estimates the total revenue the bank can expect to generate from a credit card customer over their relationship. A higher CLV indicates that the customer's value surpasses the acquisition cost, ensuring long-term profitability.
Churn Rate: Churn rate is typically expressed as a percentage and represents the number of credit card customers who have left during a specific period divided by the total number of customers at the beginning of that period.
These KPIs help the bank assess the effectiveness of its strategies in acquiring credit card customers and gauge the potential long-term financial benefit of these acquisitions.
In order to maximize profitability, the bank aims to minimize CAC and Churn while maximizing CLV.

**3.3 Which are the project objectives?**

Identify the factors associated with customer churn.
Construct a model capable of accurately predicting the probability of a customer to churn.
Offer action plans for the bank to reduce credit card customer churn.

**3.4 Which are the project benefits?**

Cost Savings.
Improved Customer Retention.
Enhanced Customer Experience.
Targeted Marketing.
Revenue Protection.
And as a result, the mentioned business problem will be resolved.

**3.5 Conclusion**

When deploying the model so that the bank can make predictions, the primary objective is to generate probability scores for each customer. This is typically more valuable for businesses when compared to making binary predictions (1/0), as it enables better decision-making and more effective customer retention strategies.
For instance, predicting the probability of churn provides more actionable insights. Instead of simply determining whether a customer will churn or not, you gain an understanding of how likely it is to happen. This information enables the bank to allocate its efforts and resources more effectively. For example, it can concentrate its retention efforts on customers with a high probability of churning.

# 4. Solution pipeline
The following pipeline was used, based on CRISP-DM framework:

Define the business problem.
Collect the data and get a general overview of it.
Split the data into train and test sets.
Explore the data (exploratory data analysis)
Feature engineering, data cleaning and preprocessing.
Model training, comparison, feature selection and tuning.
Final prediction model testing and evaluation.
Conclude and interpret the model results.
And then Deployed.
