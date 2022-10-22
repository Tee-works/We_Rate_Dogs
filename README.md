### INTRODUCTION

The objective of the study was to gather, clean and analyse over 5000+ tweets from a twitter account @dog_rates (WeRateDogs), draw some insights and make a visualization to communicate one of the insights drawn. WeRateDogs is a Twitter account that rates people's dogs with a humorous comment about the dog. The account was started in 2015 by college student Matt Nelson, and has received international media attention both for its popularity and notoreity.

The entire data wrangling process contains three major steps, namely:

Data gathering

Data assessing

Data cleaning Although, we did go beyond by both analysing the data and visualizing it with a plot. This was necessary as the data wrangling process isn't a stand alone process and for complete analysis, it must be combined with other processess to arrive at conclusions. I would be explaining in brief details the step-by-step prodecure that was undergone in this wrangling process.

### Gathering Data for this Project
This project involved gathering of data from three different sources as listed below. For each of the data source a different method of data gathering was used namely:-

Importing data via csv Using requests to download data off internet getting data from twitter API

Although getting data from twitter API was a bit challenging for me, so i had to download the json file and read it to a dataframe. I read this .txt file line by line into a pandas DataFrame with tweet ID, retweet count, and favorite count.

### Accessing Data
For this phase, I had to look at the three datasets both visually and programmatically to be able to notice and assess any possible quality or tidiness issue in the datasets before cleaning them in the next phase. A couple of issues were noted and documented in preparation for the cleaning phase. As with most data set, there were two majoy types of issues with the dataset, tidiniess and quality issues. The documented assessment is given below.


### Quality issues
There are too much outliers in rating_numerator and rating_denominator

some of the dog names are missing and incorrect in the twitter archive data

some columns in the twitter archive data have more null values such as - in_reply_to_status, in_reply_to_user_id, retweeted_status_id, retweeted_status_user_id, retweeted_status_timestamp.

timestamp column in twitter archive data is not in datatime format.

There were 2075 rows in the image predictions compared to 2356 rows in the twitter archive.

The source column has Html tags which makes it hard to read.

the data contains retweets

the tweet_id is in integer datatype, it should be a string

Inaccurate values in the rating_numerator and rating_denominator columns in the twitter archive table

### Tidiness issues
Four columns for stages of dog (doggo, pupper, puppo, floofer) should be one category column in the twitter archive table

Predictions, Confidence and dog test are spread in three columns each.

All three tables share the column tweet_id and should be merged together.

### Cleaning Data
I made use of the define, code and test format where I first defined the operation I wanted to perform, then wrote the code for it and finally conducted tests on the dataset to see if that particular operation was performed. the cleaning section was also kind of challenging for me but i made use of stackoverflow, the internet whenever i was faced with a code problem. In the section i cleaned the quality and tideness issues found while accessing the data, A lot of unwanted rows and columns especially the ones with retweets were removed.

During the cleaning the datasets, I combined the three into one master dataset (twitter_archive_master.csv) and saved it in preparation for analysis and visualization.

For insights on analysis and visualization, please refer to the 'act_report.html' file which contains a brief summary of the insights gotten from analysis.
