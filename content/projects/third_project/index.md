---
title: DeepFake Detection with GANs
summary: The goal of the study is to detect fake images. An autoencoder is trained adversarially to obtain a latent rich representation of real images. The latent representation is then used to reconstruct an image based on the given input image. We propose a comparative study to test if reconstructed features differ strongly for real and fake images leading to enhanced classification performance. We further argue that adversarially training a classifier (DCGAN) generalizes better on unseen data as compared to CNN based architectures.
tags:
- Deep Learning
- Python
- PyTorch

date: "2020-05-27T00:00:00Z"


# Optional external URL for project (replaces project detail page).
external_link: ""

image:
  focal_point: Smart

links:
- icon_pack: fab
  name: Paper
  url: https://github.com/Samarth2506/DL_Project
url_code: "https://github.com/Samarth2506/DL_Project"
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

Click here to access the [complete paper](Detect_DeepFakes_GANs.pdf) and [code here](https://github.com/Samarth2506/DL_Project).

