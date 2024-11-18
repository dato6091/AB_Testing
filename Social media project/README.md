# Introduction

Conduct an A/B Testing on a project for a social media company. In the app, users can upload pictures and interact with other users liking the content and leaving comments. 
The business model of the company is based on ads, so not only they show posts of users but also they are showing their advertisements from different brands. However, this business model is not particularly successful because the ads are not particularly relevant to the users that see them. Recently the company got a partnership request from company B, company B wants to show sponsored posts on the feed of the website so the users can see those posts more often. Those posts will have an affiliate link which, if a purchase is made, our company would get a revenue attribution (a small percentage of the sale). 

Here, I will be focusing in determining if the users are liking this new feature or not. I will do this by monitoring the following **success metrics**:
* **Daily Active Users (DAU):** To make sure users come back. I'm considering the amounts of times a user opens the app per day. 
* **Click-Through Rate (CTR):** To compare if the new type of sponsored links raise more interest than the previous sponsored posts. It is calculated as the division of the number of clicks of a user through all the ads the user has seen.

For that, I'll be using two datasets:
* Activity dataset: with the following structure:
  * **userid:** unique identifier for each user.
  * **dt:** date of the log
  * **activity_level:** number of times the user opened the app that day.
* CTR dataset:
  * **userid:** unique identifier for each user.
  * **dt:** date of the log
  * **ctr:** click-through rate 
