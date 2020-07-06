---
title: Flight Delay Prediction
summary: Predicted flight delays from structured data with attributes like origin and destination city, departure and arrival times, carrier information, passenger count and weather station data of the cities of interest. Iterated through the Data Science pipeline to build Machine Learning models including Logistic Regression and Decision Trees. Post model building, hosted the app on R Shiny. Welcome to the app!

tags:
- Machine Learning
- R
- Shiny

date: "2019-07-27T00:00:00Z"


# Optional external URL for project (replaces project detail page).
external_link: ""

image:
  focal_point: Smart

links:
- icon_pack: fab
  name: App
  url: https://samarth2506.shinyapps.io/Flight_Delays_App/
- icon_pack: fab
  name: Follow
  url: https://github.com/samarth2506
url_code: "https://github.com/Samarth2506/Learning/tree/master/Projects/Predict_Flight_Delays"
url_pdf: ""
url_slides: ""
url_video: ""

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
slides: ""
---

Predicted flight delays from structured data with attributes like origin and destination city, departure and arrival times,carrier information, passenger count and weather station data of the cities of interest. Iterated through the Data Science pipeline to build Machine Learning models including Logistic Regression and Decision Trees. Post model building, hosted the app on R Shiny. The details of the implementation is described below.

</br>

We chose to predict flight delays because we love everything planes! Additionally, flight delays caused losses of over $28 billion in the US alone in 2018. Planning for anticipated delays can significantly improve operating costs for airlines.

 The data is from Kaggle and includes data about domestic US flight carriers for 2015. The dataset has about 6 million records and 30 features. Only 20% of the data was used to train/test the models due to constraints on computation. The prediction is made for the day and airline of the user's choice.

</br>

Link to the app: https://samarth2506.shinyapps.io/Flight_Delays_App/

To read more about using the app, click on the About tab after launching the app!

## **Data Pre-processing**

* The flight data and the weather station data sets were merged carefully to avoid loss of data and retain accurate information. 

* Missing information was imputed through Knn Imputation.

* The target column was derived on the condition that flights were considered delay is they arrived 15 minutes later than the scheduled time.


</br>

## **Data Visualization**

* Performed univariate, bivariate and multivariate visualizations using data to identify underlying patterns and anamolies in data.

* Observed an imbalance of 90:10 (on time versus delayed flights) in the target feature.

</br>

## **Feature Engineering**

* Large number of levels in categorical data such as origin/destination cities proved to be a challenge. Binned cities by region such North or South to reduce levels in categorical data.  Another strategy was to keep the highest frequency levels and bin the lower frequency levels in to a sigle category.

* New columns such as day of the week, month and year were derived from the date column to investigate a correlation with flight delays with different time intervals using the *Group By* function.

</br>

## **Data Modeling**

* Built multiple classification models including Logistic Regression and Decision Trees.

</br>

## **Analysis, Iteration and Communication**

* Iterated through models using a the most important features infered from models like Decision Trees to reduce computational complexity and over-fitting of the model.

* Presented trade-off between model interpretation and model accuracy. 

* Developed a deeper understanding of model metrics such as recall, precision and F-1 score

</br>

## **Results**

* A key challenege in prediction was the imbalance in data.

* Decision Tree was the best model that achieved a score of 90% accuracy on average. 

* Hosted the app successfully using Shiny.

</br>

## **Challenges** 

* Logistic Regression model size: The glm function in R used to build the Logistic Regression model by default stores the training data when the model is saved for prediction later. As a result, the app was extremely slow to launch when deployed. To overcome this, we stripped down the saved model to reduce the model size from 1.5 GB to 18.7 KB! Consequently, latency on the hosted app reduced by 500%.

* Shiny: The project was our first foray in to building and deploying a web application. The learning curve was steep with Shiny, especially while using a ML model to make predictions in real time but totally worth it!

</br>

