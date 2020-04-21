---
date: "2020-02-01T00:00:00Z"
external_link: ""
image:
  caption: 
  focal_point: Smart
links:
- icon: twitter
  icon_pack: fab
  name: Follow
  url: https://twitter.com/TheGuptaGuy
#slides: TextCraft
summary: A dynamic user-friendly interface for analysis of topics and sentiments in text documents
tags:
- R
- Data Visualization
title: TextCraft - An asset for text analytics

url_code: ""
url_pdf: 
url_slides: 
url_video: ""
---



## Executive Summary

<div style="text-align:justify"><span>
TextCraft delivers a framework with user-friendly interface to analyze and visualize any text corpus making it a versatile asset for unstructured text analysis. TextCraft is unique in the way that it is scalable, robust and easy to interpret, thus making it seamless even for user having minimal background in dealing with text. It uses various natural language processing algorithms in the backend, which are easily configurable, producing accurately tailored results. The content is very visual and dynamic for any user to understand the effective topics and sentiments in a text corpus. One of the many possible use cases for this tool could be for business owners to potentially make business strategies and decisions based on customer review sentiment captured by this web application.
</span></div>


## Introduction

<div style="text-align:justify"><span>
Like the commonly used machine learning quote goes, "Treat your data like a product, not as a project", this web application was envisioned as an asset for users with little or no background understanding of dealing with text data. The dynamic nature of this app allows for a user to perform text analytics, mainly topic and sentiment analysis, on any text data.
</span></div>

<p align="center" style="font-family:Georgia;font-size:75%;">
  <img width="650" height="550" src="/project/TextCraft/index_files/pic2.png">
  <em></em>
</p>

<div style="text-align:justify"><span>
The app works in three stages:
</span></div>

<br>

### 1. Load Stage

<div style="text-align:justify"><span>
The user gets to upload data in a csv file or hit Application Programming Interfaces(APIs) to fetch data into the tool. The user gets to see a preview of the collected data and decide the field that becomes the response and the field on which text models are applied.
</span></div>


### 2. Process Stage


<div style="text-align:justify"><span>
This is the stage where data cleaning and modelling takes place. The user gets a glimpse of general summaries of the dataset like the TF-IDF scores, frequency counts etc. The user gets to annotate the word collection accordingly. The tool also allows the user to try different configuration parameters for running various models. 
</span></div>


### 3. Insights Stage


<div style="text-align:justify"><span>
This stage displays a set of tailored charts and visuals corresponding to the configured outputs for the user to make sense of the data. The plots are grouped by each response field categories making the analysis more granular and comprehensive.
</span></div>


<p align="center" style="font-family:Georgia;font-size:75%;">
  <img width="600" height=550" src="/project/TextCraft/index_files/pic3.png">
  <em></em>
</p>


## Dashboard Design and Implementation


### Home Tab

<div style="text-align:justify"><span>
The front end interface is also laid out in the three-stage fashion of the app's architecture for ease of interpretation. The first tab is the home page which comprises of the introduction to the tool and the instructions to use it.
</span></div>

<p align="center" style="font-family:Georgia;font-size:75%;">
  <img width="900" height="850" src="/project/TextCraft/index_files/pic4.png">
  <em>Home: Landing page of the app</em>
</p>


### Load Data Tab

<div style="text-align:justify"><span>
Under this tab, the user gets to upload a CSV file with the data or enter an API link which provides access to a json scipt of data. The json from API is automatically converted into a dataframe in R, The fetched data is previewed on the lower part of the screen. The user then decides with field becomes the text corpus and which field would categorize the text as the response variable. Though, the user can select a single response field at a time, this field can be changed to redo the analysis. For reference, let's load a dataset containing the reviews for cirque-du-soleil shows in held in Vegas. The show names becomes the response and the reviews become the text corpus.
</span></div>

<p align="center" style="font-family:Georgia;font-size:75%;">
  <img width="900" height="850" src="/project/TextCraft/index_files/pic5.png">
  <em>Load Data: The user uploads a CSV file or enters API link</em>
</p>


### Process Data Tab

<div style="text-align:justify"><span>
This is the main tab where text is analyzed and models are initiated. At the top of the screen, the user gets to see the top 10 words with their word counts, TF-IDF scores and the suggested words to remove. Suggested words to remove are defined by a collection of conditional statements, depending on the word frequency, their TF-IDF score and their correlation with the title of the responses. The Annotation part allows the user to select the words to remove or enter a specific word. The user also has the ability to reset the changes to the original form. 
</span></div>

<p align="center" style="font-family:Georgia;font-size:75%;">
  <img width="900" height="850" src="/project/TextCraft/index_files/pic6.png">
  <em>Process Data: Words selected and entered for annotation</em>
