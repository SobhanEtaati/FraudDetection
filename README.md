Overview:
- We intend to use the KNN method to detect fraudulent transactions. This dataset comprises transactions
	made using credit cards by European cardholders in September 2013, and each data point has 30 attributes.
	The primary attributes, V1, V2, ..., V28 are derived using Principal Component Analysis (PCA), and the
	only attributes not processed by PCA are Time and Amount. The Time attribute represents the elapsed time
	between transactions, while the Amount represents the transaction amount. The Class attribute is the
	model's output.

General steps of the algorithm:
  1. First, we split the data into training and test sets.
  2. Next, we select the value of k. (using Grid Search)
  3. For each data point in the test set, we perform the following steps:
    3.1. Select a distance metric to measure the distance between points.
    3.2. Choose the k nearest neighbors.
    3.3. Assign a value to the data points based on weighted or unweighted voting of these neighbors.
     
Implementation of KNN:
- To implement KNN, we must first identify the appropriate value for k. To achieve this, we can use Grid
  Search, which fits k values ranging from 1 to 40 and then reports the best one using Grid.best.
  However, due to the time-consuming nature of this process, we have separately fitted the model for k values
  from 1 to 5. For each k, we printed the Weighted Average, Macro Average, and Accuracy values and
  compared them (Fig.1). The Minkowski metric has been used in the algorithm.
	
Conclusion:
- The model should ideally perform better on the test data. By comparing the accuracy values on the test data,
  it is found that the best choices for k are 2 and 4 within the range of 1 to 5.
  However, as previously mentioned, a more effective approach is to use Grid Search to determine the best k
  value and the optimal metric within specified ranges. Nonetheless, this project is primarily aimed at
  understanding the practical implementation of the KNN algorithm and its performance on a real dataset.
