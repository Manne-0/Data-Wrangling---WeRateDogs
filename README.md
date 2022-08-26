# Data-Wrangling---WeRateDogs
# Introduction
In this project, I practiced all I learned in lesson 2 (data wrangling lesson) of the Udacity Data Analysis Nanodegree Program. The dataset that I wrangled (and analyzing and visualizing) was the tweet archive of Twitter user @dog_rates, also known as WeRateDogs. WeRateDogs is a Twitter account that rates people's dogs with a humorous comment about the dog.

# Python Libraries
- os
- pandas
- numpy
- tweepy 
- requests
- json
- matplotlib.pyplot
- seaborn

# Data Wrangling 
in this project, I carried out the following task:

1. Gathering data
2. Assessing data
3. Cleaning data
4. Storing data
5. Analyzing, and visualizing data
6. Reporting

## Gathering Data: The data were gathered from three different sources
1. WeRateDogs Twitter archive: This was provided by Udacity as a csv file and was downloaded manually. The csv file was then read into a pandas Dataframe using the pd.read_csv().

2. Tweet image predictions: This is a tsv file hosted on Udacity servers. it was downloaded programmatically using the provided URL and the Requests library.

3.Additional Twitter Data(Twitter API and JSON): I used tweet IDs in the WeRateDogs Twitter archive to query the Twitter API for each tweet's JSON data using Python's Tweepy library and stored each tweet's entire set of JSON data in a file called tweet_json.txt file. I then read this file line by line to create a pandas DataFrame that I will assess and clean.

## Assessing Data
After gathering all three datasets, i assessed them virtually and programmatically for quality and tidiness issues. I documented a total of 10 quality and tidiness issues. They are:

1. The columns; doggo, floofer, pupper and puppo all refer to dog stages and should be in one column..
2. Create one column for image prediction and another column for confidence level
3. In the Enhanced twitter archive data, the 'timestamp' column is an incorrect datatype(string instead of datetime).
4. The 'tweet_id' column has an incorrect datatype(integer instead of string).
5. There are 181 retweets
6. Unneeded columns()
7. Invalid dog name such as '0fficially', 'the', 'as', and the.
8. Some images are not dog images
9. Presence of underscores in mutiple names in dog_breed column instead of space.
10. Related dataset in three different tables.

## Cleaning Data
Before Starting the cleaning process, I made copies of the three datasets and during cleaning, I used and documented the define-code-test framework for each issues identified. After which I merged all three datasets into one high-quality and tidy dataframe.

## Storing Data
I stored the gathered, assessed, and cleaned dataframe to a csv file(twitter_archive_master.csv) using the pandas to_csv().

## Analyzing and Visualizing data
I explored the cleaned dataset and produced three insights and one visualization. insights are:

1. The Golden Retriever is the most common dog breed in this dataset. It covers 0ver 9% of the data sample sample followed by the Labrador Retriever which covers over 6% of the data sample

2. The Komondor breed is the No1 best image prediction with cinfidence level of 0.972531, followed by Clumber and Keeshond with confidence level of 0.946718 & 0.84431 respectively.

3. The scattergragh of favorites and retweets shows a positive correlation. As the favorite_counts increases, the retweets also increases.
