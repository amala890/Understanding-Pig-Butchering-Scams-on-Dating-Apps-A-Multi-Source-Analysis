# Understanding Pig Butchering Scams Targeting Dating App Users: A Multi-Source Analysis


# Google Play Store Reviews
Collected review data from 100 dating apps 

Used rule-based keyword filtering

Used google_play_scraper library in python using app_id

CSV files are named using corresponding dating app names

Collected reviewId	userName	userImage	content	score	thumbsUp	appVersion	at	replyContent	repliedAt	scam_related	is_scam	sentiment	app_name	thumbsUpCount	reviewCreatedVersion


## Analysis

 Divided into 9 main sections:
1. Scam Indicators in User Reviews <br>
User reviews were grouped based on the presence of scam-related keywords.
This serves as the ground truth data for further analysis. <br>
Total scam-related reviews collected : 249722 <br>
These reviews were grouped across 100 dating apps, sorted by increasing number of scam-related reviews per app.

**Results**


| App Name        | Scam Review Count |
|----------------|-------------------|
| Tinder          | 31,391            |
| Bumble          | 21,253            |
| OkCupid         | 17,112            |
| Zoosk           | 15,955            |
| Plenty of Fish  | 12,844            |


 2. Profile and Behavioral Characteristics <br>
Used Keyword filtering on the the previously resulted dataset.

Based on qualitative insights and keyword-based analysis of user reviews, six recurring characteristics associated with pig butchering scams were identified:

1. Generic or Unrealistic Profile Pictures  
   Users reported encountering profiles with overly attractive, professional, or stock-style images—often reused across different apps.

2. Claims of Living or Working Abroad
   Many scammers claimed to be temporarily or permanently located in a different country, making in-person meetings impractical.

3. Inconsistent Profile Information  
   Reviewers noted discrepancies between a user’s profile description and the content of their messages, suggesting fake or copied profiles.

4. Persistent Promotion of Investment Opportunities  
   Several reviews described users who gradually shifted conversations toward cryptocurrency, stock trading, or other financial schemes.

5. Shifting Communication to External Platforms 
   A common tactic involved urging victims to move the conversation from the dating app to platforms like WhatsApp, Telegram, or Line—reducing platform oversight.

6. Avoidance of Video Calls or In-Person Meetings 
   Users frequently reported that scammers made repeated excuses to avoid video calls or real-life meetings, maintaining an anonymous and untraceable presence.


**Results**
## • Generic Profile Pictures (7 Mentions)
Reports of overly attractive or stock-style profile photos.

**Apps where this was mentioned:**
- **Once** – 2 mentions  
- **Tinder** – 1 mention  
- **Bumble** – 1 mention  
- **Badoo** – 1 mention  
- **Happn** – 1 mention  
- **Plenty of Fish** – 1 mention

---

## • Claims of Living Abroad (15 Mentions)
Scammer profiles often state they live or work abroad to justify avoiding in-person meetings.

**Apps where this was mentioned:**
- **OkCupid** – 4 mentions  
- **DilMil** – 2 mentions  
- **Once**, **Bumble**, **Tinder**, **Jaumo**, **Scruff**, **eHarmony**, **The Inner Circle** – 1 mention each

---

## • Inconsistent Profile Information (27,570 Mentions)
Reviews highlighting mismatches between user bios and actual behavior or conversations.

**Top apps with the highest mentions:**

| App Name        | Inconsistent Profile Mentions |
|-----------------|-------------------------------|
| Tinder          | 4,305                         |
| Plenty of Fish  | 2,810                         |
| OkCupid         | 1,824                         |
| Hinge           | 1,691                         |
| Zoosk           | 1,416                         |

---

## • Pushing Investment Opportunities (1,030 Mentions)
Scammer profiles promoting crypto, forex, or other dubious financial schemes.

**Top apps with the highest mentions:**

| App Name        | Investment-Related Mentions |
|-----------------|-----------------------------|
| Tantan          | 226                         |
| Tinder          | 210                         |
| Plenty of Fish  | 79                          |
| Hinge           | 63                          |
| Happn           | 48                          |

