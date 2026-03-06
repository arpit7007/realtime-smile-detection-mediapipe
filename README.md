# Real-Time Smile Detection with AR Filters

A real-time computer vision application that detects smiles using MediaPipe facial landmarks and a Logistic Regression model, then overlays augmented reality filters using OpenCV.

## Overview

This project uses MediaPipe Face Mesh to detect facial landmarks from a webcam feed. The distance between the upper and lower lip landmarks is used as a feature to classify whether a person is smiling or not. A trained Logistic Regression model performs the classification. When a smile is detected, an AR fire filter appears near the mouth while glasses are displayed on the face.

## Features

* Real-time facial landmark detection using MediaPipe
* Smile detection using a Logistic Regression classifier
* Augmented Reality filters using OpenCV
* Dynamic filter positioning based on facial landmarks
* Lightweight geometric feature extraction

## Tech Stack

* Python
* OpenCV
* MediaPipe
* Scikit-learn
* NumPy
* Joblib

## Project Structure

realtime-smile-detection-mediapipe
│
├── data
│   └── smile_dataset.csv
│
├── filters
│   ├── glasses.png
│   └── fire.png
│
├── models
│   └── smile_model.pkl
│
├── src
│   ├── train_model.py
│   └── realtime_smile_detection.py
│
├── requirements.txt
└── README.md

## How It Works

1. The webcam captures real-time video frames.
2. MediaPipe Face Mesh detects facial landmarks.
3. The vertical distance between upper and lower lip landmarks is calculated.
4. A Logistic Regression model predicts whether the person is smiling.
5. If smiling, AR filters are applied using OpenCV.

Pipeline:

Webcam Frame
↓
Face Landmark Detection (MediaPipe)
↓
Feature Extraction (Mouth Height)
↓
Smile Classification (Logistic Regression)
↓
AR Filter Overlay (OpenCV)

## Installation

Clone the repository:

git clone https://github.com/yourusername/realtime-smile-detection-mediapipe.git

Navigate to the project folder:

cd realtime-smile-detection-mediapipe

Install dependencies:

pip install -r requirements.txt

## Train the Model

Run the training script:

python src/train_model.py

This will generate the trained model file:

models/smile_model.pkl

## Run the Real-Time Application

python src/realtime_smile_detection.py

Press **ESC** to exit the application.

## Example Behavior

* Glasses filter appears on detected face.
* When the system detects a smile, a fire filter appears near the mouth.
* Status text displays **Smiling** or **Not Smiling**.

## Learning Outcomes

* Real-time computer vision with MediaPipe
* Facial landmark feature extraction
* Training and using machine learning models
* Augmented reality overlays with OpenCV

## Future Improvements

* Use more facial features for better smile detection
* Improve filter stability using temporal smoothing
* Support multiple faces simultaneously
* Add more AR filters

## License

This project is for educational and research purposes.
