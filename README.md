# Netflix_Movies-and-TV-Shows-Clustering

Introduction:-

Netflix is the world's leading streaming entertainment service with over 209 million paid memberships in over 190 countries enjoying TV series, documentaries and feature films across a wide variety of genres and languages.

It is a streaming service that offers a wide variety of award-winning TV shows, movies, anime, documentaries and more – on thousands of internet-connected devices. Members can watch as much as they want, anytime, anywhere, on any internet-connected screen.

Project Overview:-

The dataset consists of tv shows and movies available on Netflix as of 2019. It has been collected from Flixable which is a third-party Netflix search engine.

In 2018, they released an interesting report which shows that the number of TV shows on Netflix has nearly tripled since 2010. The streaming service’s number of movies has decreased by more than 2,000 titles since 2010, while its number of TV shows has nearly tripled.

Objective:-

In this project, we are required to do

Exploratory Data Analysis

-> Understanding what type content is available in different countries

-> Is Netflix has increasingly focus on TV rather than movies in recent years.

-> Clustering similar content by matching text-based features

DATASET:-

The dataset consists of following columns:-

-> show_id : Unique ID for every Movie / Tv Show

-> type : Identifier - A Movie or TV Show

-> title : Title of the Movie / Tv Show

-> director : Director of the Movie

-> cast : Actors involved in the movie / show

-> country : Country where the movie / show was produced

-> date_added : Date it was added on Netflix

-> release_year : Actual release year of the movie / show

-> rating : TV Rating of the movie / show

-> duration : Total Duration - in minutes or number of seasons

-> listed_in : Genre

-> description: The Summary description

Our data set contains 7787 rows and 12 columns. We have 1 numeric and 11 categorical independent features.

Workflow:-

The workflow of this problem is divided into following sections:-

I. Data Study

First, we will import python libraries such as NumPy and Pandas to load the CSV file. Then we will import following Python libraries for different functions

1) Matplotlib ,Seaborn and Plotly - For Visualization

2) re and string- For Text Cleaning

3) nltk- To import stop words

4) sklearn – For all mathematical calculations and clustering

Later we will perform some operations to understand and analyze the data.

II. Data Manipulation

Since director column has highest null values, 30.7% of data is missing and cast, country , date added , rating column has more than 10% null values. In order to treat missing values in the director column we can fill it with ‘unknown’ and in the cast column with 'No cast', country can be filled with mode value, null values of date added and rating are very less so they can be removed.

We have created new features to store date, day, month and year separately. We have handled outliers using the IQR method.

III. EDA and Visualisation:-

1. Type of Content on Netflix

69.1% of the content available on Netflix are movies and the remaining 30.9% are TV Shows

2. Release year of Movies/TV Shows

1> Maximum number of Movies streaming on the platform were released in 2017.

2> Most TV Shows streaming on the platform were released after 2015

3> Since the number of movies releasing each year has started decreasing after 2017 whereas number of TV Shows have increased gradually after 2015

3. Number of Movies/TV Shows added per Year and per Month

1> Number of movies added to the platform showed a deliberate increase from 2017 to 2019 and has decreased after that.

2> TV Shows have been added continuously from 2015 and its number has been increased every year.

Most number of Movies and TV Shows are added between October and January

4. Top 10 Directors

Top 3 Directors are-

1> Jan Suter

2> Raul Campos

3> Marcus Raboy

5. Top 10 Actors

Top 3 Actors are

1> Anupam Kher

2> Shah Rukh Khan

3> Om Puri

6. Top Genres on Netflix

In both Movies and TV Shows top genres are International Movies/TV Shows, Dramas and Comedies Movies/TV Shows.

7. Top 10 Countries producing content on Netflix

United States is the country producing maximum content on Netflix followed by India and UK.

8. What Type of content produced by Top 10 Countries

i) Drama, International Movies, and Comedies seem popular choices in most countries.

ii) British and International Tv Shows dominate in the United Kingdom.

