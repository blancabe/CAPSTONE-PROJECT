Final Project done during the Immersive Course of Data Science at General Assembly Oct,2018-Jan,2019

INDEX:

- Goals of the project
- Models tested
- Thought process & methods of producing it
- How to run the project
- Why you created the project
- What’s interesting about it
- Link to my Jupyter Notebook


GOALS OF THE PROJECT
- 1st intention: Predict number of health inspections from ratings, reviews and bussines characteristics.
- 2nd intention: Predict Restaurant Ratings from reviews and bussines characteristics. FINAL DECISION: This project is about predicting restaurant ratings from restaurants reviews and other characteristics of the businesses.

Had to orginize data from 6 files and I end up with 2 different datasets, the first one is the Reviews gathered from Yelp documentation. It is a json file that I decode with the method JSONDecoder to read it. The second is an other json file corresponding to business features; and then I merged both with the business ID column.


MODELS TESTED

- Has been used supervised learning choosing regression models as well as classification ones. For Regression models linear regression was used first to see how was the score given without any tunning hyperparameters. GridSearch improves the score of linear regression later. Decission Tree Regressor was also performed to reduce MSE of the first model.MSE score is more representative than R2 because R2 is not taking into account that values in ratings go from 0.5 to 0.5; instead is taking all the posisble values between 0 and 5 to predict. For classification models has been chosen Logistic Regression, Decission Tree Classifier and Bagging with DT.

- For regression models evaluation has been done through RMSE and in classification case through Accuracy and Precission.

Models has been run a few times due to incongruity of scores. Still uncertainty about why models are given such a good scores and working on it.


THOUGHT PROCESS AND METHODS OF PRODUCING IT

- Firstly, after cleaning and preprocessing all the data and save it in 30 different CSV FILES I though in perform Natural Language Processing with the 'Text' column, trying to include into the list of STOPWORDS of the Countvectorizer all the word I dind't want to take into account for lack of predictive value. I had to leave it for further improvments as I had lots of problems with my kernel. So I set up the parameter max_features=2000 in the vectorizer to take into account just the most frequent words. Secondly I took the unique categories from the 'Categories' column and use them as a new features. With these selection of features plus the ones refered to the business characteristics I started to run my models -Want to improve the model doing Sentimental Analysis and using other Vectorizers and processes to filter the worthy words used as features to predict. -Also would like to do Recommendation systems and Topic Modeling and Latent Dirichlet Allocation (LDA)
HOW TO RUN THE PROJECT

- I run it in a Jupyter Notebook, launching an EC2 instance using Amazon Website Services to speed up the processes and creating a DATABASE in PostgressSQL where able to store all the data (the 30 csv files created previously) to later acces it.
WHY YOU CREATED THE PROJECT

- As a part of a final project during the Data Science Immersive Course at General Assembly, it was a requirement to complete succesfully the course.


WHAT IS INTERESTING ABOUT IT

- I found very interesting how much scores were changing depending on the features included, and discovering that word features were not as good predictors as other columns.


LINK TO MY JUPYTER NOTEBOOK

