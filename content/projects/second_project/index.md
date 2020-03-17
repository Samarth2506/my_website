---
title: Flight Delay Prediction
summary: Predicted flight delays from structured data with attributes like origin and destination city, departure and arrival times,carrier information, passenger count and weather station data of the cities of interest. Iterated through the Data Science pipeline to build Machine Learning models including Logistic Regression, SVM, Decision Trees, Random Forests and Gradient Boosting.
tags:
- Machine Learning
- R
- Python
- Scikit-Learn

date: "2018-07-27T00:00:00Z"


# Optional external URL for project (replaces project detail page).
external_link: ""

image:
  focal_point: Smart

links:
- icon: Github
  icon_pack: fab
  name: Follow
  url: https://github.com/samarth2506
url_code: ""
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

Predicted flight delays from structured data with attributes like origin and destination city, departure and arrival times,carrier information, passenger count and weather station data of the cities of interest. Iterated through the Data Science pipeline to build Machine Learning models including Logistic Regression, SVM, Decision Trees, Random Forests and Gradient Boosting. The details of the implementation are listed below.

</br>

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

* Built multiple classification models including Logistic Regression, SVM, Decision Trees, Random Forests and Gradient Boosting.

</br>

## **Analysis, Iteration and Communication**

* Iterated through models using a the most important features infered from models like Decision Trees to reduce computational complexity and over-fitting of the model.

* Presented trade-off between model interpretation and model accuracy. 

* Developed a deeper understanding of model metrics such as recall, precision and F-1 score

</br>

## **Results**

* A key challenege in prediction was the imbalance in data.

* Gradient Boosting was the best model that achieved an F-1 score of 70%. 