---

## • Shifting Conversations to Off-Platform Channels (29 Mentions)
Scammers urging users to move chats to WhatsApp, Telegram, etc., to avoid platform moderation.

**Apps where this was mentioned:**
- **Once** – 5 mentions  
- **OkCupid**, **Tantan**, **Bumble** – 2 mentions each  
- **Taimi**, **Date My Age**, **Grindr**, **Yoomee**, **Teamo**, **Vibe**, **Amolatina** – 1 mention each

# 🧠 Behavioral Traits and Timing Patterns in Pig Butchering Scams

In addition to previously identified scam indicators, further analysis uncovered a less frequent but relevant behavioral trait: **Avoiding Video Calls or In-Person Meetings**. Timing patterns in scam progression were also studied to understand how quickly scammers escalate interactions.

---

## • Avoiding Video Calls or In-Person Meetings (2 Mentions)
This behavioral trait was mentioned less frequently than others, but still appeared in reviews, suggesting a known avoidance tactic by scammers.

**Apps where this was mentioned:**
- **Tantan**
- **Bumble**

---

## 🔢 Combined Scam Red Flags (All Six Characteristics)

Total mentions across all six scam indicators by app:

| App Name   | Total Mentions (All Red Flags Combined) |
|------------|------------------------------------------|
| Tinder     | 4,517                                    |
| OkCupid    | 1,862                                    |
| Zoosk      | 1,437                                    |
| Bumble     | 1,606                                    |
| Hinge      | 1,757                                    |

---

# ⏳ Timing Patterns of Scam Escalation

Scammer interaction patterns were categorized into **Quick Escalation**, **Delayed Escalation**, and **No Mention** of escalation timing. This helps in understanding how rapidly scammers shift to manipulation and financial discussions.

### **Results: Escalation Categories**

| Escalation Category    | Reviews Analyzed |
|------------------------|------------------|
| Quick Escalation       | 222              |
| Delayed Escalation     | 164              |
| No Mention             | 249,336          |
| **Overall Escalation Ratio** | **50.21**       |

---

### Escalation Mentions by App

| App Name   | Delayed Escalation | No Mention | Quick Escalation |
|------------|--------------------|------------|------------------|
| Tinder     | 26                 | 31,321     | 44               |
| Bumble     | 19                 | 21,197     | 37               |
| OkCupid    | 16                 | 17,069     | 27               |

---

These insights reveal how scammers operate differently across platforms, both in behavioral red flags and in the timing of their manipulation attempts. Understanding these trends aids in creating detection mechanisms and preventive strategies within dating apps.


# 🔗 4. Platforms Linked in Reviews

Reviews frequently referenced external platforms, which were grouped into two main categories: **financial platforms** and **communication platforms**. These external services are often used by scammers to further manipulate or defraud users.

---

## **Results**

| Platform Type       | Total Mentions |
|---------------------|----------------|
| Crypto Wallets      | 2              |
| Investment Sites    | 12             |
| Suspicious Links    | 58             |
| WhatsApp            | 23             |

---

## Mentions by App

| App Name       | Crypto Wallets | Investment Sites | Suspicious Links | WhatsApp |
|----------------|----------------|------------------|-------------------|----------|
| Tinder         | 0              | 5                | 4                 | 2        |
| PlentyOfFish   | 0              | 2                | 2                 | 3        |
| MeetMe         | 0              | 0                | 5                 | 0        |

---

These references suggest a strong connection between scam attempts and off-platform communications or shady financial sites. Integration of link detection and warnings may help mitigate these risks.


# 💔 5. Emotional and Financial Impacts

This section captures the **emotional** and **financial** harm experienced by users based on keyword-driven filtering of review texts. Emotional harm includes phrases related to heartbreak, being misled, or feeling betrayed, while financial harm includes explicit mentions of money lost or stolen.

---

## **Results**

| Impact Type        | Total Mentions |
|--------------------|----------------|
| Financial Loss     | 276            |
| Emotional Harm     | 177            |

