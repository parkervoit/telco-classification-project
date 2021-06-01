# Telco Classification Project
<hr style="border-top: 10px groove green; margin-top: 1px; margin-bottom: 1px"></hr>

# Project Summary
<hr style="border-top: 10px groove green; margin-top: 1px; margin-bottom: 1px"></hr>

## Project Goals
- Document code, process, findings, and key takeaways in a Jupyter Notebook
- Create python modules to automate the data science pipeline
- Construct an adequate model to predict customer churn using classification tehniques
- Deliver a 5 minute high-level presentation using Jupyter Notebook 
- Be able to answer panel questions about code, process, model, findings, and key takeaways
<hr style="border-top: 10px groove green; margin-top: 1px; margin-bottom: 1px"></hr>

## Business Goals
- Find drivers for churn at Telco
- Construct an ML classification model that accurately predicts customer churn
- Report process and results
<hr style="border-top: 10px groove green; margin-top: 1px; margin-bottom: 1px"></hr>

## Audience
-  The target audience is the Codeup Data Science Team
<hr style="border-top: 10px groove green; margin-top: 1px; margin-bottom: 1px"></hr>

## Deliverables
- A final report notebook 
- A final report notebook presentation
- All necessary modules to reproduce the project
- A .csv file of prediciont probabilities and actual values for species
<hr style="border-top: 10px groove green; margin-top: 1px; margin-bottom: 1px"></hr>

## Project Context
- Data is pulled from the Telco churn database produced by IBM
- More information can be found on the IBM community [website](https://community.ibm.com/community/user/businessanalytics/blogs/steven-macko/2019/07/11/telco-customer-churn-1113).
<hr style="border-top: 10px groove green; margin-top: 1px; margin-bottom: 1px"></hr>

## Data Dictionary 
|Target|Datatype|Definition|
|:-------|:--------|:----------|
| churn | 7043 non-null : object | churn = 1 : have churned, 0 : not churned|

|Feature|Datatype|Definition|
|:-------|:--------|:----------|
|contract_type_id  |  7043 non-null : int64 | contract = 0 : month-to-month, 1 : two year, 2 : one year|
|online_security   |  7043 non-null : object| security = 0 : No, 1 : Yes, 2 : No internet |
|tech_support      |  7043 non-null : object| support = 0 : No, 1 : Yes, 2: No internet | 
|tenure            |  7043 non-null : int64 | tenure is measured in months |
### Hypotheses
> I believe that the type of contract a user has and the amount of services they subscribe to influences whether or not they churn. I also believe that the longer a Telco customer remains loyal the less likely they will churn. 

- **Hypothesis 1 -** Null rejected using chi2 test
- alpha = .05
- $H_0$: User churn is not correlated with the type of contracts they have. 
- $H_a$: User churn is correlated with the type of contract they have. 

- **Hypothesis 2 -** Null rejected using a Mann-Whitney U test
- alpha = .05
- $H_0$: The tenure of churned users is not different than users that do not churn. 
- $H_a$: The tenure of churned users have are different than users that don't churn. 

- **Hypothesis 3 -** Null rejected using chi2 test
- alpha = .05
- $H_0$: User churn is not correlated with whether or not they have online security. 
- $H_a$: User churn is correlated with whether or not they have online security. 

- **Hypothesis 4 -** Null rejected using chi2 test
- alpha = .05
- $H_0$: User churn is not correlated with whether or not they have tech support. 
- $H_a$: User churn is correlated with whether or not they have tech support. 
<hr style="border-top: 10px groove green; margin-top: 1px; margin-bottom: 1px"></hr>

## Project Pipeline
### Plan > Acquire > Prepare > Explore > Model > Deliver
- [x] Create README.md summarizing goals for the project and laying out hypotheses 
- [x] Acquire data from the database with a user-defined function. Save in acquire.py and ensure it works. 
- [x] Clean and prepare data with a user-defined function and save in a module. 
- [x] Define hypotheses and test with statistics. Document and communicate results.
- [x] Create a baseline accuracy and document results.
- [x] Train three different classification models, varying either model type, features, or model parameters.
- [x] Evaluate models on train and validate datasets.
- [x] Choose the model with the highest true positive score and lowest false negative score.
- [x] Create csv file with the user_id, predicted churn, and probability
- [x] Document conclusions, takeaways, and next steps in the Final Report Notebook.
<hr style="border-top: 10px groove green; margin-top: 1px; margin-bottom: 1px"></hr>

## Reproducability
- [x] Read this README.md thouroughly
- [ ] Download modules and env file into your working directory
- [ ] Open and run through the final_report_notebook.ipynb file