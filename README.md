# Real-Time Driver Fatigue Detection System

This project is a real-time Driver Drowsiness Detection System built using Computer Vision and Deep Learning. It monitors a driver’s face through a video feed and classifies alertness to help prevent accidents caused by fatigue.

## System Architecture

1. Video Input Capture:

The system captures live video from a dashcam or webcam installed in the vehicle.

2. Frame Extraction:

Using OpenCV, the video stream is broken into individual frames for processing, where each frame is treated as a standalone image.

3. Face Detection

Each frame is passed through a pre-trained ResNet-based Caffe model (.caffemodel) using OpenCV to detect and localize the driver’s face.

4. Face Region Cropping

The detected face region is extracted and cropped to remove irrelevant background information and focus only on facial features.

5. Drowsiness Classification

The cropped face images are fed into a VGG16-based deep learning model trained on approximately 9,000 labeled images.
The model classifies the driver as:

Active (Alert)
Fatigued (Drowsy)

6. Performance Optimization

The initial model achieved approximately 85% accuracy.
After introducing face cropping, performance improved significantly due to reduced background noise and better feature extraction.

7. Real-Time Processing

The system runs in real time, achieving approximately 17 FPS on CPU while processing a ~20 FPS video stream.

## Dataset

The model was trained on a multiracial driver fatigue dataset sourced from Kaggle.

📦 Total Images: ~9000
🏷 Labels: Active / Fatigue Subjects

Dataset Link:
https://www.kaggle.com/datasets/rakibuleceruet/drowsiness-prediction-dataset

## VGG16-based image classification model:

Link to Model: 
https://drive.google.com/file/d/1zyOEzHi1LVrZCeqVdtF9yn7ARYQrtsOt/view?usp=drive_link
