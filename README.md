# AIND Term II: Computer Vision Course Project

## Rubric items

#### Files Submitted

| Criteria       		|     Meets Specifications	        			            | 
|:---------------------:|:---------------------------------------------------------:| 
| Submission Files      |  CV_project.ipynb--> all completed python functions requested in the main notebook CV_project.ipynb (TODO items) should be completed		|

#### Documentation

| Criteria       		|     Meets Specifications	        			            | 
|:---------------------:|:---------------------------------------------------------:| 
| Comments         		| The submission includes comments that describe the functionality of the code.  Every line of code is preceded by a meaningful comment.  1. describing input parameters to OpenCV module functions.  2. function calls  3. explaning thought process in common language	|

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
| Blur and edge detect a test image.  | The submission returns an edge detected image that has been blurred properly and with the dictated parameters. |


#### Step 4: Hiding the identity of an unwilling participant automatically

| Criteria       		|     Meets Specifications	        			            | 
|:---------------------:|:---------------------------------------------------------:| 
| Find and blur the face of an individual in a test image. |  The submission provides code to automatically detect the face of a person in a test image and blur their face to mask their identity.  |


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
|  Answer a few questions about your training and visualize the Loss function.| The submission successfully discusses any potential issues with their training, and addresses the provided questions regarding this.  |


#### Step 8:  Facial Keypoints Detector: complete the pipeline
| Criteria       		|     Meets Specifications	        			            | 
|:---------------------:|:---------------------------------------------------------:| 
| Combine OpenCV face detection with your trained convnet facial keypoint detector. | The submission successfully combines OpenCV's face detection with their trained convnet keypoint detector. |
