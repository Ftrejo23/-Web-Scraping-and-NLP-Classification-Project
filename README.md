# Project 3 - Web Scraping and Classification
---

## Problem Statement
We are looking into breaking into the world of freelance data journalism and are reaching out to Nate Silver and co. at FiveThirtyEight so they can hear our pitch on how to create a Reddit post that will get the most engagement. We want to find out what characteristics of a post on Reddit will be the most predictive of the overall interaction on a post as measured by number of comments (above/below the median). With this we hope to provide a classification model to FiveThirtyEight that is satisfactory and jumpstart our career!

## Data Dictionary 
|Feature|Type|Description|
|---|---|---|
|subreddit|object|subreddit that the post belongs to|
|title|object|title of the post|
|number_of_comments|int|number of comments in the post|
|time_difference|int|post age in minutes|




## Executive Summary
FiveThirtyEight has made its name known as a leader in data journalism. From politics to sports blogging, the talent at FiveThirtyEight is outstanding and it is my pleasure to pitch my idea of a Reddit post classifier. Reddit is a very popular social media site and we are striving to identify the characteristics that make a high interaction post. We will build a classification model that will help us identify the most predictive characteristics of a high interaction post.

At FiveThirtyEight the mission statement, We use data and evidence to advance public knowledge — adding certainty where we can and uncertainty where we must, truly embodies what data journalism should be. Whether you are a fan of Reddit or not, it is hard to ignore that the site has 48 million active monthly users. Being able to create a post with high interaction is a great way to get information out to a massive audience. What better way to advance public knowledge than through public awareness.

In order to create our classification model, we will be web scraping using the Reddit API PRAW. From here we will clean our data of any missing values and any duplicates. Once we have all our data scraped and cleaned then we can move on to preprocessing our features. Once our data is processed to our liking we can move on and start testing different classification models, shooting for a model that produces the highest accuracy with interpretable results.

As a recent graduate of General Assembly, I have gained the experience necessary to undertake such a task. I am familiar with the skills needed and have completed prior projects that showcase a high aptitude to perform. I am also genuinely interested in our problem at hand and I believe that to be a foundational aspect to performing good work, I am sure those at FiveThirtyEight can agree.

The opportunity to work with an entity such as FiveThirtyEight is a dream come true. The mission that they strive for is something that I truly resonate with. We will create a model that can accurately classify a “hot” post and identify the characteristics of a high interaction post. With this, we can help advance public knowledge and spread awareness of different topics to a giant user base. Let’s create this model and help further FiveThirtyEight’s mission.

### Conclusions/Recommendations
We were tasked with creating a classification model to find out what characteristics of a post on Reddit will be the most predictive of the overall interaction on a post as measured by number of comments (above/below the median). Our best model, Random Forest, produced an accuracy score of 66.68%, which is 16.68% better than our baseline. Our model also produced feature importance which allowed us to identify the top 5 features to craft a Reddit post that will have better odds of increased overall interaction.

Our model identified the folloowing 5 features as the most important: time_difference, subreddit_appears_more_than_once, subreddit_in_top_10, number, and year. The feature time_difference, or post age, is the only continuous variable so further exploration was necessary. We discovered that for our "hot" (above the median number of comments) posts the average post age was 578 minutes or roughly 10 hours. We also saw that for our "not-hot" (below the median number of comments) posts the average post age was 395 minutes or roughly 7 hours. We can gauge that when writing a post it takes time to get engagement but if our post is not "hot" after 10 hours we may want to reconsider our post. For the following 2 features, subreddit_appears_more_than_once and subreddit_in_top_10, number, we want our post to be from a subreddit that appears more than once in "hot" and in our top 10 list. The last 2 features, number and year, are tokens/words that appeared in our posts. Number is a tokenized word for any post that contained numbers so we want to make sure that our post has numbers in it to better increase our chances of a high interaction post. If possible we also want to include the word "year", potentially stating what year we are in or a past/future year, again to better increase our chances of a high interaction post.

We believe that our finding can benefit those at FiveThirtyEight but we do recommend a substantial amount of additional data be collected to better improve our model. Reddit has about 48 million active monthly users so new posts are made constantly. To create a better model we should collect data at certain day/time intervals as well to see if there is any relationship as to what day a post was made and post interaction. Collecting additional post attributes is also recommended, there may be additional attributes that our model can use to show potentially better predictive power than the features that were collected.