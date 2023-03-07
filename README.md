![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54) ![Jupyter Notebook](https://img.shields.io/badge/jupyter-%23FA0F00.svg?style=for-the-badge&logo=jupyter&logoColor=white) ![scikit-learn](https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=for-the-badge&logo=scikit-learn&logoColor=white) ![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white) ![NumPy](https://img.shields.io/badge/numpy-%23013243.svg?style=for-the-badge&logo=numpy&logoColor=white) ![Matplotlib](https://img.shields.io/badge/Matplotlib-%23ffffff.svg?style=for-the-badge&logo=Matplotlib&logoColor=black) ![Reddit](https://img.shields.io/badge/Reddit-%23FF4500.svg?style=for-the-badge&logo=Reddit&logoColor=white)

***Sections***
- Data Dictionary
- Data Scraping
- Data Engineering
- Modeling
- Problem Statement
- Executive Summary
- Conclusions

***Data Dictionary***
| Column Name        | Data Type | Description                                                                        |
|--------------------|-----------|------------------------------------------------------------------------------------|
| 'author_username'  | string    | The Reddit username of the poster                                                  |
| 'author_id'        | string    | The id assigned to the poster by Reddit                                            |
| 'post_text'        | string    | The text body of the Reddit post                                                   |
| 'post_title'       | string    | The title text of the Reddit post                                                  |
| 'neg_sentiment'    | float     | Negative sentiment score assigned by VADER                                         |
| 'pos_sentiment'    | float     | Positive sentiment score assigned by VADER                                         |
| 'neu_sentiment'    | float     | Neutral sentiment score assigned by VADER                                          |
| 'comp_sentiment'   | float     | Composite sentiment score assigned by VADER                                        |
| 'num_comments'     | int       | Number of comments on the Reddit post                                              |
| 'post_score'       | int       | Number of upvotes minus downvotes on the Reddit post                               |
| 'post_subreddit'   | int       | The subreddit the post originated from: 1 for ChangeMyView, 0 for UnpopularOpinion |
| [EVERYTHING ELSE]  | int       | Count vectorized words dervived from post_text and post_title                      |

***Data Scraping***
All queries for the data scraping process can be found in 'AllQueries.txt' in this folder. Subreddits scraped were ChangeMyView and UnpopularOpinion.

***Data Engineering***
Title and body of reddit posts were merged together, lemmatized, and vectorized. Common English stopwords were removed, as were additional stopwords of Author's choosing. Text was stripped of hyperlinks and of moderator addenda.

***Modeling***
Models were chosen for inferential power combined with enough predictive power to be taken seriously. Final choices were XGBoosted Decision Tree and Logistic Regression, optimized around the ROC AUC metric.

***Problem Statement***
- My (hypothetical) company is an advertising firm. Management has indicated that they would like to see how feasible it would be to insert astroturfers into opinion forums to generate positive public sentiment for our clientele’s products and negative public sentiment for opposing products.
- We have selected two popular opinion forums on the website Reddit.com: “Change my View” and “Unpopular Opinion.” Our goal is to analyze the words they use and what they talk about to form our conclusions.

***Executive Summary***

- [FAKE MEDIA GROUP] is one of the fastest growing companies on the market. You have original, interesting content all over your network. The problem is getting more users to keep that growth sustained.

- As you are well aware, it can be difficult to get into the advertising space. Many consumers will simply ignore an advertisement out of hand, and without careful study of psychological tricks and tactics none of your ad will remain in their head. You need a way to create brand awareness and positive sentiment without treading on consumers delicate (metaphorical) toes.

- The solution? Astroturf marketing. With the right training, and employee or chat bot can guide users toward your brand without their awareness that they are being advertised to. It's cheaper than buying airtime, can be picked up by real grassroots attention, and can be used to create negative public sentiment towards the competition. We can keep you informed on the latest trends in language and speech patterns on various fora so that you can do the advertising your company needs.

- We have multiple machine learning models ready to show you that describe exactly what makes an individual post on a particular forum look like the others around it. Through hours of testing and analysis, we can give you the tools to convince potential users that your advertisements are just normal forum posts.

- If you're ready, we'd love to take you on as our client. [FAKE MEDIA GROUP] represents a load of loveable media that we want to see flourish in today's market. With the right tools in your hands, we're sure that you can make that happen.

***Conclusions***
- Overall, it appears that Unpopular Opinion is a good target forum for a demo of astroturf marketing. Denigrating things is very common there, which would make the goal of generating negative public sentiment for our clientele’s competing products simple to add to the mix. Additionally, inserting a promotion for our clientele's product in the text statement of a reddit post would not appear to be amiss.
- Change my View does not appear to have many characteristics that would make it a useful staging ground for a demo. There is a focus on geopolitical or societal issues, with little chance of making a stand for a clientele’s product without being seen as clear advertising.
- I propose the company move forward with a demo for our clients on the Unpopular Opinion subreddit.