iii) Regional specialties such as Anime in Japan, Spanish TV Shows in Spain and Korean Tv Shows in South Korea are more prominent in these countries.

iv) It is also observed that in the countries where the regional language is not English, International Tv Shows/Movies are more in demand.

9. Ratings of content

i) TV-MA :for Mature Audiences

ii) R : Restricted

iii) PG-13 : Parents strongly cautioned. May be Inappropriate for ages 12 and under

iv) TV-14 : Parents strongly cautioned. May not be suitable for ages 14 and under

v) TV-PG : Parental Guidance suggested

vi) NR : Not Rated

vii) TV-G : Suitable for General Audiences

viii) TV-Y : Designed to be appropriate for all children

ix) PG : Parental Guidance suggested

x) G : Suitable for General Audiences

xi) NC-17 : the content isn't suitable for children under 17 and younger

xii) TV-Y7-FV : Suitable for ages 7 and up

Most content on Netflix is rated for Mature Audiences(MA) and over 14 years old

10. Duration of Movies/TV Shows

i) Most movies on Netflix have a duration range from 80 to 120 minutes

ii) Screenshot 2023-01-07 185107

iii) Most number of TV shows are having single season

iv) Grey's Anatomy is the longest TV Show with 16 Seasons

v) Feature Engineering

Firstly, we add genres, rating and description of our dataset to form our target variable.

I. Text Cleaning

We conerted all words in lowercase and remove everything except the alphabets.

II. Word Tokenization

We converted the sentence into a token of words using the tokenization method.

III. Punctuation Removal

We have applied a function to remove punctuation in the target variable.

IV. Stop Word Removal

We have removed all the stop words using nltk library.

V. Lemmatization

Applying Word Net Lemmatizer to extract meaningful words from the target variable.

VI. TF-IDF-Term Frequency-Inverse Document Frequency

Term frequency-inverse document frequency is a text vectorizer that transforms the text into a usable vector.

VII. Clustering Algorithms

1} K-Means Clustering

K-means is a centroid-based algorithm, or a distance-based algorithm, where we calculate the distances to assign a point to a cluster. The main objective of the K-Means algorithm is to minimize the sum of distances between the points and their respective cluster centroid.


2} Hierarchical Clustering

Hierarchical clustering is an unsupervised machine learning algorithm, which is used to group the unlabelled datasets into clusters. In this algorithm, we develop the hierarchy of clusters in the form of a tree, and this tree-shaped structure is known as the dendrogram.


3} DB SCAN

DBSCAN stands for Density-Based Spatial Clustering of Applications with Noise. It is a density-based clustering algorithm. The algorithm increases regions with sufficiently high density into clusters and finds clusters of arbitrary architecture in spatial databases with noise.

CONCLUSION

I) Majority of content on Netflix is movies. Netflix has 5372 movies and 2398 TV shows.

II) The number of movies on Netflix is growing significantly faster than the number of TV shows.

III) We saw a huge increase in the number of movies and TV Shows after 2015. Highest number of movies released in 2017.

IV) Less Number of movies released after 2017 whereas a greater number of TV shows were released in this period.

V) Most of these contents are released either in the year ending or in the beginning.

VI) International Movies/TV Shows are the top most genre in Netflix which is followed by Drama and Comedy movies/TV shows.

VII) The United States is the major content producing country on the platform followed by India, UK, Japan, South Korea.

VIII) Jan Suter and Raul Campos have directed the most content on Netflix.

IX) Also 6 of the actors among the top ten actors with maximum content are from India. Anupam Kher, Shah Rukh Khan, Om Puri are the top 3 Actors.

X) TV-MA tops the rating chart, indicating that mature content is more popular on Netflix.

XI) Most of the movies have a duration between 80 to 120 minutes.

XII) Most TV shows have a single season. Grey's Anatomy is the longest TV Show with 16 Seasons.

XIII) k=13 was found to be an optimal value for clusters using which we grouped our data into 13 distinct clusters.
