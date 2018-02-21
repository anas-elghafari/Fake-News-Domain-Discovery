# Fake-News-on-Social-Networks

3 pickle files are included here: fakenews tweets, msm tweets, and a sample of 200,000 tweets containing links that we want to classify the links or the domains. All 200,000 tweets come from users who shared fake news links, so we expect that other fake news sites and links are present in this list.

The pickle files are all lists of tweets. Each element in the list is a list of length 9, consisting of the following:
  t[0]: boolean whether or not this tweets is a retweet of another tweet
  t[1]: via: the user who made or re-tweeted this tweet
  t[2]: username original author of tweet
  NOTE: when the tweet is a re-tweet, then t[2] is the original author and t[1] is retweeter. When it is not a retweet then both fields will contain the same username
  t[3]: tweet id: unique identifer assigned by twitter.
  t[4]: the body of the tweeet
  t[5]: the expanded urls: the urls included in the body of the tweets are often (always?) automatically shortened by twitter. t[5] will store the expanded links. Note: those expanded urls can themselves be links shortened by fb.me or bit.ly. In that case, twitter API does not how to exapnd those, and so they remain as they are.
  t[6]: the geolocation if it is exists (otherwise, 'none')
  t[7]: retweet count
  t[8]: favorites count
  NOTE: if t is a retweet, then the retweet and fav counts refer to the underlying tweets
  
  
  
  
