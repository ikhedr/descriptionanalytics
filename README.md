# Text Analytics 

This readme shows the output from the code, this a good description
of how to mine text data and extract entities and predict.

This code is just samples of how to mine text analytics.

Output from code 

  Date received           Product     Sub-product  
0    03/12/2014          Mortgage  Other mortgage   
1    10/01/2016  Credit reporting             NaN   
2    10/17/2016     Consumer Loan    Vehicle loan   
3    06/08/2014       Credit card             NaN   
4    09/13/2014   Debt collection     Credit card   

                                      Issue                   Sub-issue  
0  Loan modification,collection,foreclosure                         NaN   
1    Incorrect information on credit report              Account status   
2                Managing the loan or lease                         NaN   
3                                Bankruptcy                         NaN   
4                     Communication tactics  Frequent or repeated calls   

                        Consumer complaint narrative  
0                                                NaN   
1  I have outdated information on my credit repor...   
2  I purchased a new car on XXXX XXXX. The car de...   
3                                                NaN   
4                                                NaN   

                             Company public response  
0                                                NaN   
1  Company has responded to the consumer and the ...   
2                                                NaN   
3                                                NaN   
4                                                NaN   

                                  Company State ZIP code            Tags  
0                    M&T BANK CORPORATION    MI    48382             NaN   
1  TRANSUNION INTERMEDIATE HOLDINGS, INC.    AL    352XX             NaN   
2          CITIZENS FINANCIAL GROUP, INC.    PA    177XX  Older American   
3                AMERICAN EXPRESS COMPANY    ID    83854  Older American   
4                          CITIBANK, N.A.    VA    23233             NaN   

  Consumer consent provided? Submitted via Date sent to company  
0                        NaN      Referral           03/17/2014   
1           Consent provided           Web           10/05/2016   
2           Consent provided           Web           10/20/2016   
3                        NaN           Web           06/10/2014   
4                        NaN           Web           09/13/2014   

  Company response to consumer Timely response? Consumer disputed?  
0      Closed with explanation              Yes                 No   
1      Closed with explanation              Yes                 No   
2      Closed with explanation              Yes                 No   
3      Closed with explanation              Yes                Yes   
4      Closed with explanation              Yes                Yes   

   Complaint ID  
0        759217  
1       2141773  
2       2163100  
3        885638  
4       1027760  

<class 'pandas.core.frame.DataFrame'>
Int64Index: 249978 entries, 1 to 973358
Data columns (total 18 columns):
Date received                   249978 non-null object
Product                         249978 non-null object
Sub-product                     197795 non-null object
Issue                           249978 non-null object
Sub-issue                       155758 non-null object
Consumer complaint narrative    249978 non-null object
Company public response         121395 non-null object
Company                         249978 non-null object
State                           249173 non-null object
ZIP code                        247948 non-null object
Tags                            42573 non-null object
Consumer consent provided?      249978 non-null object
Submitted via                   249978 non-null object
Date sent to company            249978 non-null object
Company response to consumer    249978 non-null object
Timely response?                249978 non-null object
Consumer disputed?              164125 non-null object
Complaint ID                    249978 non-null int64
dtypes: int64(1), object(17)
memory usage: 36.2+ MB
None

Index([u'Product', u'Consumer complaint narrative'], dtype='object')
             Product                       Consumer_complaint_narrative  \
1   Credit reporting  I have outdated information on my credit repor...   
2      Consumer Loan  I purchased a new car on XXXX XXXX. The car de...   
7   Credit reporting  An account on my credit report has a mistaken ...   
12   Debt collection  This company refuses to provide me verificatio...   
16   Debt collection  This complaint is in regards to Square Two Fin...   

    category_id  
1             0  
2             1  
7             0  
12            2  
16            2  

Product                         249978
Consumer_complaint_narrative    249978
category_id                     249978
dtype: int64
Product                         15000
Consumer_complaint_narrative    15000
category_id                     15000
dtype: int64

             Product                       Consumer_complaint_narrative  
