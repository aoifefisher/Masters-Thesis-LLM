# Masters-Thesis-LLM
Welcome to my final masters thesis project ! For this project I created large language model built with a supervised learning technique to sort text based on the most prevelant emotion present out of the four most basic emotions higlighted in the Basic Emotion Theory (anger, fear, sadness, joy). 

How I want to organize it 
- overview section
- step by step section
- data analysis section
- how this project can be useful section 

**Overview**

Within this project I had the goal of tagging each tweet with the strongest emotion creating, training, and using a machine learning model to tag the tweets with said emotion. In order to do so I used the BERT encoding algorithm to encode my text which I then numerically associated with one of the four above emotions. I then passed this trained data, with the tagged emotions having come from crowd sourced annotations, through two different machine learning models to determine which model would be the most effective. I used both a decision tree model and a random forests model, training both of them and tuning the hyperparameters. I then used the completed random forests model to compare the sentiment of tweets from the 2020 US presidential election and the 2024 US presidential election. Out of all the above I used the BERT model to embed the text but the rest of the data preparation was done by myself.  

**Step by step what I did** 
- For both models I prepared my data by importing the embedding model, embedding the tweets and encoding the four basic emotions they were tagged with to be numerical.
- I tested this data for normalcy including each emotion was equally represented within the training data.
- I eventually chose BERT as it is well known as a reliable model that has been trained on extensive amounts of data. 
-  I combined the output of the BERT embedding with the associated numerical form of the correct emotion appeared as a two dimensional array with the first part being a matrix with a fixed length of 64 inputs, normalized by adding additional 0’s to the end of the matrix to ensure the same length of all matrixes. The second part being a number 1-4 which was correlated with one of the four basic emotions. Out of all the above I used the BERT model to embed the text but the rest of the data preparation was done by myself.  
- I then split this data into training data and testing data and fed this data through both models to train them with no hyperparameters included.
- After that I tuned the hyperparameters of both of my models
- For the decision tree model I used a grid search with a variety of different inputs to find my hyperparameters which created a model with 99% accurate testing data and minimal overfitting on the first try.
- For my random forests model I had a harder time tuning my hyperparameters. I was unable to do a complex grid search with a large amount of inputs because of a lack of computing power. As a result I had to start with a more basic and general grid search offering each input variable options that were spaced distantly from each other. From there I was able to take the results of the first run and hone in on the best hyperparameter values by testing hyper parameters closer and closer to the best options with each run. I eventually got hyperparameters which had an accuracy score of 98.9% and had minimal overfitting. I also included visualizations along the way including a visualization of my decision tree in order to offer a representation of how the decision tree is tagging my text. 	
- the end I used my random forests model for my data analytics because random forests models are more reliable than a decision tree model. This is because a decision tree model relies on the algorithm and branches built within training of just one tree while a random forest model builds a large number of decision trees, a forest of them, and takes the average of these results. By relying and training on a multitude of decision trees and aggregating their predictions, random forest models become more reliable, decrease the risk of overfitting, and can be applied to a more versatile amount of data while still maintaining its accuracy. 
- For my data analytics I compared tweets about the 2020 US presidential election to tweets about the 2024 US presidential election. I looked at the change in emotions between the two elections and tested for statistical significance at the change in emotion. I created multiple visualizations to compare the two election sentiments and highlight the overall changes. My main finding is that fear was the strongest emotion during the time of both elections though the amount of fear decreased between the 2020 and 2024 election by 34.8% and instead the levels of anger and joy rose, both by around 8%.

**My data analysis**
- Include screenshots of the outcomes, include more info about the data, maybe do the same analysis with a different test set since the test set I used showed kinda crazy outcomes 

**include a section that highlights why this project is usefull** 
It's useful becaussseee
- other people can use the tagger to show sentiment
- can be used for google reviews, yelp reviews, to focus on improvement areas
- can be used for marketing 
