---
date: "2016-04-27T00:00:00Z"
external_link: ""
image:
  caption: Photo by rawpixel on Unsplash
  focal_point: Smart
links:
- icon: twitter
  icon_pack: fab
  name: Follow
  url: https://twitter.com/TheGuptaGuy
#slides: MSSEDA
summary: The idea is to develop a customisable survey system which is userfriendly, portable and can be used for wide-ranging applications.
tags:
- Python
- Data Visualization
title: Modular Survey System with Data Analytics

url_code: ""
url_pdf: https://github.com/neonflux56/Project_MSSDA/blob/master/MSSDA.pdf
url_slides: https://github.com/neonflux56/Project_MSSDA/blob/master/MSSEDA.pdf
url_video: ""
---


This project undertakes this issue regarding the data conundrum to come out with a better solution to data management. The idea is to develop a customisable survey system which is userfriendly, portable and can be used for wide-ranging applications. Our project takes this up a notch by adding the current trends in technology like security and analytics with effective implementation. The deployment of the device involves a predefined set of steps, which remains the same for any task its being programmed for. This can be shown in the flowchart below:

![](/MSSDA/index_files/Screenshot 2016-11-23 10.56.02.png)

The applications of this device in its respective field is potentially limitless. It integrates the functionalities of all its counterparts into a single, portable device. Some of the everyday applications are mentioned below:

1. Enumeration and census - provide an insight into the current status of related parameters and serves as the basis of constructing, planning, forecasts. It is also an essential part for a democratic process as it enables the citizens to examine the decisions made by the government and the local authorities and decide their effectiveness. But every enumeration process comes with an inherent time gap between its iterations, during which the corresponding devices remain idle. With the adoption of the proposed device, a single device can be configured to be used with any enumeration platforms and hence mitigating the idle time.

2. Polling - The most strategically precise move before taking a decision affecting the masses, is to take a poll of the opinions. The contents of such a poll are usually diverse, all of which can be configured on our device, leading a step closer towards an efficient system. In this opinionated world, the system offers everyone a chance to voice their ideas and opinions. This is the fundamental concept of the democracy that we live in.

3. Customized Data Entry - Camera module, fingerprint scanner and the included hex keypad module can be configured to form a basic data acquiring device, that can easily be appreciated for its convenient multipurpose in Aadhaar office, Passport centres, RTOs etc. Any layman can understand the operation of the system and this would enable easy customization of the system providing multivariate surveys for everyone to interpret and understand.

4. Prediction - Another important application to the proposed concept is the prediction model developed. Prediction is an essential part in various fields of study which help preparing for future consequences. The data collected from the survey is subjected to machine learning algorithms to predict using a probabilistic approach as to what the output can be provided the same features.


The implementation of machine learning algorithm multivariate linear regression to determine the probabilistic output is one of the major applications of the proposed system. The data obtained is in the .csv file form which is further imported by python script to perform the function. The python script reads the file from the SD card reader and classifies the data as parameters for all of the columns except the last column of data which is the main end question containing the affirmative and negative class. This applies a multivariate regression classifier (logistic regression) on this data to analyze the probabilistic output for a test data. The input for the test data is taken when the python script is run and the user answers the same parameter questions displayed on the Terminal. The input is then used in the classifies as test data and the survey data taken as the training data.

The main perspective of this project was to develop a product similar to the EVMs currently in use, but with enhanced security, portability and most importantly, practicality. This was accomplished by making the product completely customizable, enabling the user to configure the device to meet any requirements. Data privacy and security was enhanced by many folds through data encryption and multi layer authentication. The polling scenario considered here returned high levels of accuracy and precision, which only increased with the size of the dataset processed.Device configured to register votes performed better, more efficiently than the existing purpose made devices. Analysis and representation of the data conveyed the progress and final outcome of the event in a simple and precise manner.
