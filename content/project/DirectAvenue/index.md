---
date: "2020-03-01T00:00:00Z"
external_link: ""
image:
  caption: TheDrum
  focal_point: Smart
links:
- icon: twitter
  icon_pack: fab
  name: Follow
  url: https://twitter.com/TheGuptaGuy
#slides: 
summary: Developed a Gradient Boosting regression model to predict the reach for unrated TV advertisements
tags:
- Python
title: GRP and Reach estimation for unrated TV ad-spots 

url_code: ""
url_pdf: ""
url_slides: ""
url_video: ""
---

<div style="text-align:justify"><span>
<p><b><i><u>Note:</u> This project was implemented in collaboration with the data-driven media agency DirectAvenue, Carlsbad, CA. Non-Disclosure Agreement(NDA) signed prevents me from releasing the codebase or any more details on the project.
 </i></b></p>
</span></div>

## Executive Summary
<br>
<div style="text-align:justify"><span>
In the TV advertisement industry, businesses seek to maximise the consumer reach by airing ads at optimal investment levels. Neilson Corporation rates TV ad-spots and provides estimates of the consumer reach with metrics like Gross Rating Points(GRP) or Reach Percentage. DirectAvenue is a data-driven media agency which collaborates with businesses to optimize their advertisement investments. In this project, the deliverable was to predict the consumer reach for unrated TV ad-spots using the data from Nielson-rated spots. A gradient boosting regression model using python was developed with factors like location, spot cost, airing station, airing time of the day and day of the week. Key metrics were identified and the model was deployed for DirectAvenue to make valid recommendations to their clients for optimizing media investments.
</span></div>

## Project Overview
<br>
<div style="text-align:justify"><span>
With the advent of advertising through mass media channels, some of the biggest drivers of profit have been T.V. spots, or individual advertisements seen on T.V. channels. Top companies bid for slots ranging from 15 seconds to 1 minute in length. One of the more popularized examples of T.V. spots are Super Bowl Ads, which are advertisements that air specifically during the Super Bowl in early February. Companies bid for slots that, according to CNBC, cost about $175,000 per second in an attempt to create the most provocative advertisement.
</span></div>
<br>
<div style="text-align:justify"><span>
There are different metrics that can be used to measure the success of a T.V. spot, the most prominent being ‘Impressions/Reach’ and ‘GRP’. These metrics are closely related in definition, as we can define impressions/reach as the amount of “eyeballs” that have seen each spot and GRP as the percentage of the U.S. T.V. audience that is targeted by a T.V. spot. GRP is calculated from a T.V. channels viewership, but we can directly tie a channel’s GRP to a T.V. spot’s GRP. We can separate reach from GRP as reach can be used to extract unique viewership from GRP, which includes duplicate viewers. The Nielsen Corporation is an advertising market research agency that measures GRP and reach of advertisements. Nielsen rates a certain number of U.S. T.V. channels, and T.V. spots shown on these “rated” channels receive distinct GRP and reach statistics.
</span></div>
<br>
<div style="text-align:justify"><span>
On channels not rated by Nielsen, there is no official source for GRP and reach information. While we do not have spot metrics for unrated channels, we can extract attributes regarding those channels, as well as spots shown on both unrated and rated channels, such as the length of the spot, cost of the spot, time aired, etc. We can use attributes for channels that have been rated by Nielsen to train a statistical model, and using this model, we have the unique opportunity to forecast the rating of spots shown on channels not rated by Nielsen. The whole objective of this project was to estimate the reach of a TV spot using an ML pipeline so that DirectAvenue’s customers could better return on their marketing investments.
</span></div>
<br>
<div style="text-align:justify"><span>
During the course of this project, aside from cleaning the data we faced certain unique challenges. The GRP feature was on a relative scale at the ‘station’ level and depended on the audience size under the station it was aired. This was converted to an absolute scale for consistency and this would result as our response feature in our model. We trained multiple tree based regression models using scikit-learn python on 70% of the training data and testing the performance of the model on 30% validation set. The metric used to measure the performance was the root mean square error (RMSE). The model was tuned with 3-fold cross-validation and hyper parameter tuning. XGBoost resulted in the lowest RMSE value and was used to make the final predictions of audience size. The reach measure was estimated using these predictions and key rating indicators were identified.
</span></div>




