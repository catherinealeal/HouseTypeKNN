# Predicting House Type Using K-Nearest Neighbors 

## Goal 

Use the k-nearest neighbors algorithm to predict the housing type of homes in Melbourne. Also decide the best k-value that yields the highest accuracy and whether to implement weighted or majority voting. 

## Creating Classifier 

The function knn_class, takes five parameters, the training dataframe (that includes the target column), the hyper parameter k, the name of the target column, a single observation row of the test dataframe, and a boolean use_weighted_vote.  

When use_weighted_vote is set to true, weighted voting is implemented, otherwise majority voting is used. 

The function returns the predicted target classification for that observation. 

For each value of k in the set {1,3,13,25,50,100}, the class prediction for each oberservation in the test set was calculated, as well as the overall accuracy of the classifier. 

![image](https://github.com/catherinealeal/HouseTypeKNN/assets/100166102/23c29506-8247-46b3-83bc-74116bc98a32)

## Conclusion 
- I would chose k = 25 and a weighted voting scheme because these parameters yield the highest accuracy of predictions, as seen by the orange peak in the plot. 
- Weighted voting is generally more accurate because it takes into account the distance from each point to the target variable, so it makes sense that the weighted voting accuracies would be higher than those of the majority voting. 
- Increasing the k-value has pros and cons. While increasing k does make the prediction more robust to noise, it may cause some trends in the data to be overlooked. We can tell from the downward trend of the plot after k=25 that considering more points actually misinforms the prediction, so ideally, 25 neighbors should be considered.

## View full project [here](https://github.com/catherinealeal/HouseTypeKNN/blob/main/HouseTypeKNN.ipynb)
