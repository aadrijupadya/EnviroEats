# EnviroEats

EnviroEats is a progressive machine learning web application that aims to solve two vast healthcare and environmental problems. 

## Inspiration

Poor dietary styles and lack of nutrition knowledge of the American public has led to high rates of obesity, food related diseases such as diabetes and cardiovascular disease. In addition, to causing health problems, these poor dietary styles have also posed a massive threat to the environment through greenhouse emissions and heavy resource (land and water) usage.

Many people tend to find ‘healthy’ and ‘eco-friendly’ recipes online through various recipe websites, or modern ‘eco-friendly’ restaurants, but can never be sure if these labels are just greenwashing (a common marketing phenomenon in which products are marketed as eco-friendly even though they are not) or legitimate.

Our web application aims to solve some of these problems.

## What it Does
We created a web application that has multiple functionalities: A trained CNN model to classify how Healthy a food is A semantic, word2vec based NLP model to quantify the carbon footprint of a given food Login email authentication A place for users to upload recipes that they find to be healthy and a place for other users to view these healthy recipes

## How we Built it 

* JS, HTML, CSS for Front-end, Python, Flask, MySQL for backend
* The CNN model uses a PyTorch ResNet (common CNN architecture) and resizes the given images. It then applies data augmentation and random oversampling to prevent overfitting and poor performance due to class imbalance. The model then outputs a probability that a certain image belongs to a certain class.
* The NLP model uses the Spacy Word2Vec API trained on both the usual en_core_web_sm dataset and a kaggle recipe dataset to analyze the similarity between the words provided and our food emissions data to quantify the amount of carbon footprint that creating a food with those particular ingredients might cause. We use MySQL databases and tables to store our data and run our apps with Flask, a Python based application library.

## Future Steps

* Deployment on Heroku or some sort of flask app hosting service
* A mobile-application or computer camera-plug-in to directly feed in images from camera
* Using RNNs and NLP to generate synthetic healthy recipes given a set of ingredients
* More comprehensive and clean reports for environmental impact
* Improving performance of models with more data
