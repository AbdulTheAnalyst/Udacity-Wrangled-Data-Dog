# Udacity - data - cleaning (Wrangling)

This is one of my project on Udacity Data Analyst Nanodegree
### Domain
This analysis is focused on **Animal Breed** Analytics
## Project Overview
The dataset wrangled (and analyzing and visualizing) is the tweet archive of Twitter user @dog_rates, also known as WeRateDogs. WeRateDogs is a Twitter account that rates people's dogs with a humorous comment about the dog. These ratings almost always have a denominator of 10. The numerators, though? Almost always greater than 10. 11/10, 12/10, 13/10, etc. Why? Because "they're good dogs Brent." WeRateDogs has over 4 million followers and has received international media coverage.
## Project Steps Overview
Step 1: Gathering data

Step 2: Assessing data

Step 3: Cleaning data

Step 4: Storing data

Step 5: Analyzing, and visualizing data

Step 6: Reporting

- The Wrangling process is divided into three steps:

  1 Gathering the data 

  2 Accessing the data 

  3 Cleaning the data 
Each step was explained below:
### 1. Gathering Data 
The data used was gathered from three different sources
- A. **Enhanced Twitter Archive** :
    Contains data extracted programmatically from tweet data sent by WeRateDogs. The data include the rating, dog name, and dog stage and some other related information.
- B. **Image Prediction File** :
    Produced by running every image in the WeRateDogs Twitter archive through a neural network that classifies breed of dogs. This process resulted in a table full of image predictions (the top 3 only) alongside each tweet_id, image URL and the image number that corresponded to the most confident prediction (numbered 1 to 4 since tweet can have up to 4 images).
- C. **Additional Data through Twitter API** : Obtained by querying Twitter’s API then stored in a txt called tweet-json. Gathering this data requires a Twitter developer account The ready made version was used in this work and was read line by line into a pandas DataFrame with tweet ID, retweet count, and favorite count , and was later saved to a ‘tweet_data.csv’ file for future purpose.
### 2. Accessing Data 
After gathering each of the above pieces of data, they were assessed visually and programmatically for quality and tidiness issues.
- A. **Tidiness:**

T1. Dog stage data is separated into 4 columns 

T2. All data is related but divided into 3 separates dataframes

- B. **Quality**:

Enhanced Twitter Archive :
Q1. There are 181 retweets as indicated by tweeted _status_id 
Q2. Some dog names are invalid (None, a, an, & the missed of name) 
Q3. Invalid tweet_id data type (integer instead of string) 
Q4. Invalid timestamp data type (string not datetime)
