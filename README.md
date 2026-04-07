# CCTV Violence and Weapon Detection using YOLOv8m

This project implements YOLOv8m (You Only Look Once v8 Medium) for detecting violent activities and weapons in CCTV footage. The model is fine-tuned on a custom-built surveillance dataset designed specifically for real-world security monitoring scenarios.

The system aims to assist automated surveillance systems by detecting suspicious activities and weapon presence in real time.

# Project Overview

Monitoring CCTV cameras manually is inefficient and prone to human error. This project presents an AI-based real-time object detection system capable of identifying:

Violent activities
Weapons
Normal background scenes

By using a fine-tuned YOLOv8m model, the system can detect threats directly from surveillance footage and support smart security systems.

# Dataset Description

A custom CCTV dataset was created and curated for this project to simulate real-world surveillance scenarios.

Dataset Size
Total Images: ~8,000 images
Split: Training, Validation, and Test sets
Classes

The dataset contains three classes:

Weapon
Knife
Gun
Rifle
Blunt weapons
Other weapon-like objects
Violence
Fighting
Snatching
Physical assault
Aggressive human interactions
Background
Scenes with no violence or weapons
Annotation files are empty .txt files
Annotation Format

# Annotations follow the YOLO format:

class_id x_center y_center width height

Each image has a corresponding .txt label file.

# Model Architecture

This project uses YOLOv8m, a modern and efficient object detection model developed by Ultralytics.

# Key characteristics:

Single-stage object detector
Anchor-free detection mechanism
Multi-scale feature learning
High-speed real-time inference
Optimized for GPU acceleration

YOLOv8m offers a balanced trade-off between speed and accuracy, making it ideal for real-time surveillance applications.

# Data Augmentation

To improve model robustness on low-quality and diverse CCTV footage, a strong augmentation pipeline was implemented using Albumentations.

# Augmentation techniques include:

Horizontal flipping
Random scaling
Random cropping
Rotation
Brightness and contrast adjustments
Blur and noise simulation
Color transformations

These augmentations help the model learn robust visual features from challenging surveillance environments, including:

Low resolution images
Poor lighting conditions
Motion blur
Occlusions
Training Strategy

The YOLOv8m model was fine-tuned on the custom CCTV dataset using transfer learning.

# Training steps include:

Loading pretrained YOLOv8m weights
Preparing dataset with YOLO annotations
Applying augmentation pipeline
Fine-tuning the model on custom classes
Evaluating performance on validation and test sets
