# Description

This is the repository for the final project of the course **Applied Forecasting**, 
offered by the University of Nicosia and the Institute for the Future. In this repository we will document the whole project work, the results as also any related information.

## About this course

Forecasts are needed for setting up inventory levels, constructing production or delivery
schedules and in all types of planning: from budgeting to strategic. This course covers all
types of forecasts and offers concrete information to business executives on how to improve the accuracy of their predictions. Such information is based on the findings of the M Competitions organized by Spyros Makridakis, the initiator of the course.

## Course Outline

- The Basis of Forecasting
- Data for Forecasting
- Statistical Methods
- Explanatory and ML/Methods
- Commercial Forecasting Packages
- Forecasting Applications

## Spiros Makridakis

Dr Spyros Makridakis is a Professor at the University of Nicosia, the director of the Institute For the
Future (IFF) and an Emeritus Professor at INSEAD.
He has authored, or co-authored, twenty-two
books and more than 250 articles.

He was the founding editor-in-chief of the Journal of Forecasting and
the International Journal of Forecasting and is the organizer of the M
(Makridakis) Competitions

# About the final project

## Project Requirements

The final project is outlined bellow, but the general idea is to select a data-set and perform forecasting competition, applying both machine-learning methodologies as well as traditional statistical. We will firstly massage the data-set to improve the accuracy of the forecasting techniques, then we will apply the techniques and finally we will draw a conclusion on what methodology was proven superior and what business insight can be extracted.

After analyzing the dataset you will have to submit a report that includes the following:
   - A short description of the problem being solved. You should briefly state what the data represents, what the main objective of the application considered is, why its results are important, and what are the main parameters that should be taken into consideration for solving it.
   - A presentation of the dataset used. You should present the series you wish to predict and the external variables that will be considered to do so, commenting on their correlation (e.g., correlation matrix and scatter plots).
   - A presentation of the data cleansing techniques you applied: G iven that the dataset involves some missing, as well as extreme values, you should process the data before forecasting using appropriate techniques. Then, you should briefly present them.
   - Time series decomposition: You should examine the seasonal and trend patterns present at various frequencies, such as daily, weekly and monthly. Then, you should also present these results and make a brief comment.
   - Statistical forecasting methods: You should apply at least one statistical forecasting method for predicting the future values of the series for the upcoming time period. The selected method(s) should be clearly described (inputs, outputs, and
  parameters considered).
   - Machine Learning forecasting methods: You should apply at least one ML forecasting
  method for predicting the future values of the series for the upcoming week. The selected method(s) should be clearly described (inputs, outputs, and parameters considered).
   - An overview of your “forecasting competition”. Given that various forecasting methods may be appropriate for dealing with the problem being solved, you are expected to test your alternatives and report the expected accuracy of the methods you have developed, while commenting on your results to justify your final choice. Emphasis should be given to the metrics and processes used for performing this validation as objectively as possible. In order to perform this validation, you may use the last 168 observations of the dataset as outsample data, or apply a rolling-origin evaluation for even more indicative results.

## Use-case background

Although the course does provides a sample data-set, it is advised that we used data from our current companies (this is an executive training program after-all) and I am fortunate enough that I have been employed as a Product Analyst at [balena.io](https://balena.io) for the last two months. Thus, after some internal discussion, we identified a use-case that has two important characteristics:

1. It is a low-impact field, thus any mental bias that might effect the team due to a wrong forecast will have little-to-none business effects.
2. It is an interesting field that might prove useful should the forecasting technique produces a fruitful result.

### balena.io

Before we delve into the use-case, it is pertinent to describe, on a high-level, the platform which produces the data-set that we will use.

Balena.io is a company that reduces friction for fleet-owners, people who develop applications and deploy code on a fleet of IoT devices. 

In order to do that, we we have brought several paradigms of the cloud-native development to the world of embedded Linux devices.

Each device that is managed by [balena-cloud](https://www.balena.io/cloud/) (the core product) and runs [BalenaOS](https://www.balena.io/os/), will connect to our back-end server, so that it can be managed remotely.


## Use case

We will forecast the number of online devices on a hourly/daily basis, as seen by our internal VPN. This data-set can further be enhanced with metadata regarding the size of the fleet that they belong to for further analysis. The data-set is set between 2016 and 2018, while a small-dataset of out-of-sample devices will be used to benchmark the forecast.

In essence, the data-set is a set of `online` and `offline` events for each device, at specific time-stamps. Since there is a number of different `VPN servers` that the devices could connect to, there is some added complexity regarding the detection of the time for which the device stayed online, but this will be analysed as part of the project.

### Disclaimer
The data are completely anonymized and thus it's impossible, even for me, to correlate them to any prior or existing customer.

## Goal

Our **business-facing goal** is to work on the data-set on both hourly and daily basis, detecting potential seasonality on both levels and then perhaps performing a double forecast, on both the daily online status and the hourly one. This way, our engineers will be able to better anticipate the load on the VPN servers and make proper adjustments to our infrastructure, ensuring both **quality of service** and **reducing cost** at the same time.

Moreover, the project's goals and requirements are mentioned in the above section, where we will have the chance to benchmark statistical vs machine-learning methodologies.

**Bonus**
An interesting additional point will be to see how the Covid-19 situation has affected the data-set, as we live in a time of great uncertainty, perhaps even in a time of another black swan.
 
