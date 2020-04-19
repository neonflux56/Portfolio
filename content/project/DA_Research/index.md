---
date: "2017-04-01T00:00:00Z"
external_link: ""
image:
  caption: Photo-rawpixel
  focal_point: Smart
links:
- icon: twitter
  icon_pack: fab
  name: Follow
  url: https://twitter.com/TheGuptaGuy
#slides: MSSEDA
summary: Developing a customisable survey system which uses Logistic Regression to predict a categorical survey information.
tags:
- Python
- Data Visualization
title: Modular Survey System with Data Analytics

url_code: ""
url_pdf: https://github.com/neonflux56/Project_MSSDA/blob/master/MSSDA.pdf
url_slides: https://github.com/neonflux56/Project_MSSDA/blob/master/MSSEDA.pdf
url_video: ""
---

## Introduction

The concept of Modular Survey System is to design an extremely versatile hardware device to store survey results in an SD card and then apply visual and predictive analytics on the survey data collected. This project develops a customisable survey generator which is user-friendly, portable and can be used for a wide range of applications. The deployment of the device involves a predefined set of steps, which remains the same for any task its being programmed for. This can be shown in the flowchart below:

![](/project/MSSDA/index_files/Screenshot 2016-11-23 10.56.02.png)

The applications of this device in its respective field is potentially limitless. It integrates the functionalities of all its counterparts into a single, portable device. Some of the everyday applications are mentioned below:

1. Enumeration and census - provide an insight into the current status of related parameters and serves as the basis of constructing, planning, forecasts. It is also an essential part for a democratic process as it enables the citizens to examine the decisions made by the government and the local authorities and decide their effectiveness. But every enumeration process comes with an inherent time gap between its iterations, during which the corresponding devices remain idle. With the adoption of the proposed device, a single device can be configured to be used with any enumeration platforms and hence mitigating the idle time.

2. Polling - The most strategically precise move before taking a decision affecting the masses, is to take a poll of the opinions. The contents of such a poll are usually diverse, all of which can be configured on our device, leading a step closer towards an efficient system. In this opinionated world, the system offers everyone a chance to voice their ideas and opinions. This is the fundamental concept of the democracy that we live in.

3. Customized Data Entry - Camera module, fingerprint scanner and the included hex keypad module can be configured to form a basic data acquiring device, that can easily be appreciated for its convenient multipurpose in Aadhaar office, Passport centres, RTOs etc. Any layman can understand the operation of the system and this would enable easy customization of the system providing multivariate surveys for everyone to interpret and understand.

4. Prediction - Another important application to the proposed concept is the prediction model developed. Prediction is an essential part in various fields of study which help preparing for future consequences. The data collected from the survey is subjected to machine learning algorithms to predict using a probabilistic approach as to what the output can be provided the same features.

## Implementation

The implementation of multivariate linear regression ML algorithm to determine the probabilistic output is one of the major applications of the proposed system. The data obtained is in the .csv file form which is further imported by python script to perform the function. The python script reads the file from the SD card reader and classifies the data as parameters for all of the columns except the last column of data which is the main end question containing the affirmative and negative class. This applies a multivariate regression classifier (logistic regression) on this data to analyze the probabilistic output for a test data. The input for the test data is taken when the python script is run and the user answers the same parameter questions displayed on the Terminal. The input is then used in the classifies as test data and the survey data taken as the training data. Logistic Regression is a classification type to address the binary classification problem in our project. The output 0 is taken as the ’positive class’ and the output 1 is taken as the ’negative class’. The sigmoid function or logistic function is used which is represented by the following equations:

![](/project/MSSDA/index_files/Screenshot 2019-11-22 11.56.33.png)

The function g(z), shown here, maps any real number to the (0, 1) interval, making it useful for transforming an arbitrary-valued function into a function better suited for classification. For the parameter , the cost function is given below.

![](/project/MSSDA/index_files/Screenshot 2019-11-22 11.56.42.png)

To optimize the training dataset and to minimize the error, the cost function is used in the gradient descent process.

![](/project/MSSDA/index_files/Screenshot 2019-11-22 11.56.49.png)

![](/project/MSSDA/index_files/Screenshot 2019-11-22 11.54.02.png)

The polling scenario considered here returned high levels of accuracy and precision, which increased with the size of the dataset processed.

## Future Scope

Innovations are necessary to break the old practice to implement new technology with more advantages. Few more modules, newer and adaptable algorithms can be added to make the
Modular survey system effective and with more security. 

1. Data acquisition:
The device can be easily configured to acquire repetitive data, by interfacing it with generic data gathering attachments such as a fingerprint sensor, camera module, and a keyboard. This same setup, for example, can be used to collectpublic identification or registration of new recruits in a company.

2. Security enhancement:
Further improvement on the security end employs fingerprint authorization and encryption of the data stored locally. This two step authorization - RFiD and Biometric, ensures more security against data or device manipulation than any other commercial device.

3. Cloud integration:
With the security offered by encryption, cloud integration opens up a new horizon of applications. Real time data transfer and analysis can now be done. Several modules can be deployed in an area linked through the cloud, with centralized controlling and analysis. Loss of data due to physical damage to the device or memory device corruption is also avoided through cloud backup. To further ease the process of data transfer and storing, data compression technique such as LZW is adaptable for our requirements.

{{%alert%}}
Click [PDF](https://github.com/neonflux56/Project_MSSDA/blob/master/MSSDA.pdf) to view more details on this project.
{{%/alert%}}
