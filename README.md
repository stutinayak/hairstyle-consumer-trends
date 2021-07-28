# hairstyle-consumer-trends

Question (Pipeline)
In the above situation you have been provided with a dataset based upon images. Imagine the situation in which you would need to source the information from an online source. 
Describe the data pipeline you would build in order to reach a similar result.

Answer: 
In order to source information from an online source the following pipeline could be used: 
1. With the help of an API (if there exists one) extract the relevant information needed from the source. Another way of extracting is to scrape the data from the web.
2. Extract the metadata about the information e.g. type of data, size of data, date etc.
3. Structure the data in a format that can be analyzed - csv, json etc. 

Question (Premium photography identification)
Professional photographers are a distinct group of creatives. Their work is highly subjective and only by using human intuition we are able to classify them. How would you use visual recognition in order to separate professional photographers from amateurs ones?
Note: describe what steps you would take in order to answer the question and what possible elements of professional photographers you would take into consideration.

Answer:  
When it comes to professional photography the main part is editing. In order to develop a visual recognition to classify pictures into amateur v/s professional the main goal is to have enough data for both classes. 
In some cases the images would not be enough information so additional feature engineering can be included in the pipeline. The features can be extracted from both type of images - amateur and professional. 
Conventional approaches typically adopt handcrafted features to computationally model the photographic rules (lighting, contrast), 
global image layout (rule-of-thirds) and typical objects (human profiles, animals, plants) in images. 
In more recent work, generic deep features and learned deep features from deep learning models like Convolutional Neural Networks (CNN) exhibit stronger representation power for this task. Naive Bayes classifier, SVM, boosting and deep classifier are typically used for binary classification of high-quality and low-quality images, whereas regressors like support vector regressor are used in ranking or scoring images based on their aesthetic quality. There has been a lot cool research state-of-the-art techniques which could be used: https://arxiv.org/pdf/1610.00838.pdf and https://github.com/miyamotty/awesome_ImageAesthetics.

A cloud approach could also be adopted for this problem: In this do not have the data tagged: we could use the Amazon Sagemaker Ground Truth (https://aws.amazon.com/sagemaker/groundtruth/). 
1. Ground Truth creates its own model as images are labeled by people
2. As this model learns, only images the model isn’t sure about are sent to human labellers
3. This can reduce the cost of labelling jobs by 70%
