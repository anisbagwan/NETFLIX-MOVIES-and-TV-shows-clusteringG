<h1 align="center">NETFLIX-MOVIES-and-TV-shows-clustering </h1>

![image](https://user-images.githubusercontent.com/84036652/178097284-a1c325b5-98b6-4eab-a154-3de695190be2.png)

## 📄 Introduction : 
Netflix, Inc. is an American subscription streaming service and production company. Launched on
August 29, 1997, it offers a film and television series library through distribution deals as well as its
own productions, known as Netflix Originals.
Netflix can be accessed via internet browser on computers, or via application software installed on
smart TVs, set-top boxes connected to televisions, tablet computers, smartphones, digital media

players, Blu-ray Disc players, video game consoles and virtual reality headsets on the list of Netflix-
compatible devices. It is available in 4K resolution.

Netflix has become dominant company in the on-demand media industry, with 167 million paying
subscribers around the world. By creating compelling original programming, analysing its user data to
serve subscribers better, and above all by letting people consume content in the ways they prefer,
Netflix disrupted the television industry and forced cable companies to change the way they do
business.

## 🎯 Objective:
Our main objectives of this project is to do exploratory analysis and find useful insights from dataset,
to understand what type content is available in different countries, also to find out is Netflix has
increasingly focused on TV rather than movies in recent years and at last to do clustering of similar
content by matching text-based features from dataset.

## 🛠 Data Pre-processing:
 * In first few steps I hovered aroundx dataset like understood the summury of data.
 * Checked shape of data that have 7787 rows and 12 columns. These columns are the independent features and one of them is a dependent feature.
 * Then checked the null count of dataset using 'info()' method but fortunately data doesn't have any null values. Also saw the data types of columns.
 * After that counted the unique elements for each vriable. And then started the pre-processing of data.
 * In pre-processing of data we checked for null count of data.
 * We got 5 columns- "director","cast","country","date_added"and "rating" , with null values in it. Dropping whole rows with null values would lead to loss of information. Better approach would be to replace null values with a clear text indicating "No Data".
 * After that we checked for duplicate values but fortunately the datasrt doesn't have any kind of duplicate values in it.
 * Then we moved to next step that is Feature Engineering.
 
## 💡 Feature Engineering:
 * From all the variables we have - "date_added" and "release_year" indicates a date and year respectively. Hence, we can change their values to their appropriate type i.e datetime. Doing this will help us to extract month and year from the "date_added" column for the analysis part.
 * From this changes we came to know that, Netflix added all its contents in the span of 14 years, from 2009 to 2021.

## 🔍 Exploratory Data Analysis:
  *  We started this project with the intention to obtain some useful insights related to the type of Netflix
content. 
  *  For this, we performed exploratory data analysis on our data after cleaning and making it
easy to analyse.
  *  This analysis helped us to understand the trend. We found that most of the content
on Netflix are of TV-MA and TV-14 rating. USA and India are two countries producing the maximum
number of contents.
  *  Documentaries and stand up are top genre in terms of number of contents they
have on platform.
  *  Further we found number of movies on Netflix outnumbers TV-shows.
  * Below pie graph is showing the content of netfilx in percentage.
    
![image](https://user-images.githubusercontent.com/84036652/177276496-9aef61ae-72ec-416b-bad1-a3529c283288.png)
  * Clearly number of Movies on Netflix outnumbered the number of TV Shows. Almost 70% content are movies while rest 30% are TV Shows.




## ⚙️ Model Fitting:
Our next job was to make an unsupervised clustering model. For this, we processed our text by
removing unuseful characters like - stop words, punctuation and did stemming. After getting the
length for each text feature we rescaled them for generalisation and started applying algorithms. We
first used K-means clustering. In order to find appropriate cluster number, we used elbow method and
finally got the best silhouette score of around 0.35. Next, we applied Hierarchal Agglomerative
Clustering for which we made dendrogram. We also obtained silhouette score of around 0.32. With
this we achieved our objectives of the project.

## ⚖️ Model Evaluation:
