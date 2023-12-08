  **EYE BLINK DETECTION FOR PARALYSED PATIENTS USING HAAR CASCADE CLASSSIFIER.**
  
We represent a real time method based on some video and image processing algorithms for eye blink detection. 
The motivation of this research is the need of disabling who cannot communicate with human.

	**Main objectives**

1]	Allow paralysis victims to communicate independently
2]Be accessible to people with financial constraints

**Scope**

The Scope of the proposed work is on HUMAN COMPUTER INTERFACE

HCI for physically challenged impaired people with respect to movement need to satisfy certain conditions such as HCI should not be in connection, avoid dedicated apparatus,
it should offer better performance, and it should get processed on customer computer. 
The main reasons for these conditions are not because the research could gather lesser capital but because the end user might not be able to afford highly expensive commodities and 
hence a system working on one of the most common of infrastructure is of great use to the user.

**Hardware Requirements**
CPU	: Intel 2.1 GHZ

Memory	: 4GB

Disk	: 100GB

Display	: 15 inch color


Camera Installation: The software needs to detect the blinking of eyes with the assistance of camera. So, the computer should be installed with the camera. 
Desktop computer doesn’t have camera, so an extra camera needs to be installed and linked to the software. The laptop is equipped with the camera, so it will be linked.


	**Software (Tools &Technologies) Requirements**

Coding	: Python
Platform	: python 3.7 or 3.8 Tool	: Spyder
OS	: Windows 7


Open CV: It is a library of programming functions mainly realtime computer vision. 
It was originally developed by Intel and it was later supported by Willow Garage and is now maintained by IITSSEZ. 
OpenCV is written in C++ and is primarily interface is in C++. There are bindings in python, java and MATLAB/Octave.


Installation and Usage: run pip install OpenCVpython Import the packages for 3 3OpenCV: Open Python IDLE and type following codes in Python terminal.
>>>import cv2

>>>print(cv.version)

Python dlib: It is developed by Davis King, the dlib C++ library is a cross-platform package for threading networking, numerical operations.
placing a strong emphasis on extremely high- quality and portable code. 
From a computer vision perspective, dlib has reveal state-of- the-art implementations, including:
Facial landmark detection, Correlation tracking, Deep metric learning.

**System Architecture of the proposed system**


1.	Capturing the frame from the video using the system’s camera initializes the execution of the proposed system.
2.	The frames are converted into gray scale image and we are making zero and ones combination of white and black pixels.
3.	We are considering 68 point pixel for face and 6 point pixel for eye lids.
4.	The Face Detection is done using haar cascade Algorithm processes on the captured video frames which is converted as gray scale image to give out the rectangular boxed face. 

5.	The output from Face Detection Algorithm then gets processed using AdaBoost Classifier to detect the eye region in the face.
6.	Eye detected will be sent to check whether the eye is closed or open.
7.	When the eyes are open the virtual keyboard numbers are being played sequence until the eyes are closed.
8.	Once eye is closed then the particular need of the patient in that number is given as a output for care takers.
9.	The outputs are in the form of image display, text alerting, audio played etc.

1.	Frame Capturing
Frame Capturing The first step that is the initialization. After taking a short video of the participant’s face using the front camera of the Samsung mobile.
A process Frame method will be used to create the frames from the captured video.
Afterwards the colored frames will be converted to gray scale frames by extracting only the luminance component.

3.	Face Detection

The Haar classifier is used in this algorithm for face detection. Haar classifier rapidly detects any object, based on detected feature not pixels, like facial feature. 
However, the area of the image being analyzed for a facial feature needs to be regionalized to the location with the highest probability of containing the feature.
By regionalizing the detection area, false positives are eliminated. 
As the result, the face is detected and marked   with color rectangle and will be used later to approximate an axis of the eyes for eye detection step.

3.	Eye Detection

To detect the eye, first, the Haar cascade classifier should be trained, in order to train the classifiers, the Ada Boost algorithm and Haar feature algorithms must be implemented, two set of images are needed. One set contains an image or scene that does not contain the object. The EBCM used all detected elements from the Haar Cascade Classifier.

4.	Eye Tracking

The corneal-reflection and pupil-center are the two eye’s parts that are the most important parts to extract the features that will be used method. 
These features help us in tracking the eyes movement.
By identifying the center of the pupil and the location of the corneal reflection, 
the vector between them is measured. Besides, with further trigonometric calculations, point-of- regard can be found. The method succeeded in making the face and the eye's pupil moved together in the same direction synchronously and with the same direction. 




