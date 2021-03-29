# DSC680_Loan_Approval

Motivaction:

The motivation behind this project is firstly it is a school assignment.  Then in terms if this was a real world project: 
	Financial institutions spend and loose money every year on the cultivation and approval/ denial of loan application.  The idea is that if machine learning could be used to either 1) approve the loan altogether before sending to underwriting for final sign off or 2) give a solid pre-approval so that sales staff time can be better utilized in making sure the pre-approved loans make it through underwriting and to closure instead of just trying to cultivate loan applications. 

Build Status:

This project is currently in the development phase. 

Code Syle: 
This is being written in Python 3 and will try and follow proper Pythonic coding principles and standards.  

This project was built using Jupyter Notebooks in an Anaconda environment. 

Sample Code: **************************************************

# function to change categorical variables in the train set 
def to_binary(x, pos_cat):
    if type(x)== float and np.isnan(x):
        return x
    if x == pos_cat:
        return 1
    return 0 
pos_class =[('Gender','Male'),('Married','Yes'),("Education",'Graduate'),('Self_Employed','Yes'),('Property_Area','Urban'),('Loan_Status','Y')]
# conver all categ. to binary 
for col, cat in pos_class:
    train[col]=train[col].apply(to_binary, pos_cat=cat)
train.Dependents=train.Dependents.replace('3+', '3').astype(float)

************************************************************** 
FEATRUES:
It is the hope that this project will have real world application in improving the effectiveness of the approval/pre-approval process for financial institutions to aid in revenue growth.  Some of the things that will set this apart from other similar projects is the following: 
1) the use of pipe-lines for processing and assembling the algorithms. 
2) When all models have been built and taught the using grid search the best models will be kept 
3) Those model will then be put together using an ensemble technique like Soft Vote


