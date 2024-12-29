How can we detect fraudulent activities from our customers while still making our services satisfactory and increasing customer traffic?
=> can we classify customers [by … ], who are likely to engage in fraudulent activities or not?
=> consequence of false-positives: losing money, because you might send someone to double check, reduced customer satisfaction (fine)
=> consequences of false-negatives: losing money., because client steals money
Models:
What we want to predict:
0 = the client is not engaging in any fraudulent activity
1=  the client is engaging in fraudulent activity
Assumptions:
If a client is located in the region 101, 103, 104, 107 or 311, and has a monthly electricity consumption > 100, the client is more likely to act fraudulent. [Baseline model]
If there is a monthly spread in the total electricity consumption between 200 and 1000, the client is more likely to act fraudulent => if you have relatively stable electricity consumption (0-100 spread), you are less likely to cheat.
Also: the lower the max electricity consumption per month, the lower the probability to cheat.
Evaluation metric: Recall, because we have highly imbalance data (total_N =, fraud_N =  (%), non-fraud_N =  (%)); we want to reduce the false-negatives



Project: Fraud Detection Challenge in Electricity and Gas Consumption

Value of Product:

There are clients that are cheating in the measurement of their electricity or gas consumption in Tunisia. 
This creates financial loses for the electricity company and it is necessary to detect such cases as soon as possible without reducing customer satisfaction or expending too many resources.
The product will provide a solution to this problem by increasing the probability of detection of the fraudulent clients based on their data.

Prediction:

0 = the client is not engaging in any fraudulent activity
1=  the client is engaging in fraudulent activity

Evaluation Metric:

It is important to detect clients that are fraudulent as fraudulent therefore reduce the number of false negatives (fraudulent clients that are detected as non-fraudulent).
This is important for the business case as fraudulent clients create negative impact in the finances of the company.
Therefore, recall is the best metric that captures this behavior and it is also understandable in business cirlces.
In more technical analysis the AUC and ROC curve will give a better representation of the general model performance. 

Baseline Model:

If a client is located in the region 101, 103, 104, 107 or 311, and has a monthly electricity consumption > 100, the client is more likely to act fraudulent. [Baseline model]
Based on that we can estimate : total_clients = 135493, fraudulent_clients = 7566, non-fraudulent_clients = 127927.
With these numbers and the fraud information from the dataset, we can calculate the confusion matrix.

Score:

Recall : 0.58
AUC Score:  0.55