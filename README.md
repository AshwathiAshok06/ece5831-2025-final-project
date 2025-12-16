# Vehicle Detection and Speed Estimation

This project implements a vision-based system to detect vehicles in traffic videos, classify their type, and estimate their speed using computer vision and deep learning techniques. The system processes video input frame by frame and produces annotated video output along with numerical speed data.

## Project Overview

The system performs the following tasks:
- Detect vehicles from traffic video using background subtraction
- Track each vehicle across frames using centroid-based tracking
- Classify vehicles into four types: car, bus, truck, and motorcycle
- Estimate vehicle speed in miles per hour (mph) based on pixel motion
- Display results directly on the video and save data for analysis

The project is developed using Python with OpenCV for computer vision tasks and TensorFlow/Keras for deep learning.

## Datasets Used

### Dataset 1: Vehicle vs Non-Vehicle Images  
Used for binary vehicle detection training.  
Link: https://www.kaggle.com/datasets/brsdincer/vehicle-detection-image-set/data  

- Total images: 17,760  
- Vehicle images: 8,792  
- Non-vehicle images: 8,968  

### Dataset 2: Vehicle Detection – 8 Classes  
Used for vehicle type classification.  
Link: https://www.kaggle.com/datasets/sakshamjn/vehicle-detection-8-classes-object-detection  

- Original dataset contains 8 classes  
- This project uses a subset of 4 classes:
  - Car
  - Bus
  - Truck
  - Motorcycle  
- Vehicle regions are cropped from labeled images and resized for training

## Test Video

The end-to-end system is tested using real traffic footage.  
Test video link: https://youtube.com/shorts/opPstOQ2KXc?si=xB3mei9KulyE_7vc  

Additional motorway and bridge-view traffic videos are also used for evaluation.

## Method Summary

- Background subtraction (MOG2) is used to detect moving vehicles
- Contours and bounding box filtering remove noise and false detections
- A binary CNN filters non-vehicle detections
- Centroid-based tracking assigns unique IDs to vehicles
- A multi-class CNN predicts vehicle type
- Speed is estimated using centroid displacement over time and calibrated to real-world units

## How to Run

1. Open the provided Jupyter Notebook (`.ipynb`) file.
2. Ensure required libraries are installed (OpenCV, TensorFlow, NumPy, Matplotlib).
3. Update dataset paths if needed.
4. Run the notebook cells sequentially.
5. Output includes annotated video frames and speed logs.

## Output

- Annotated video with:
  - Vehicle ID
  - Vehicle type
  - Estimated speed (mph)
- CSV or printed logs for speed and tracking data

## Course Information

ECE 5831 – Pattern Recognition and Neural Networks  
Final Project

## Authors

- Ashwathi Ashok  
- Tharun Subramanya  
- Vedhesh Aandiyappan Saravanan
