# Who Said That?
## Reddit API Web Scraping, NLP, and Classification Models

### Problem Statement  
Have you ever been in a situation where two programs are on at the same time and you find yourself having to share the TV with your roommates or live-in significant other? Fans of Bravo's Real Housewives franchise might butt heads with avid watchers of the NBA when both programs happen to be airing simultaneously. Perhaps there is a way we can quantify how similar these seemingly different programs.  
Using text webscraped from Subreddits [r/BravoRealHousewives](https://www.reddit.com/r/bravorealhousewives) and [r/NBA](https://www.reddit.com/r/nba), this project utilizes NLP in order to create a classification model that determine which particular subreddit a post or comment came from.  
### Executive Summary
After using NLP methods like stemming, lemmenizing, tokenizing, and CountVectorizer, and TF-IDF transformations, we fit various classification methods (Logistic Regression, Random Forest, AdaBoost, Gradient Boost, and MultiNomial Naive Bayes) through a Voting Classifier and end up with a train accuracy score of 92% and test accuracy score of 87%.  
This model can be used to compare and contrast speech patterns and topics concerning fans of the Real Housewives and the NBA. In the end, we discover similar words used frequently in both topics which can make it more difficult to train our models to better predict classes. With more time and processing power, we might include additional features (higher n-grams) and tune different hyperparameters.  
### Table of Contents
- Data  
  - Text of comments & posts from both subreddits: [data_final.csv](./data/data_final.csv)  
  - Tuned models and train/test data: [models.pk](./data/models.pk)
- Code  
  - [Web Scraping and Data Cleaning](./code/web_scraping_and_data_cleaning.ipynb)  
  - [Preprocessing and Hyperparamter Tuning](./code/preprocessing-and-hyperparameter-tuning.ipynb)  
  - [Final Model and Conclusion](./code/final-model-and-conclusion.ipynb)  

### Data Dictionary
Combined webscraped data collected in `final_data.csv`  

| text |target|
|---------|--------|
| Text collected from posts and comments | 1 = BravoRealHousewives, 0 = NBA |
