# Predicting_March_Madness

## Background: 

The goal of this project was to use machine learning techniques to predict the 2022 NCAA Mens Basketball Tournament. This started as a final project for my Master Program's Big Data Analytics class under Professor Jon Fox. The original project/code was created by myself and four teammates: Farahin Choudhury, Matthew Laken, Annie Titus, and Jiebin (Alex) Zhu. Any future improvements to the code will be a solo effort. 

## Files:

2022 March Madness Prediction.docx: The written report for the project.

2022 March Madness Prediction.pptx: The presentation for the project.

2022 March Madness Prediction.ipynb: The code used to create the models for the project. Markdown notes offer some details on how the code works.

Note: The original data for this project will not be included as the data is owned by Google and is part of a Kaggle competiiton. A link to the original Kaggle page is included in the written report. 

## Technical Requirements:

Any text editor that supports python can be used to run the code. Use of a GPU is highly recommended given the size of the dataset (especially on older or less powerful hardware).

## Development:

### Data Cleaning:

Most of the source code for data cleaning was found within this post (https://www.activestate.com/blog/fantasy-march-madness-how-to-predict-winners/) written by Dante Sblendorio whose repository is linked in the references section. The data preparation included:

1.	Normalizing the number of points in game to account for games that go into overtime.
2.	Calculating certain metrics such as points per game(ppg), number of games for winning/losing teams, and win percentage for the season.
3.	Excluding 2020 from the dataset (as there was no tournament that year).
4.	Partitioning the data into a training and testing dataset. 

### Models:

The two models created and implemented in this analysis were XGBoost and convolutional neural networks. XGBoost, or eXtreme Gradient Boosting, is a library meant for computing gradient boosting at scale. The premise of gradient boosting is to provide a prediction from classification tasks defined in the model. Since XGBoost requires a classification metric for this model, the output of the training model provides the ‘logloss’ error as the evaluation. XGBoost was selected due to its accuracy and time performance. A model that doesn’t take too long to run, but still has a rather accurate result is what our team was looking for.

Our team decided to explore another model for better reference. The other model, using a convolutional neural network (CNN), did not produce the ideal outcome but it is still worth exploring and including as part of the overall analysis. This deep learning model implemented the activation function ‘rectified linear unit’, also known as ReLU (activation = ‘relu’). This made the most sense to use and seemed more efficient than the sigmoid activation. In general, neural networks are quite powerful and can provide insights other algorithms might not be able to.


### Results:

![2022 Bracket](https://user-images.githubusercontent.com/87530934/213572570-141bab54-6cd6-4eda-a1de-3a2914711608.png)

# References:

March machine learning mania 2022 - NCAAM. Kaggle. (2022). Retrieved March 19, 2022, from https://www.kaggle.com/c/mens-march-mania-2022/data

Pomeroy, K. (2022). 2022 Pomeroy College Basketball Ratings. Retrieved March 19, 2022, from https://kenpom.com/

reHOOPerate. (2020, January 15). New and improved March madness neural network for 2020. Medium. Retrieved March 19, 2022, from https://medium.com/re-hoop-per-rate/new-and-improved-march-madness-neural-network-for-2020-c154aa1041b7

Sblendorio, D. (2021, March 19). Fantasy march madness: How to predict winners. ActiveState. Retrieved March 19, 2022, from https://www.activestate.com/blog/fantasy-march-madness-how-to-predict-winners/ 

Dante Sblendorio's Repository: https://gitlab.com/dsblendo/kaggle_mm



