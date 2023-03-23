---
title: Handwritten digits demo!
description: MNIST digits classifier demo with canvas, allowing the user to create their own hand-drawn digits.
date: 2023-03-23
scheduled: 2023-03-23
tags:
  - mnist
  - classifier
  - image
  - docker
layout: layouts/post.njk
image: https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExNWViNjg1ZmIwMWZhOGZlZmY4ZTBmN2I4YmFkNTZhYTUzZGJjODQ1MiZjdD1n/wIYiDdDAMqsM0J9yhM/giphy.gif
---

# MNIST-KERAS-FLASK-JS

![a gif](https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExNWViNjg1ZmIwMWZhOGZlZmY4ZTBmN2I4YmFkNTZhYTUzZGJjODQ1MiZjdD1n/wIYiDdDAMqsM0J9yhM/giphy.gif)


This repository contains a simple web application that uses Keras and Flask to create an MNIST digit recognition model. The application allows users to upload an image or draw on an HTML canvas to get digit predictions.

## Features

- Keras-based MNIST digit recognition model
- Flask server for serving the model
- Web interface to test the model with uploaded images or drawings on an HTML canvas

## Requirements

Make sure you have the following Python packages installed:

- Flask==2.1.1
- Flask-CORS==3.0.10
- tensorflow==2.6.0
- Keras==2.6.0
- numpy==1.19.5
- Pillow==9.0.1
- protobuf==3.20.1

You can install the required packages using the following command:

````text/2-3
pip install -r requirements.txt
````

## Docker

The application can be built and run using Docker. To build the Docker image, run the following command in the project directory:
````text/2-3
docker build -t mnist-keras-flask-js .
````


To run the Docker container, use the following command:

````text/2-3
docker run -p 5000:5000 mnist-keras-flask-js
````


The application will be available at `http://127.0.0.1:5000`.

## Usage

There are two web pages available for testing the model:

1. **test-api.html**: This page allows you to upload an image to test the MNIST prediction model. The prediction result will be displayed below the image upload form.
2. **canvas_drawing.html**: This page allows you to draw a digit on an HTML canvas. The MNIST prediction model will predict the digit based on your drawing, and the prediction result will be displayed next to the canvas.

To access these pages, you can either run the Flask server locally or use the Docker container as described above. Then, navigate to `http://127.0.0.1:5000/static/test-api.html` or `http://127.0.0.1:5000/static/canvas_drawing.html` in your web browser.	