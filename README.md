[//]: # (Image References)

[image1]: ./images/obamas_with_keypoints.png "Facial Keypoint Detection"

# AIND Term II, Computer Vision Capstone Project 
# Facial Keypoint Detection and Real-time Filtering

## Project Overview

Welcome to the Computer Vision capstone project in the AI Nanodegree program! In this project, you’ll combine your knowledge of computer vision techniques and deep learning to build and end-to-end facial keypoint recognition system. Facial keypoints include points around the eyes, nose, and mouth on any face and are used in many applications, from facial tracking to emotion recognition. Your completed code should be able to take in any image containing faces and identify the location of each face and their facial keypoints, as shown below.

![Facial Keypoint Detection][image1]

The project will be broken up into a few main parts in one Python notebook:

__Part 1__ : Investigating OpenCV, pre-processing, and face detection

__Part 2__ : Training a Convolutional Neural Network (CNN) to detect facial keypoints

__Part 3__ : Putting parts 1 and 2 together to identify facial keypoints on any image!

You'll also be given *optional* exercises that allow you to extend this project so that it works on video and allows you to implement fun face filters in real-time!


## Project Instructions

### Instructions

1. Open the notebook and follow the instructions.
	
	```
		jupyter notebook CV_project.ipynb
	```

__NOTE:__ While some code has already been implemented to get you started, you will need to implement additional functionality to successfully answer all of the questions included in the notebook. __Unless requested, do not modify code that has already been included.__


## Evaluation

Your project will be reviewed by a Udacity reviewer against the Computer Vision project [rubric](#rubric).  Review this rubric thoroughly, and self-evaluate your project before submission.  All criteria found in the rubric must meet specifications for you to pass.


## Project Submission

When you are ready to submit your project, collect the following files and compress them into a single archive for upload:
- The `CV_project.ipynb` file with fully functional code, all code cells executed and displaying output, and all questions answered.
- An HTML or PDF export of the project notebook with the name `report.html` or `report.pdf`.
- Any additional images used for the project that were not supplied to you for the project. __Please do not include the project data sets in the `data/` folder.__

<a id='rubric'></a>
## Project Rubric

#### Files Submitted

| Criteria       		|     Meets Specifications	        			            | 
|:---------------------:|:---------------------------------------------------------:| 
| Submission Files      |  CV_project.ipynb--> all completed python functions requested in the main notebook CV_project.ipynb (TODO items) should be completed		|

#### Documentation

| Criteria       		|     Meets Specifications	        			            | 
|:---------------------:|:---------------------------------------------------------:| 
| Comments         		| The submission includes comments that describe the functionality of the code.  Every line or function (chunk of functional code) is preceded by a meaningful comment.  

Comments should generally: 1. Describe input parameters to OpenCV functions.  2. Describe the purpose of function calls.  3. Explain the coder's thought process in common language.	|

#### Step 1:  Add eye detections to our face detection setup
| Criteria       		|     Meets Specifications	        			            | 
|:---------------------:|:---------------------------------------------------------:| 
|  Add eye detections to the current face detection setup. |  The submission returns proper code detecting and marking eyes in the given test image. |


#### Step 2: De-noise an image for better face detection

| Criteria       		|     Meets Specifications	        			            | 
|:---------------------:|:---------------------------------------------------------:| 
| De-noise an image for better face detection.  |  The submission completes de-noising of the given noisy test image with perfect face detections then performed on the cleaned image. |


#### Step 3: Blur and edge detect an image

| Criteria       		|     Meets Specifications	        			            | 
|:---------------------:|:---------------------------------------------------------:| 
| Blur and edge detect a test image.  | The submission returns an edge-detected image that has been blurred then edge-detected using the specified parameters. |


#### Step 4: Hiding the identity of a person automatically

| Criteria       		|     Meets Specifications	        			            | 
|:---------------------:|:---------------------------------------------------------:| 
| Find and blur the face of an individual in a test image. |  The submission shoul provide code to automatically detect the face of a person in a test image then blur their face to mask their identity.  |


#### Step 5:  Specify the Network Architecture
| Criteria       		|     Meets Specifications	        			            | 
|:---------------------:|:---------------------------------------------------------:| 
|  Specify a convolutional network architecture for learning correspondence between input faces and facial keypoints. | The submission successfully provides code to build an appropriate convolutional network. |


#### Step 6:  Compile and Train the Model
| Criteria       		|     Meets Specifications	        			            | 
|:---------------------:|:---------------------------------------------------------:| 
|  Compile and train your convnet.| The submission successfully compiles and trains their convnet.  |


#### Step 7:  Answer a few questions and visualize the Loss
| Criteria       		|     Meets Specifications	        			            | 
|:---------------------:|:---------------------------------------------------------:| 
|  Answer a few questions about your training and visualize the loss function.| The submission successfully discusses any potential issues with their training, and answers all of the provided questions.  |


#### Step 8:  Facial Keypoints Detector: complete the pipeline
| Criteria       		|     Meets Specifications	        			            | 
|:---------------------:|:---------------------------------------------------------:| 
| Combine OpenCV face detection with your trained convnet facial keypoint detector. | The submission successfully combines OpenCV's face detection with their trained convnet keypoint detector. |