---

## Financial Loss Mentions by App

| App Name   | Financial Loss Mentions |
|------------|--------------------------|
| Tinder     | 71                       |
| Bumble     | 40                       |
| OkCupid    | 21                       |

---

## Emotional Harm Mentions by App

| App Name   | Emotional Harm Mentions |
|------------|--------------------------|
| Tinder     | 44                       |
| Bumble     | 33                       |
| OkCupid    | 17                       |

---

These findings emphasize the real-world consequences of pig butchering scams — not just financial losses, but significant emotional distress for users. Dating platforms can benefit from incorporating emotional sentiment analysis and fraud-reporting tools.


# 📊 6. App-Specific Trends

This section analyzes user complaints about **poor scam detection** mechanisms in dating apps and reviews suggesting **safety improvements**. Such feedback highlights the demand for stronger anti-scam systems.

---

## **Results**

- Total Complaints about Scam Detection: **8,532**
- Total User Suggestions for Safety Improvements: **243**

| Rank | App Name      | Poor Detection | Safety Suggestions |
|------|---------------|----------------|--------------------|
| 1    | Tinder        | 1,620          | 55                 |
| 2    | PlentyOfFish  | 851            | 7                  |
| 3    | Once          | 506            | 1                  |
| 4    | OkCupid       | 503            | 6                  |
| 5    | Bumble        | 433            | 49                 |

---

These trends underline the need for dating platforms to invest in **scam reporting systems**, **profile verification**, and **user education** features.

---

# ⭐ 7. Low Score Indicators

A significant portion of scam-related or dissatisfaction-driven reviews are marked with **low star ratings**, predominantly **1 or 2 stars**.

---

## **Results**

| Review Score | Number of Reviews | Percentage   |
|--------------|-------------------|--------------|
| 1 Star       | 158,798           | 95.36%       |
| 2 Stars      | 7,731             | 4.64%        |

---

These indicators show that **low-rated reviews are highly correlated** with scam reports and platform dissatisfaction. Filtering reviews by low scores can be an effective strategy to prioritize moderation and scam detection.


 # 👍 8. High “ThumbsUp” Count

User reviews with high **ThumbsUp** or "likes" reflect **widespread agreement or concern**, often signaling systemic issues such as scams. These reviews are likely to be more **visible and trusted** by the user community.

---

## **Results**

| App Name   | Total ThumbsUp Count |
|------------|----------------------|
| Bumble     | 2,267                |
| Zoosk      | 2,247                |
| Tinder     | 1,871                |
| OkCupid    | 1,706                |

---

These numbers show that **popular dating apps** have numerous highly upvoted reviews, potentially raising red flags about **shared negative experiences** or **fraudulent behavior** encountered by multiple users.

---

# 🛠️ 9. Response from Developers

This section inspects the `replyContent` field to evaluate how frequently developers respond to reviews, especially those **mentioning scams**. Proactive responses can help rebuild **user trust** and indicate that the platform acknowledges scam-related concerns.

---

## **Results**

| App Name   | Developer Response Count |
|------------|---------------------------|
| Bumble     | 3,394                     |
| Tinder     | 2,237                     |
| Tantan     | 1,448                     |
| Waplog     | 1,297                     |

---

These results suggest that **some platforms are actively engaging** with users through replies. However, **the quality and relevance** of these replies would need further inspection to determine if they effectively address scam-related issues.

[Google Play Store Results](https://docs.google.com/spreadsheets/d/1F_fKnJPWhuJjJUiX6J8HUmy67MvxfGvHm_3dNucsKa4/edit?usp=sharing)

## Public Dataset
Apps: Tinder, Bumble, Plenty of Fish, Hinge
Collected reviewId	userName	userImage	content	score	thumbsUpCount	reviewCreatedVersion	at	replyContent	repliedAt	appVersion

# Analysis

[Public Dataset Results](https://docs.google.com/spreadsheets/d/1_DDtXt-oNUFR8MkBBvxaI7PFHQb97AGdy9864VK-8oQ/edit?usp=sharing)


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































