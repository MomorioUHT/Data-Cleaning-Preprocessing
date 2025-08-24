# Data-Cleaning-Preprocessing
* Example Data: ```loan.csv```

### Features

* Loan_ID: Loan reference number
* Gender: Applicant gender
* Married: Applicant marital status
* Dependents: Number of family members
* Education: Applicant education/qualification
* Self_Employed: Applicant employment status
* ApplicantIncome: Applicant's monthly salary/income
* CoapplicantIncome: Additional applicant's monthly
* LoanAmount: Loan amount
* Loan_Amount_Term: The loan's repayment period (in days)
* Credit_History: Records of previous credit history
* Property_Area: The location of property
* Loan_Status: Status of loan

### Data Cleaning Technique used
* Filling NaN values
    * continuous features: using mean method
    * categorial features: using mode method
* Dealing with outliers
    * using interquartile range to cap out maximum values