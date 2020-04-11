# sc_challenges
Notebooks and files containing attempts at the Skill Connect Challenges

# Week 1 challenges 
## Classification
  **Dataset**
  [Abalone](http://archive.ics.uci.edu/ml/datasets/Abalone) dataset used, target variable is number of rings. Since boundaries between subsequent rings may be too thing the 24 classes have been grouped together to form 6 classes.  

  **Algorithms Used**
  1. Logistic Regression (one vs all)
      - 61.48% (self coded)
      - 68.06% (sklearn)
  2. Naive Bias
      - 51.51%
  3. kNN 
      - 67.22% (self coded)
      - 67.58% (sklearn)
  4. SVM 
      - 69.61% (sklearn)
  5. Decision Trees
      - 60.77% (sklearn)
  6. Boosted Trees
      - 67.10% (sklearn)
  7. Random Forest
      - 67.70% (sklearn)
  8. Neural Networks
      - 68.54% (pytorch)
      - 18.80% (sklearn - overfit)



## Clustering
  **Dataset**
  [Iris](https://scikit-learn.org/stable/modules/generated/sklearn.datasets.load_iris.html) dataset used, self coded example uses only two features for visualization in 2 dimesions and to show centroid movement paths. Sklearn usage involves all the classes.
  **Accuracy**
  88.33 %

## Linear Regression
  **Dataset**
  [Boston Housing](https://scikit-learn.org/stable/modules/generated/sklearn.datasets.load_boston.html) dataset used.  
  Self coded implementation uses pytorch to calculate gradients.  
  **MSE/2**
  - Self coded: 205.07
  - Sklearn: 103.55
