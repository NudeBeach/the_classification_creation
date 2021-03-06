# Final Thoughts

I began this project with one goal in mind. I wanted to build and evaluate several machine learning models with the purpose of finding the best model to predict credit risk. I split this into two notebooks, one focused solely on resampling methods and the other focused on ensemble classifiers. Evaluating the models ended up being broken into three questions:

  1. Which model had the best balanced accuracy score? 
  
  2. Which model had the best recall score?

  3. Which model had the best geometric mean score?

I ended up adding a fourth question in the ensemble notebook:

  4. What are the top three features?

I will first give the answers for each respective notebook.

## Resampling
1. Which model had the best balanced accuracy score?
    -   With balanced accuracy you want your score to be as close to one as possible. With this idea in mind, Oversampling was the best technique, with SMOTE oversampling being the best method.
  
2. Which model had the best recall score?
    -  With recall score one is again looking for a number as close to one as possible. Keeping this in mind, Oversampling ended up being the best technique and oddly, both methods ended up having the same average for recall.

3. Which model had the best geometric mean score?
    - Again with geometric mean score we are looking for a number close to one. Keeping this in mind, both of my Oversampling algorithms ended up having the same geo score of 0.84.

## Ensemble Classifiers

1. Which model had the best balanced accuracy score? 
    -  When looking at a balanced accuracy score one wants a number that is closest to one. From the data one could see that the EasyEnsembleClassifier had the best balanced accuracy score. It also had the best compared to the resampling algorithms as well.
  
2. Which model had the best recall score?
    - With recall we are once again looking for a number closer to one. Looking at the "rec" column in our classification report one can see that the EasyEnsembleClassifier had the better recall, but not by much.

3. Which model had the best geometric mean score?
    - Once again we are looking for a number that is closer to one. Looking at our classification report one can see that the EasyEnsembleClassifier basically demolished the BalancedRandomForest.

4. What are the top three features?
    - When analyzing the BalancedRandomForest I found that the top three features that had an effect on the target data were: 1. Loan Amount, 2. Interest Rate, 3. Installment.

### Conclusion

Again, I began this project with the goal of finding the best model to predict credit risk. I looked at two different algorithm techniques for making predictions with imbalanced data. By using resampling methods I found that SMOTE oversampling was the best method with the highest balanced accuracy score. Both Oversampling methods had an equal score for recall and both had an equal score for geo. This illustrates that first off, oversampling as a whole is the better method when compared to undersampling. Then we can see that of the oversampling techniques, what really differentiates them is the balanced accuracy score and not even by alot. Looking at Ensemble Classifiers I found that EasyEnsembleClassifier basically won everything. EasyEnsembleClassifier had the best balanced accuracy score, the best recall score, and the best gemoetric score. Then going deeper and comparing the EasyEnsembleClassifier with a balanced accuracy of 0.925 to SMOTE oversampling with a balanced accuracy of 0.83885, the EasyEnsembleClassifier was clearly the best overall method for making predictions. The EasyEnsembleClassifier was very impressive. On a sidenote, with the Ensemble Classifiers, I also found that the three features that had the biggest impact on the target data were: 1. Loan Amount, 2. Interest Rate, and 3. Installment, which makes sense.  