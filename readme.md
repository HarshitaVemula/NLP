# Multiclass classification of movies using their subtitles based on their ratings.
<img src="movie.jpg" width="100%">

# Task
A motion picture content rating system is an organization designated to classify films based on their suitability for audiences due to their treatment of issues such as sex, violence, or substance abuse; their use of profanity; or other matters typically deemed unsuitable for children or adolescents. 

The Motion Picture Association of America (MPAA) classifies movies into 5 categories.
<img src="ratings.png" width="100%">

The task is to classify movies into these five categories while exploring the various multiclass classification algorithms.

# Evaluation
The evaluation metric used is accuracy per class and F1 score.

# Models 
- One vs all - SVC and Logistic Regression
- All pairs
- Linear multiclass predictors

# Methodology
- Data preprocessing: The Data collected from various repositories was cleaned by dropping reapeated instances and structured data frames were created. The text data was then cleaned by removing stopwords, stemming and lemmatizing. tfidf vectorizer was used to obtain the required covaraites(1 grams, 2 grams and 3 grams) from the text. The titles were also tokenized and were used as features.

- Models : 

One vs all, all pairs and multiclass predictors were considered. Theoretically multiclass predictors should perform better than the other 2 kinds of classifiers. But this did not seem to be the case practically.

The classifiers used were:
-One vs all : 
SVC : accuracy = 0.45 , f1 score (weighted) = 0.47
Logistic regression using liblinear solver with l2 penalty and balanced class weight : accuracy =.60 and f1 score = 0.605

-Multiclass classification
SVC : accuracy = 0.57 and f1 score = 0.56
Logisticregression with cv using lbfgs solver and balanced class weight : accuracy = 0.589 and f1 score = 0.578

-All pairs










