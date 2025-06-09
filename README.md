# Understanding Pig Butchering Scams Targeting Dating App Users: A Multi-Source Analysis

# Data Sources
## Google Play Store Reviews
Collected review data from 100 dating apps
Used rule-based keyword filtering
Used google_play_scraper library in python using app_id
CSV files are named using corresponding dating app names
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
Used rule-based keyword filtering
Ciollected username	caption	media_path	post_url	likes	comments

**Twitter:**
Collected using Twitter API and nitter
Query using Hashtags
Used rule-based keyword filtering
link	text	user	likes	quotes	retweets	comments

# Analysis
## Google Play Store
 Divided into 9 main sections:
1. Scam Indicators in User Reviews <br>
User reviews were grouped based on the presence of scam-related keywords.
This serves as the ground truth data for further analysis. <br>
Total scam-related reviews collected : 249722 <br>
These reviews were grouped across 100 dating apps, sorted by increasing number of scam-related reviews per app.

**Results**
AppName                     Scam Review Count
 Tinder           <br>               31,391
 Bumble            <br>              21,253
 OkCupid           <br>              17,112
 Zoosk              <br>             15,955
 Plenty of Fish      <br>            12,844

 2. Profile and Behavioral Characteristics
Used Keyword filtering on the the previously resulted dataset.
Six key scam-related characteristics were identified based on qualitative and keyword
based analysis of dating app user reviews:
 • Generic Profile Pictures– Reports of profiles using overly attractive or stock-style
 images.
 • Claims of Living Abroad– Mentions of users who state they live or work in
 another country.
 • Inconsistent Profile Information– Comments highlighting mismatched details
 between profile descriptions and actual conversation.
 • Pushing Investment Opportunities– Reviews noting that a user persistently
 promoted financial schemes or trading.
 • Shifting Conversations to Off-Platform Channels– Observations that the user
 insisted on moving to WhatsApp, Telegram, etc.
 • Avoiding Video Calls or In-Person Meetings– Complaints about users who
 repeatedly made excuses to avoid face-to-face communication.

**Results**
• Generic Profile Pictures (7)
The apps that have the most mentions for these features are Once (2 mentions), Tinder (1 mention), Bumble(1 mention), Badoo (1 mention), Happn (1 mention), and Plenty Of Fish (1 mention).
• Claims of Living Abroad (15)
OkCupid(4 mentions),DilMil(2 mentions), where Once, Bumble, Tinder, Jaumo, Scruff, eHarmony, The Inner Circle each have 1 mention. 
• Inconsistent Profile Information
Total Inconsistent Profile Information Mentions Count: 27570
AppName                   Inconsistent Profile Mentions Count
 Tinder                              4,305
 Plenty Of Fish                      2,810
 OkCupid                             1,824
 Hinge                               1,691
 Zoosk                               1,416
 • Pushing Investment Opportunities (1030)
 AppName                       Mentions of Investments
 Tantan                              226
 Tinder                              210
 Plenty Of Fish                      79
 Hinge                               63
 Happn                               48
 • Shifting Conversations to Off-Platform Channels (29)
 Dating app Once has reported the highest number of this scam, which is 5 people mentioned about this, followed by OkCupid, Tantan, Bumble with 2 mentions. Other   apps such as Taimi, Date My Age, Grindr, Yoomee, Teamo, Vibe, Amolatina have 1 mention each.
 • Avoiding Video Calls or In-Person Meetings (2)
This behavioral trait was less frequently mentioned than other scam indicators but still surfaced in reviews from a few major platforms like Tantan and Bumble. 

 AppName                       Total Mentions (All6RedFlagsCombined)
 Tinder                                  4,517
 OkCupid                                 1,862
 Zoosk                                   1,437
 Bumble                                  1,606
 Hinge                                   1,757

3. Timing Patterns
Define Keywords for Timing & Escalation
Grouped into Quick Escalation, Delayed Escalation and No Mention

**Results**
 Escalation Categories                   Reviews Analyzed
 Quick Escalation                             222
 Delayed Escalation Mentions                  164
 No Mention                                   249,336
 Overall Escalation Ratio                     50.21

app_name	delayed_escalation	no_mention	quick_escalation
Tinder	        26	             31321	        44
Bumble          19	             21197	        37
Okcupid	        16	             17069	        27

4. Platforms Linked in Reviews
Grouped into financial platforms and communication platforms

**Results**
Platform Type           Total Mentions
Crypto Wallets                2
Investment Sites              12
Suspicious Links              58
WhatsApp                      23

app_name	crypto_wallets	investment_sites	suspicious_links	whatsapp
Tinder	        0	              5	                  4	           2
PlentyOfFish	  0	              2	                  2	           3
MeetMe	        0	              0	                  5	           0

5. Emotional and Financial Impacts
Calculates the financial and emotional harm
Uses keyword filtering

**Results**
Total financial Loss mentioned: 276
Total emotional harm mentioned: 177

AppName      Financial Loss Mention 
Tinder          71
Bumble          40
OkCupid         21


AppName       Emotional Harm Mentions 
 Tinder          44
 Bumble          33
 OkCupid         17

6. App-Specific Trends
Discusses Complaints about scam detection and User Suggestions for Safety Improvements

**Results**
Complaints about scam detection (8532)
User Suggestions for Safety Improvements (243)
Rank	 App Name	 Poor Detection	 Safety Suggestions	
1	    Tinder	        1,620	          55	
2	    PlentyOfFish	  851	            7	
3	    Once	          506	            1	
4	    Okcupid	       503	            6	
5	    Bumble	        433	            49	

7. Low Score Indicators
Reviews with a “score” field of 1 or 2 are more likely to mention dissatisfaction or scams. 

**Results**
 Score = 1       158,798 (95.36%)
 Score = 2       7,731 (4.64%)

 8. High “ThumbsUp” Count
Reviews with a large number of likes or thumbs up might highlight widespread issues, including scams. 

**Results**
 App                    ThumbsUpCount
 Bumble                    2,267
 Zoosk                     2,247
 Tinder                    1,871
 OkCupid                   1,706

 9. Response from Developers
Check the “replyContent” field for any official responses that acknowledge scams or fraudulent activity.
AppName      Response Count
 Bumble          3394
 Tinder          2237
 Tantan          1448
 Waplog          1297



## Social Media Platforms
To enrich the understanding of pig butchering scams beyond app store reviews, data was collected from Reddit, Instagram, and Twitter (X). The following scam-related scenarios were extracted using rule-based keyword filtering, applied to the content field of each post or comment:
1. Scammer Personas
2. Common Tactics by Scammers
4. Duration of Interaction
5. Countries with Most Scam Reports
6. Financial Loss Incurred
7. Dating App Analysis

After labeling the above scenarios, associated dating app names were extracted from each post (where available) to map scam reports back to specific platforms.
Posts that discuss scam experiences not matching any of the predefined keyword-based heuristics but still relevant to the broader context are categorised to "Other". Posts that do not provide sufficient context or do not contain recognizable keywords related to scams, tactics, losses, or app mentions  are categorised to "Unknown".

Results:
[Social Media Count](https://docs.google.com/spreadsheets/d/1VnSGZurTh2rxqB3xIeeg1QAnYYXezteyVVZ0qS7XuVI/edit?usp=sharing)

# Public Dataset
[Public Dataset Results](https://docs.google.com/spreadsheets/d/1_DDtXt-oNUFR8MkBBvxaI7PFHQb97AGdy9864VK-8oQ/edit?usp=sharing)






