1   Credit reporting  I have outdated information on my credit repor...   
2      Consumer Loan  I purchased a new car on XXXX XXXX. The car de...   
7   Credit reporting  An account on my credit report has a mistaken ...   
12   Debt collection  This company refuses to provide me verificatio...   
16   Debt collection  This complaint is in regards to Square Two Fin...   

    category_id  
1             0  
2             1  
7             0  
12            2  
16            2  
(15000, 39107)
#### 'Bank account or service':
  . Most correlated unigrams:
       . deposit
       . overdraft
  . Most correlated bigrams:
       . overdraft fees
       . checking account
#### 'Checking or savings account':
  . Most correlated unigrams:
       . enterprise
       . zone
  . Most correlated bigrams:
       . entire day
       . entire financial
#### 'Consumer Loan':
  . Most correlated unigrams:
       . vehicle
       . car
  . Most correlated bigrams:
       . auto loan
       . car loan
#### 'Credit card':
  . Most correlated unigrams:
       . rewards
       . card
  . Most correlated bigrams:
       . american express
       . credit card
#### 'Credit card or prepaid card':
  . Most correlated unigrams:
       . enterprise
       . zone
  . Most correlated bigrams:
       . entire day
       . entire financial
#### 'Credit reporting':
  . Most correlated unigrams:
       . experian
       . equifax
  . Most correlated bigrams:
       . xxxx equifax
       . credit report
#### 'Credit reporting, credit repair services, or other personal consumer reports':
  . Most correlated unigrams:
       . crippled
       . whilst
  . Most correlated bigrams:
       . company collecting
       . requesting removal
#### 'Debt collection':
  . Most correlated unigrams:
       . collection
       . debt
  . Most correlated bigrams:
       . collect debt
       . collection agency
#### 'Money transfer, virtual currency, or money service':
  . Most correlated unigrams:
       . enterprise
       . zone
  . Most correlated bigrams:
       . entire day
       . entire financial
#### 'Money transfers':
  . Most correlated unigrams:
       . paypal
       . western
  . Most correlated bigrams:
       . money transfer
       . western union
#### 'Mortgage':
  . Most correlated unigrams:
       . modification
       . mortgage
  . Most correlated bigrams:
       . mortgage company
       . loan modification
#### 'Other financial service':
  . Most correlated unigrams:
       . username
       . guard
  . Most correlated bigrams:
       . loan relief
       . check cashing
#### 'Payday loan':
  . Most correlated unigrams:
       . speedy
       . payday
  . Most correlated bigrams:
       . took payday
       . payday loan
#### 'Payday loan, title loan, or personal loan':
  . Most correlated unigrams:
       . enterprise
       . zone
  . Most correlated bigrams:
       . entire day
       . entire financial
#### 'Prepaid card':
  . Most correlated unigrams:
       . prepaid
       . rushcard
  . Most correlated bigrams:
       . prepaid card
       . rush card
#### 'Student loan':
  . Most correlated unigrams:
       . student
       . navient
  . Most correlated bigrams:
       . student loans
       . student loan
#### 'Vehicle loan or lease':
  . Most correlated unigrams:
       . enterprise
       . zone
  . Most correlated bigrams:
       . entire day
       . entire financial
#### 'Virtual currency':
  . Most correlated unigrams:
       . tool
       . trading
  . Most correlated bigrams:
       . requests assistance
       . email requests
       
['Debt collection']

['Credit reporting']

Warning: The least populated class in y has only 2 members, which is too few. The minimum number of groups for any class cannot be less than n_splits=5.
  % (min_groups, self.n_splits)), Warning)
model_name
LinearSVC                 0.840460
LogisticRegression        0.819791
MultinomialNB             0.712534
RandomForestClassifier    0.387135
Name: accuracy, dtype: float64
"I requested a home loan modification through Bank of America. Bank of America never got back to me."
  - Predicted as: 'Mortgage'

"It has been difficult for me to find my past due balance. I missed a regular monthly payment"
  - Predicted as: 'Credit reporting'

"I can't get the money out of the country."
  - Predicted as: 'Bank account or service'

"I have no money to pay my tuition"
  - Predicted as: 'Debt collection'

"Coinbase closed my account for no reason and furthermore refused to give me a reason despite dozens of request"
  - Predicted as: 'Bank account or service'


Process finished with exit code 0