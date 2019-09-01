# R-KNN-Caravan
KNN model using Caravan dataset to classify who purchase insurance from Caravan

# Introduction
We will discuss the K-Nearest Neighbor algorithm and how to use it for classification problems. 

# Prediction Algorithm<br>
1. Calculate the distance from the new point(X) to all the existing data points<br>
2. Sort the points in your data by increasing distance from X<br>
3. Predict the majority label of the "k" closest points

- Choosing the value of "k" is very important because "k" will determine which class is the new data point assigned to.
- How you calculate the distance is also very important

### The disadvantage is:<br>
- High prediction cost when the dataset is very large in size
- Not good for a dataset that has too many features because it throws off your ability to measure distance in various dimensions.
- Also, categorical features don't work well for KNN

# Data
In the ISLR library, we have Caravan dataset that has 5822 rows and 86 variables. Each row is for one customer. This is a bunch of customer
demographic data measured across many variables. The variable `Purchase` has two levels- "yes" or "no".It measures if the customer purchased
insurance from Caravan company. Only about 6% of customers in this dataset purchased insurance. 

# Steps:
1. Get the data<br>
2. Make sure there are no missing values<br>
3. Perform EDA<br>
4. Save the dependent variable<br>
5. Normalise all the independent variables<br>
6. Do the train-test split on data<br>
7. Build the KNN model using class library's knn(): 
  predicted.dependent.var <- knn(train.data, test.data, train.dependent.var, k=1)<br>
8. Evaluate the model by calculating the misclassification error: missclass.err <- mean(train.dependent.var != predicted.dependent.var)<br>
9. Find out the ideal value of k that will minimize the misclassification error by using a for loop for different k values<br>
10. Visualize the K elbow method output<br>
11. Finalize the ideal k value and get the final predictions of dependent variable in the test dataset

