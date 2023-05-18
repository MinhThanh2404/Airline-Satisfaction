# Airline-Satisfication
This is a group final project of Data Analysing Programming subject. We are asked to choose a dataset and apply all the knowledge introduced during the course to analyse it. Our dataset is about the passengers' qualification in many respects after flights from an airline company. Through this research, we aim to predict how the customers qualify their experience on the flight with 2 ways of approach: clustering and classification.
## About the dataset
This data is given by an anonymous airline organization, about the feedback of the customers on various context and their flight data, which have been consolidated. It has been labelled by the categorical variable named Satisfaction (satisfied / dissatisfied).
## Workflow
1. Import data
2. Preprocess data
3. Visualize data
4. Cluster: skip the categorical variable - Satisfaction, build and apply a unsupervising model, evaluate the accuracy by comparing the new label created by the model with the original label, aka the categorical variable.
5. Classify: divide the dataset into the training set and the testing set (8:2), apply various supervising models to evaluate which model gives the best prediction

### *The report is written in Vietnamese. To summarize:*
* After preprocessing, we encoded all the non-numerical variables, and conducted some dimensionality reduction techniques, which resulted in the omission of the Departure Delay in Minutes variable.
* Classification: we chose k-NN, Decision Tree, SVM as supervising models, and accuracy scores to evaluate the models. It showed that Decision Tree and SVM classified well.
* Clustering: we intended to choose 2 models - KMeans and HAC, however, due to the large number of observations in this dataset and the limited RAM of the program, we could only apply KMeans model. With the number of clusters k=2 (equal to the number of dinstinct values of Satisfaction variable), the KMeans model generated quite poor predicting result, proved by the 0,172 silhouette score. We decided to take a pair of variables having lowest correlation coefficient - Class and Gate location - to cluster the passengers. Eventually, dividing the dataset into 5 clusters was evaluated 0,602 silhouette score, a pretty acceptable score.
