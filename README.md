# 🚗 Drowsy Driver Monitoring and Detection --
 
#### Using tkinter and OpenCV --

- The alert system will activate as soon as the driver's head will incline by some angle and the eye level will shift.
- The beeping mechanism will help him be alert. 
- The GUI has been done using Tkinter.

#### ✔ Import Libraries --
    - import numpy
    - from pygame import mixer
    - import time
    - import cv2
    - from tkinter import *
    - import tkinter.messagebox
    
    
Driver Drowsiness Detection System

Objective:
The objective of this intermediate Python project is to build a drowsiness detection system using computer vision techniques. This system aims to detect when a person's eyes are closed for an extended period while driving, indicating potential drowsiness, and alert the driver to prevent accidents.

Project Overview:
In this Python project, we utilize OpenCV for capturing images from a webcam and feeding them into a deep learning model that classifies whether a person's eyes are 'Open' or 'Closed'. The workflow of the project can be summarized as follows:

Step 1: Image Capture

Images are captured as input from a webcam in real-time.
Step 2: Face Detection and Region of Interest (ROI)

We use OpenCV to detect faces in the images.
Once a face is detected, a Region of Interest (ROI) is defined around the detected face.
Step 3: Eye Detection and Feeding to Classifier

Within the ROI, we further detect the eyes using eye cascade classifiers.
The detected eyes are extracted and fed into a deep learning classifier.
Step 4: Eye Classification

The deep learning model classifies whether the eyes are 'Open' or 'Closed'.
Step 5: Drowsiness Score Calculation

A score is calculated based on the duration of closed eyes.
If both eyes are closed, the score increases; when eyes are open, the score decreases.
An alarm is triggered if the score exceeds a predefined threshold, indicating potential drowsiness.
Technical Details:

Dataset: A custom dataset of approximately 7000 eye images was created. These images were categorized as 'Open' or 'Closed' and manually cleaned for training.

Model Architecture: A Convolutional Neural Network (CNN) is used for classification. The CNN architecture includes convolutional layers (32 nodes, kernel size 3), followed by a fully connected layer (128 nodes) and an output layer with 2 nodes. ReLU activation is used in the hidden layers, and softmax in the output layer.

Libraries and Tools:

OpenCV for image capture and processing.
TensorFlow and Keras for deep learning model development.
Pygame for playing an alarm sound.
Execution:
To run the project, execute the 'drowsiness detection.py' script. It captures real-time webcam images and analyzes them for drowsiness, sounding an alarm if necessary.

Conclusion:
This Driver Drowsiness Detection System is a practical application of computer vision and deep learning. It can significantly enhance road safety by alerting drivers when they are becoming drowsy. This project demonstrates the effective integration of hardware (webcam), software (OpenCV, TensorFlow, Keras), and machine learning techniques to address a critical safety concern on the road.

