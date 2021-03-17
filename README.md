### Written Report of Findings
# Overview of analysis
The goal of my analysis was to develop a machine learning model capable of determining the credit risk of potential borrowers with sufficient specificity and precision to be used in practice.

# Results
* LogReg with RandomOverSampling
 * BAS: 0.645
 * REC: 0.70
 * PRE: 0.01
* LogReg with SMOTE
 * BAS: 0.626
 * REC: 0.59
 * PRE: 0.01
* LogReg with ClusterCentroids
 * BAS: 0.547
 * REC: 0.65
 * PRE: 0.01
* LogReg with SMOTEENN
 * BAS: 0.606
 * REC: 0.62
 * PRE: 0.01
* BalancedRandomForest
 * BAS: 0.666
 * REC: 0.45
 * PRE: 0.02
* EasyEnsembleClassifier
 * BAS: 0.745
 * REC: 0.66
 * PRE: 0.02
 

# Summary
The models tested generally yeilded unsatisfactory precision but reasonable sensitivity when identifying high risk individuals; if the general population of applicants is balanced similarly to the data used in this study, then these models would deny loans to many who may be low risk but would rarely offer a loan to someone who is high risk. I recommend the EasyEnsembleClassifier for further analysis - right now the precision of the high risk class is 2%, meaning 98% of those labeled high_risk would actually be false positives. That said, 66% of all high risk applicants are correctly identified, and with a balanced accuracy score of 0.745 it's off to a great start compared to the other models. There are ample opportunities with pre-processing to tighten the screws and get better results with more time. 