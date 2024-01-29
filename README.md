# Assignment-1-Database-Essentials
Twitter database schema
Purpose: We need to create database schema for Twitter like application.

let's explain each table schema in detail:

Table Users:
user_id: Primary key (unique identifier) for each user.
name: Name of the user.
email: Email address of the user.
mobile_number: Mobile number of the user.
created_at: Timestamp indicating when the user account was created.

Tbale Tweets:
tweet_id: Primary key for each tweet.
comment_id: Foreign key referencing another tweet's ID if this tweet is a comment on another tweet.
user_id: Foreign key referencing the user_id in the Users table, indicating the user who posted the tweet.
tweet_content: The actual content of the tweet.
commented_content: Content of the tweet if it's a comment on another tweet.
parent_tweet_id: Foreign key referencing the tweet_id of the parent tweet if this tweet is a comment.
created_at: Timestamp indicating when the tweet was posted.

Table Likes:
Like_id: Primary key for each like.
tweet_id: Foreign key referencing the tweet_id in the Tweets table, indicating the tweet that was liked.
retweet_id: Foreign key referencing the retweet_id in the Retweets table, indicating the retweet that was liked.
user_id: Foreign key referencing the user_id in the Users table, indicating the user who liked the tweet or retweet.
created_at: Timestamp indicating when the like was made.

Table Retweets:
retweet_id: Primary key for each retweet.
original_tweet_id: Foreign key referencing the tweet_id in the Tweets table, indicating the original tweet that was retweeted.
user_id: Foreign key referencing the user_id in the Users table, indicating the user who retweeted.
created_at: Timestamp indicating when the retweet was made.

Table Follows_datas:
Follow_id: Primary key for each follow relationship.
follower_user_id: Foreign key referencing the user_id in the Users table, indicating the user who is following.
following_user_id: Foreign key referencing the user_id in the Users table, indicating the user who is being followed.
created_at: Timestamp indicating when the follow relationship was established.

These tables together form a relational database schema for a social media platform, allowing users to create accounts, post tweets, comment on tweets, like tweets and retweets, and follow other users.
