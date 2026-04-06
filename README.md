# Forest-Fire-Detection-System

## Introduction:

Forest fires are among the most devastating natural disasters, causing severe environmental damage, loss of wildlife, and threats to human life and property. Early detection of fire and smoke is critical to minimize these losses and enable quick response from authorities.With the advancement of artificial intelligence and computer vision, deep learning models can now automatically detect fire and smoke in images and videos with high accuracy.
This project uses a deep learning–based object detection approach to build an automated forest fire detection system.


## Project Overview:

This project implements a Forest Fire and Smoke Detection System using the YOLOv8n object detection model. The system is trained on a dataset containing annotated images of fire, smoke, and normal forest scenes. Once trained, the model can analyze images to identify potential fire and smoke incidents.
The primary aim of this project is to design a reliable and fast detection model that can be used in surveillance systems, drones, or monitoring stations for early warning and disaster management.


## Project Objectives:

- Detect fire and smoke in forest environments automatically
- Reduce response time for fire control authorities
- Build a real-time detection system using deep learning
- Train a model using a labeled dataset

## Model Used-Yolov8n:

YOLO (You Only Look Once) is a object detection algorithm that detects objects .Features includes:
- Faster training
- Higher detection accuracy
- Small object detection 
- Easy integration with Python

In this project, the YOLOv8 Nano (yolov8n) model is used because it is lightweight and trains quickly while still providing good accuracy.

## Yolov8n-Layers and Activation Function: 
- YOLOv8n has around 169 layers, but the count may appear higher when individual operations inside modules like C2f are counted separately.
- It uses the Sigmoid Linear Unit activation function in most layers for learning complex patterns, while a Sigmoid function is used in the final layer to generate probability-based detection outputs.

## About the Dataset:

- The dataset contains 21000+ images annotated for two classes: Fire and Smoke, enabling the model to detect both flames and smoke in different environments.
- All annotations are provided in YOLO format, where each image has a corresponding .txt file with bounding box coordinates and class labels.
- The dataset is organized into train, validation, and test folders, making it directly compatible with YOLOv8 training workflows.
- Images include diverse scenarios such as varying lighting conditions, backgrounds, and fire intensities, which helps improve model generalization.

  Here's the link: https://www.kaggle.com/datasets/sayedgamal99/smoke-fire-detection-yolo


##  About Training:

- The YOLOv8n model was trained using a pre-annotated fire and smoke dataset obtained from Kaggle.
- The model was trained for 50 epochs, meaning it learned from the entire dataset 50 times to improve its accuracy.
- Images were resized to 640 × 640 pixels and trained in batches of 16 images at a time.
- The dataset configuration was provided through a data.yaml file, which specified the paths to training and validation images and the class names fire and smoke.
- After training, the model saved its best weights and training results automatically, which can be used later for testing and prediction.

 ## About Validation:
 
- The trained model was loaded using the best saved weights (best.pt) generated after training.
- Validation was performed on images from the validation dataset to evaluate how well the model detects fire and smoke on unseen data.
- The model predicted bounding boxes, class labels, and confidence scores for each detected object using the Ultralytics YOLOv8n model for randomly selected images from the validation folder.
- The final annotated images were displayed using Matplotlib to visually inspect the model’s detection performance and accuracy.
- Performance was measured using standard object detection metrics including precision, recall, F1-score, and mean Average Precision (mAP@0.5).
- Class-wise metrics were calculated separately for fire and smoke to understand how well the model performs on each category and overall average metrics were also computed to provide a summary of the model’s performance.
- Final model accuracy was estimated from the overall mAP score and displayed as a percentage which is 76.98%

  
  <img width="345" height="147" alt="image" src="https://github.com/user-attachments/assets/c36ca505-dbae-4533-86b7-d22cc822daef" />
 

