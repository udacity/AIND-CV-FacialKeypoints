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

All of the starting code and resources you'll need to compete this project are in a Github repo! Before you can get stared coding, you'll have to make sure that you have all the libraries and dependencies required to support this project.

### Amazon Web Services

This project requires GPU acceleration to run efficiently. Please refer to the Udacity instructions for setting up a GPU instance for this project, and refer to the project instructions in the classroom for setup. [link for AIND students](https://classroom.udacity.com/nanodegrees/nd889/parts/16cf5df5-73f0-4afa-93a9-de5974257236/modules/53b2a19e-4e29-4ae7-aaf2-33d195dbdeba/lessons/2df3b94c-4f09-476a-8397-e8841b147f84/project)


### Local Environment Instructions

You should follow the AWS instructions in your classroom for best results.

1. Clone the repository, and navigate to the downloaded folder.
```
git clone https://github.com/udacity/AIND-CV-FacialKeypoints.git
cd AIND-CV-FacialKeypoints
```

2. Create (and activate) a new environment with Python 3.5 and the `numpy` package.

	- __Linux__ or __Mac__: 
	```
	conda create --name aind-cv python=3.5 numpy
	source activate aind-cv
	```
	- __Windows__: 
	```
	conda create --name aind-cv python=3.5 numpy scipy
	activate aind-cv
	```

3. Install/Update TensorFlow (for this project, you may use CPU only).
	- Option 1: __To install TensorFlow with GPU support__, follow [the guide](https://www.tensorflow.org/install/) to install the necessary NVIDIA software on your system.  If you are using the Udacity AMI, you can skip this step and only need to install the `tensorflow-gpu` package:
	```
	pip install tensorflow-gpu==1.1.0
	```
	- Option 2: __To install TensorFlow with CPU support only__:
	```
	pip install tensorflow==1.1.0
	```

4. Install/Update Keras.
 ```
pip install keras -U
```

5. Switch [Keras backend](https://keras.io/backend/) to TensorFlow.
	- __Linux__ or __Mac__: 
	```
	KERAS_BACKEND=tensorflow python -c "from keras import backend"
	```
	- __Windows__: 
	```
	set KERAS_BACKEND=tensorflow
	python -c "from keras import backend"
	```

6. Install a few required pip packages (including OpenCV).
```
pip install -r requirements.txt
```


### Data

All of the data you'll need to train a neural network is in the AIND-CV-FacialKeypoints repo, in the subdirectory `data`. In this folder are a zipped training and test set of data.

1. Navigate to the data directory
```
cd data
```

2. Unzip the training and test data (in that same location). If you are in Windows, you can download this data and unzip it by double-clicking the zipped files. In Mac, you can use the terminal commands below.
```
unzip training.zip
unzip test.zip
```

You should be left with two `.csv` files of the same name. You may delete the zipped files.

*Troubleshooting*: If you are having trouble unzipping this data, you can download that same training and test data on [Kaggle](https://www.kaggle.com/c/facial-keypoints-detection/data).

Now, with that data unzipped, you should have everything you need!

## Notebook

1. Navigate back to the repo. (Also your source environment should still be activated at this point)
```shell
cd
cd AIND-CV-FacialKeypoints
```

2. Open the notebook and follow the instructions.
```shell
jupyter notebook CV_project.ipynb
```

__NOTE:__ While some code has already been implemented to get you started, you will need to implement additional functionality to successfully answer all of the questions included in the notebook. __Unless requested, do not modify code that has already been included.__


## Evaluation

Your project will be reviewed by a Udacity reviewer against the Computer Vision project [rubric](#rubric).  Review this rubric thoroughly, and self-evaluate your project before submission.  All criteria found in the rubric must meet specifications for you to pass.


## Project Submission

When you are ready to submit your project, collect the following files and compress them into a single zip archive for upload:

 - The `CV_project.ipynb` file with fully functional code. All code cells should be executed and displaying output, and all questions should be answered.
 - An HTML *or* PDF export of the project notebook with the name `report.html` or `report.pdf`.
 - Any additional images used for the project that were not supplied to you for the project. 
 - **Please do not include the project data sets in the data/ folder**. They are too big and only your executed notebook code and text will be evaluated.

Alternatively, your submission could consist of only the **GitHub link** to your repository.

<a id='rubric'></a>
## Project Rubric

#### Files Submitted

| Criteria       		|     Meets Specifications	        			            | 
|:---------------------:|:---------------------------------------------------------:| 
| Submission Files      |  `CV_project.ipynb`--> all completed python functions requested in the main notebook `CV_project.ipynb` **TODO** items should be completed.		|


#### Step 1:  Add eye detections to the face detection setup
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
| Blur and edge detect a test image.  | The submission returns an edge-detected image that has first been blurred, then edge-detected, using the specified parameters. |


#### Step 4: Automatically hide the identity of a person (blur a face)

| Criteria       		|     Meets Specifications	        			            | 
|:---------------------:|:---------------------------------------------------------:| 
| Find and blur the face of an individual in a test image. |  The submission should provide code to automatically detect the face of a person in a test image, then blur their face to mask their identity.  |


#### Step 5:  Specify the network architecture
| Criteria       		|     Meets Specifications	        			            | 
|:---------------------:|:---------------------------------------------------------:| 
|  Specify a convolutional network architecture for learning correspondence between input faces and facial keypoints. | The submission successfully provides code to build an appropriate convolutional network. |


#### Step 6:  Compile and train the model
| Criteria       		|     Meets Specifications	        			            | 
|:---------------------:|:---------------------------------------------------------:| 
|  Compile and train your convnet.| The submission successfully compiles and trains their convnet.  |


#### Step 7:  Answer a few questions and visualize the loss
| Criteria       		|     Meets Specifications	        			            | 
|:---------------------:|:---------------------------------------------------------:| 
|  Answer a few questions about your training and visualize the loss function.| The submission successfully discusses any potential issues with their training, and answers all of the provided questions.  |


#### Step 8:  Complete a facial keypoints detector and complete the CV pipeline
| Criteria       		|     Meets Specifications	        			            | 
|:---------------------:|:---------------------------------------------------------:| 
| Combine OpenCV face detection with your trained convnet facial keypoint detector. | The submission successfully combines OpenCV's face detection with their trained convnet keypoint detector. |
