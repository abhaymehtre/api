# ML based model training and deployment using FastApi and CICD.

This repository contains a dataset collected from kaggle on the Spam Classification Dataset which is based on neural network for spam classification. It also trains a simple spam classification model that determines if a text message is a spam.


# Process Flow

The repository consists of a train_spam_detector file, where it does the following:
1.  Reads the spam dataset.
2.  Splits the spam dataset into training and testing sets.
3.  Creates a text preprocessing and deep learning pipeline for spam classification.
4.  Trains the model pipeline on the training set.
5.  Evaluates the model pipeline on the testing set.
6.  Saves the trained model pipeline.

 
## Work Flow
The work flow starts with training the model by collecting the data from the csv file.  A fastApi based file is created where the GET and POST calls will be used.  The **preprocessor** function above removes emoticons and unwanted characters from the text input while the **classify_message** function calls the **preprocessor** function to clean a text message before using the spam detection model to generate predictions. The **classify_message** function returns a dictionary, which can conveniently be interpreted as a JSON response.

## Execution of the project

1. Clone the repository by using git clone.
2. Then install thre requirement softwares and libraries like FastAPI, sklearn, joblib and others are per the requirement.
3. Once the libraries are installed then, using pip install uvicorn install the uvicorn to run the FastApi based app.  Command: uvicorn main:app --reload
4. The system will  allot a localhost based http url. Clicking on it will render you to the execution of main.app.
5. We can test this new GET request by navigating to the API URL from localhost.
6. Please follow the below sections to get the spam related probability of the text message you give as an input in the URL. 

## Using Query Parameters

For a REST API, query parameters are part of the URL string and are prefixed by a “?”. For example, for the spam detection API we are creating, a GET request could look like this:

> 127.0.0.1.8000/spam_detection_query/?message=’hello, please reply to this message’_

## Automatically Generated Documentation

If you navigate to [http://127.0.0.1:8000/docs](http://127.0.0.1:8000/docs) after the run the above command you will find the documentation page for the FastAPI app. 








