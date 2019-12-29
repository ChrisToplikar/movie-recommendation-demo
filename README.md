# movie-recommendation-demo
This is a movie recommendation system built in Java.  Program reads a data file containing rated movies by users.  Program predicts similar movies that user will like in descending order. 

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

## Predicting movie ratings using an item-bsed recommender system
An item based recommender system predicts a rating that userId (u) will give to itemId (i) based on the ratings that the user has previously given to items that are similar to i. More specifically, to predict rating(u,i), an item-based recommender iterates through all items that have been previously rated by user u and takes the weighted average of the ratings that the user gave to such items . The rating of item j is weighted by the similarity of item j to item i. That means the more similar item j is to the target item i, the more its rating weighs in predicting the rating of item i.

## Getting Started
Download or clone the repository. Run the Main.java file

## Description of Project Files
MainWindow.xaml.cs- Controls the main functionality and logic of the user interface.

MainWindow.xaml- User interface of the application.

Packages.cs- This file represents the Packages objects for the application.  

## Testing
Unit tests were performed on a variety of edge cases for packages.  

## Demonstration
Here is an example of the application running.
![alt text][logo]

[logo]: https://github.com/ChrisToplikar/WPF-shipping-inventory-demo/blob/master/demo.JPG?raw=true
 "Application Demo"