</p>

<p align="center" style="font-family:Georgia;font-size:75%;">
  <img width="900" height="850" src="/project/TextCraft/index_files/pic7.png">
  <em>Process Data: Selected words are removed from corpus</em>
</p>

<div style="text-align:justify"><span>
Once the redundant words are removed from the corpus, the app runs two main models - topic and sentiment analysis. For the topic analysis part, Latent Dirichlect Allocation (LDA) model is used in an unsupervised fashion to identify the most matching words for a particular topic. The top TF-IDF scores with respect to each response category is also obtained in the backend. The user is allowed to change the model configuration parameters like the seed value, number of topics, number of words per topic etc. The user also can perform the text tokenization in a unigram or bigram method, which basically refers to the number of words per token. For the chosen example, let's choose unigram modeling showing top 7 words and running LDA for 4 unsupervised topics. Clicking on 'Analyze Document Corpus' initiates the process.
</span></div>

<p align="center" style="font-family:Georgia;font-size:75%;">
  <img width="900" height="850" src="/project/TextCraft/index_files/pic8.png">
  <em>Process Data: LDA model configuration options</em>
</p>


### Get Insights Tab

<div style="text-align:justify"><span>
The model takes a little while to run before producing the analysis results. The Get Insights tab comprises of two sub-tabs topic and sentiment analysis. The topic analysis shows two main plots. The first plot describes the grouped categories in the response field and the top words corresponding to that category. The bottom chart is the output from the unsupervised LDA model associating/clustering the words in each of the topics. The number of topics and the number of words displayed per topic is fed under the configuration part in the Process Data tab.
</span></div>

<p align="center" style="font-family:Georgia;font-size:75%;">
  <img width="900" height="850" src="/project/TextCraft/index_files/pic9.png">
  <em>Get Insights: Top words for each response/show </em>
</p>


<p align="center" style="font-family:Georgia;font-size:75%;">
  <img width="900" height="850" src="/project/TextCraft/index_files/pic10.png">
  <em>Get Insights: Unsupervised topic analysis from LDA model</em>
</p>

<div style="text-align:justify"><span>
The sentiment analysis sub-tab comprises of all the sentiment and emotion distribution in the entire corpus and also grouped by each response category. The package 'sentimentr' from cran was used for this part of analysis. NRC Lexicon for identifying the emotion of a word was used to associate the review context with emotion. The plots below show the distribution of emotion in the entire corpus and the emotion for a single show name.
</span></div>

<p align="center" style="font-family:Georgia;font-size:75%;">
  <img width="900" height="850" src="/project/TextCraft/index_files/pic11.png">
  <em>Get Insights: Emotion distribution across entire corpus</em>
</p>

<p align="center" style="font-family:Georgia;font-size:75%;">
  <img width="900" height="850" src="/project/TextCraft/index_files/pic16.png">
  <em>Get Insights: Emotion distribution across the show - MJ One</em>
</p>

<div style="text-align:justify"><span>
A sentiment score was used to as a measure to identify the general sentiment. The score distribution was analysed at various levels. Tts mean and standard deviation was calculated per response group. Following plots show the results of this analysis.
</span></div>

<p align="center" style="font-family:Georgia;font-size:75%;">
  <img width="900" height="850" src="/project/TextCraft/index_files/pic12.png">
  <em>Get Insights: Average sentiment distribution for each response/show</em>
</p>

<p align="center" style="font-family:Georgia;font-size:75%;">
  <img width="900" height="850" src="/project/TextCraft/index_files/pic13.png">
  <em>Get Insights: Positive/negative distribution across entire corpus</em>
</p>

<p align="center" style="font-family:Georgia;font-size:75%;">
  <img width="900" height="850" src="/project/TextCraft/index_files/pic14.png">
  <em>Get Insights: Positive/negative distribution across each response</em>
</p>

<p align="center" style="font-family:Georgia;font-size:75%;">
  <img width="900" height="850" src="/project/TextCraft/index_files/pic15.png">
  <em>Get Insights: Statistical representation of sentiment score per response</em>
</p>




## References

- [http://www.tfidf.com/](http://www.tfidf.com/)

- [https://cran.r-project.org/web/packages/sentimentr/sentimentr.pdf](https://cran.r-project.org/web/packages/sentimentr/sentimentr.pdf) 

- [http://sentiment.nrc.ca/lexicons-for-research/](http://sentiment.nrc.ca/lexicons-for-research/) 

- [https://docs.rstudio.com/shinyapps.io/](https://docs.rstudio.com/shinyapps.io/) 


