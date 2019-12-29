# movie-recommendation-demo
This is a movie recommendation system built in Java that I made for a class project.  The application reads user information from a data set and then predicts which movies the user will most like based on thier prior ratings.  

## Description
This is an item-based recommendation system. Recommendation systems are widely used on the web for recommending products and services to users based on their past actions and interaction with the system. Recommendation systems have important applications in several areas, such as:
* Product recommendation. Amazon and ebay provide recommendations to you based on yourpurchase history. Facebook recommends friends. Dating websites recommend dating partners,etc.
* Movie recommendation: Netflix offers its customers recommendations of movies they mightlike. These recommendations are based on ratings provided by users. In fact, the importance ofpredicting ratings accurately is so high, that Netflix offered a prize of $1M to the first algorithmthat could beat its own recommendation system by 10%.
* News Articles: news services recommends news articles to the readers based on the articles thatthey have read in the past.

**Input into the recommender system**
The input to your recommender system is a dataset consisting of 100,000 ratings from about 1000 users on about 1700 movies. The dataset is extracted from here: http://files.grouplens.org/datasets/movielens/ml-100k.zip

**There are two input files attached to this assignment:**
1. movies.dat: Each line in the movies.dat represents a unique movie
2. ratings.dat: All ratings are contained in the file ratings.dat

**Output of the Program**
The recommender system will predict the ratings that the user will give to the movies he/she has not rated yet.

user ID: 1 top 5 recommendations: Cyclo (1995)::4.382758930148253| Office Killer (1997)::4.24082725472752| Little City (1998)::4.234925942215377| Death in Brunswick (1991)::4.224473123463171| Mamma Roma (1962)::4.178130372636395|

## Predicting movie ratings using an item-based recommender system
An item based recommender system predicts a rating that userId (u) will give to itemId (i) based on the ratings that the user has previously given to items that are similar to i. More specifically, to predict rating(u,i), an item-based recommender iterates through all items that have been previously rated by user u and takes the weighted average of the ratings that the user gave to such items . The rating of item j is weighted by the similarity of item j to item i. That means the more similar item j is to the target item i, the more its rating weighs in predicting the rating of item i.

![alt text][logo1]

[logo1]: https://github.com/ChrisToplikar/movie-recommendation-demo/blob/master/algorithm%20of%20recommender.JPG?raw=true
 "Algorithm"
 
There are various metrics to measure the similarity between two items. The one that we use for this project is the Cosine similarity between the two item vectors.

Suppose that we represent each item as a vector of all the ratings for that item, that is:

item<sub>i</sub>=(r<sub>1i</sub>,r<sub>2i</sub>,...r<sub>ni</sub>)

Where r<sub>ui</sub> is the rating given by user u to items i and n is the number of unique users in the system. If user u has not rated item i, then the entry r<sub>ui</sub> = 0.
Then the cosine similarity of item<sub>i</sub> and of item<sub>j</sub> is calculated as follows:
![alt text][logo2]

[logo2]: https://github.com/ChrisToplikar/movie-recommendation-demo/blob/master/cosine%20similarity.JPG?raw=true
 "Cosine Similarity"
 
 Where N is the set of all unique users.

## Getting Started
Download or clone the repository. Run the Main.java file

## Description of Project Files
* Main.java- This is the main entry to the application
* DataBase.java- This class reads the input data set and converts the data into movie or rating objects
* Movies.java- This class is used to represent the movie data set.
* Ratings.java- This class is used to represent the rating data set.
* RatingPredictors.java- This class computes the predicted ratings of users with movies
* PredictionRatingDataHolder- This is a utililty class that keeps track of all predicted ratings.

## Testing
Unit tests were performed on different test samples.  A sample dataset was used in testing.



