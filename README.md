# Jobathon-Nov-2021-AV
Solution Approach 
Feature Engineering Approach
Model Selected
Model Building


Steps Followed

1. Isolated the EMP IDs that were common to both the train and test sets for later use
2. Identified the EMP IDs that had a last working date and set them as employees who are leaving the organisation
3. Converted the Total Business Value and the Quarterly Rating to average values per EMPID in order to bring them at a EMP ID level
4. Created a new feature called designation change to check if the employee designation had improved over their tenure
5. Label and hot encoded the Gender,City,Education Level values 
6. Scaled Numerical features like salary,Avg Business Value
7. Avg Quarterly rating was maintained as a weighted variable and not hot encoded
8. Performed Age bucketing into Young, Middle Aged and Older but missed to include in the feature set
9. Since the final processed data was so severely imbalanced with higher resignations and lower retention , went for anomaly detection algorithms like OneClassSVM,
IsolationForest and Local Outlier Factor of which the SVM produced the best F1 score on the training and validation set. All other techniques like ensemble algorithms and oversampling were not useful
10. Split the training only data after removing the test EMP IDs into train and validation 80:20
11. Selected ONECLASSSVM based on F1 score of the validation set.
