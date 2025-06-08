# Understanding Pig Butchering Scams Targeting Dating App Users: A Multi-Source Analysis

# Data Sources
## Google Play Store Reviews
Collected review data from 100 dating apps
Used rule-based keyword filtering
Used google_play_scraper library in python using app_id
Collected reviewId	userName	userImage	content	score	thumbsUp	appVersion	at	replyContent	repliedAt	scam_related	is_scam	sentiment	app_name	thumbsUpCount	reviewCreatedVersion


## Public Dataset
Apps: Tinder, Bumble, Plenty of Fish, Hinge
Collected reviewId	userName	userImage	content	score	thumbsUpCount	reviewCreatedVersion	at	replyContent	repliedAt	appVersion


## Social Media Platforms

**Reddit:**
Query cerain subreddits using PRAW
Used rule-based keyword filtering
Collected Subreddit	Title	ID	Author	URL	Content	Image

**Instagram:**
Query using Hashtags through instagraphi
username	caption	media_path	post_url	likes	comments

**Twitter:**
Collected using Twitter API and nitter
Query using Hashtags
link	text	user	likes	quotes	retweets	comments

# Analysis
## Google Play Store











