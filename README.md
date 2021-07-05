# Cryptocurrencies

## Project Overview of the Analysis
#### The goal of this project was to analyze the outcomes of six different methods of evaluating credit risk.
Using a dataset from a peer-to-peer lending services company, each of the methods was used to create training and target variables and then make predictions through the use of the `LogisticRegression` classifier.  The accuracy of each model's performance was then evaluated by the calculation of an accuracy score of those predictions.  Finally, a confusion matrix was generated in which the predictions were assigned based on their accuracy and an imbalanced classification report was printed out.  For the purposes of this analysis, two classes were determined:  `low-risk` and `high-risk`.

#### Resources
- Data Source: <br>
`Resources/LoanStats_2019Q1.csv`

- Software:  Jupyter Notebook
- Languages:  Pandas, Python
- Libraries:  `imbalanced-learn`  `scikit-learn`
- Methods: <br>Oversampling  `RandomOverSampler`  `SMOTE`  
            Undersampling  `ClusterCentroids`  
            (Over and Under) Sampling  `SMOTEENN`  
            Bias Reduction  `BalancedRandomForestClassifier`  `EasyEnsembleClassifier`
  
## Results of the Analysis
* The balanced accuracy score of the Naive Random Oversampling is 65.14%
* The precision of the imbalanced classification report for the Naive Random Oversampling is 0.01 for the high-risk class and 1.00 for the low-risk class
* The recall of the imbalanced classification report for the Naive Random Oversampling is 0.67 for the high-risk class and 0.64 for the low-risk class

![NaiveRandomOversampling](https://user-images.githubusercontent.com/77071776/124400906-8747ff80-dceb-11eb-8a03-f371db85f173.PNG)

* The balanced accuracy score of the SMOTE Oversampling is 62.67%
* The precision of the imbalanced classification report for the SMOTE Oversampling is 0.01 for the high-risk class and 1.00 for the low-risk class
* The recall of the imbalanced classification report for the SMOTE Oversampling is 0.61 for the high-risk class and 0.64 for the low-risk class

![SmoteOversampling](https://user-images.githubusercontent.com/77071776/124400916-97f87580-dceb-11eb-8188-c168a32650c1.PNG)

* The balanced accuracy score of the Cluster Centroids Undersampling is 52.93%
* The precision of the imbalanced classification report for the Cluster Centroids Undersampling is 0.01 for the high-risk class and 1.00 for the low-risk class
* The recall of the imbalanced classification report for the Cluster Centroids Undersampling is 0.61 for the high-risk class and 0.45 for the low-risk class

![ClusterCentroidsUndersampling](https://user-images.githubusercontent.com/77071776/124402077-5b307c80-dcf3-11eb-8ac6-d0e9ce45aaaf.PNG)

* The balanced accuracy score of the SMOTEENN (Over and Under) Sampling is 62.48%
* The precision of the imbalanced classification report for the SMOTEENN (Over and Under) Sampling is 0.01 for the high-risk class and 1.00 for the low-risk class
* The recall of the imbalanced classification report for the SMOTEENN (Over and Under) Sampling is 0.71 for the high-risk class and 0.54 for the low-risk class

![SMOTEENN](https://user-images.githubusercontent.com/77071776/124400926-b8283480-dceb-11eb-8890-1ff3949c8ccf.PNG)

* The balanced accuracy score of the Balanced Random Forest Classifier is 78.78%
* The precision of the imbalanced classification report for the Balanced Random Forest Classifier is 0.04 for the high-risk class and 1.00 for the low-risk class
* The recall of the imbalanced classification report for the Balanced Random Forest Classifier is 0.67 for the high-risk class and 0.91 for the low-risk class

![BalancedRandomForestClassifier](https://user-images.githubusercontent.com/77071776/124400947-dc841100-dceb-11eb-83e0-3decd43cd269.PNG)

* The balanced accuracy score of the Easy Ensemble Classifier is 92.54%
* The precision of the imbalanced classification report for the Easy Ensemble Classifier is 0.07 for the high-risk class and 1.00 for the low-risk class
* The recall of the imbalanced classification report for the Easy Ensemble Classifier is 0.91 for the high-risk class and 0.94 for the low-risk class

![EasyEnsembleClassifier](https://user-images.githubusercontent.com/77071776/124400951-e279f200-dceb-11eb-8ece-d29a3ec4695f.PNG)



## Summary
Because of the significance of the imbalance between the low-risk and high-risk class, the precision in the classification report isn't going to represent the entire story.  In this case, the recall (or accuracy) score should share more of the story.  The Easy Ensemble Classifier is the model that should be used because of the greatest accuracy of any of the models.  In combination with the accuracy score of 92.54% shown by the Easy Ensemble Classifier, the precision and recall scores place this model above the other five. 
