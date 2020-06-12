# Article-Recommender-System
For this project I analyze the interactions that users have with articles on the IBM Watson Studio platform, and make recommendations to them about new articles I think they will like. 

My project is divided into the following tasks

I. Exploratory Data Analysis

Provide Some insight into the descriptive statistics of the data as well as data visualization.


II. Rank Based Recommendations

Provide functions to get top n articles names and ids with highest number of user subscriptions.


III. User-User Based Collaborative Filtering

Provide functions to get top n article subscriptions from users who have highest similarities to the input user id.
* Reshape the dataframe with users as the rows and articles as the columns. 
* Each user should only appear in each row once.
* Each article should only show up in one column. 
* Place a 1 where the user-row meets article-column if the user subscripted the article. 
* Otherwise, place a 0 where the user-row meets that article-column.


IV. Content Based Collaborative Filtering

Provide functions to get top n articles names and ids with highest similarities to the input article id.
* Utilize NLP techniques to remove punctuation, stopwords and tokenize the doc body text.
* Perform topic modeling which has 7 topics in total via LDA model from Gensim.
* Find the top 3 topics for each article and form a new dataframe with column article id, article name and other 7 columns representing 7 topics. Place 1 where the article row meets the topic column if that topic is in the top 3 topics of the article. Otherwise, place zero.
* Find the top 3 topics for the unseen text using the LDA model. Form the same row for the unseen text with 1s under the top 3 article columns.
* Find the similarity by computing the dot product of the article row and the transpose of the unseen text row.
* Return the top n ariticles with highest similarities.


V. Matrix Factorization
Build use matrix factorization to make article recommendations to the users.
