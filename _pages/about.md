---
title: "About"
permalink: /about/
layout: single
author_profile: true
---

I am a robotics perception and machine learning engineer specializing in
computer vision, autonomous driving, 3D geometry, and production-oriented
ML systems.

Before beginning my graduate studies, I worked for seven years as a Research
Engineer at Hyundai Motor Company, developing and validating camera-based
perception systems for autonomous-driving and ADAS applications.

## Education

**University of Illinois Urbana-Champaign** — Champaign, IL  
*Master of Engineering in Autonomy and Robotics*  
Aug 2026 – Expected Dec 2027

Relevant coursework: Computer Vision, Applied Machine Learning, Principles
of Safe Autonomy

**Georgia Institute of Technology** — Remote  
*Online Master's Coursework in Computer Science*  
Aug 2025 – May 2026

Relevant coursework: Robotics: AI Techniques

**Konkuk University** — Seoul, South Korea  
*Bachelor of Science in Electronics Engineering*  
Mar 2015 – Aug 2019

Relevant coursework: Artificial Intelligence, Image Processing, Digital
Signal Processing

## Experience

**Hyundai Motor Company** — Gyeonggi, South Korea  
*Research Engineer, Autonomous Driving Perception Technology*  
Jul 2019 – Jul 2026

- Developed camera-based perception systems for autonomous-driving and
  ADAS applications.
- Worked across object detection, multi-object tracking, camera calibration,
  3D object localization, motion prediction, and perception validation.
- Integrated TensorRT-optimized perception models into ROS2-based
  front-camera systems and validated them through on-vehicle testing.
- Built ML data and evaluation pipelines using Python, PyTorch, Apache
  Airflow, Ray, and Kubernetes.

## Selected Projects

### Scalable Sim-to-Real Monocular 3D Object Localization

Developed geometry-driven data synthesis and monocular 3D object localization
framework that transfers from simulation to real-world driving data.

Designed dual-stream localization network using 2D keypoints, global
bounding-box context, visibility masks, and geometric consistency loss to
estimate object position and orientation.

Achieved 1.49 m longitudinal mean absolute error within 70 m on real-world
driving data using simulation-only training data.

### 2.5D Object Detection and Keypoint Network

Developed YOLOv5-based vehicle perception model combining object detection,
front, rear, and side-view classification, and side-facet keypoint estimation.

The model achieved 0.740 mAP, 0.804 F1 score, and 27.70 ms inference latency
on NVIDIA T4.

Converted the model to TensorRT and integrated the detection and tracking
pipeline into a ROS2-based front-camera system for on-vehicle testing.

### Multi-Object Tracking and Visual Re-Identification

Developed and validated Kalman-filter-based multi-object tracking system,
optimizing track management policies and data association logic through
sequence-level ground truth and MOTA-based quantitative evaluation.

Integrated visual Re-ID features into multi-object data association, improving
MOTA from 33.13 to 40.10 while reducing computational cost by 29.1% through
shared detection and Re-ID features.

### End-of-Line Camera Calibration

Engineered end-of-line front-camera calibration algorithm estimating yaw,
pitch, and roll within 0.0005 degrees of reference values using nonlinear
3D-to-2D projection equations.

Deployed the calibration algorithm for vehicle installation and validation
in an L2 ADAS front-camera perception system.

### End-to-End Motion Prediction

Integrated Mamba-based interaction block into an end-to-end autonomous-driving
motion-prediction model, reducing sequence complexity from O(L^2) to O(L).

Reduced median GPU inference latency from 8.07 ms to 5.60 ms on NVIDIA H100.

Developed CasADi-based trajectory optimizer to generate temporally smooth
ground-truth trajectories from frame-wise 3D object labels.

### Video Anonymization and ML Data Pipeline

Built active-learning video anonymization and continuous-learning pipeline
for privacy-compliant autonomous-driving data processing.

Implemented Apache Airflow workflows and Ray-based distributed inference on
Kubernetes and packaged the anonymization engine as an internally deployable
Python library.

Improved Dice from 89.11% to 92.61% across new vehicle configurations and
unseen driving environments without manual labeling.

### ADAS Parking Perception Validation

Built ADAS parking perception evaluation and failure-analysis tools in C#,
C++, and Python, validating object detection and 3D localization outputs using
camera and LiDAR data.

Projected LiDAR point clouds into the image plane and applied
point-in-polygon filtering to isolate object-associated points for
localization validation.

## Publication

**Scalable Sim-to-Real Monocular 3D Object Localization across Diverse Sensor
Configurations**  
IEEE International Conference on Intelligent Transportation Systems
(ITSC), 2026

## Technical Skills

**Programming:** C++, Python, MATLAB, C#  

**Machine Learning:** PyTorch, YOLOv5, Faster R-CNN, ONNX, TensorRT, Model
Optimization  

**Computer Vision:** Object Detection, Keypoint Detection, Semantic
Segmentation, Camera Calibration, Camera Projection, Coordinate
Transformations, 3D Object Localization  

**Robotics and Estimation:** ROS2, Multi-Object Tracking, Re-Identification,
Kalman Filtering, Data Association, Motion Prediction, Trajectory Optimization  

**Systems and Tools:** Linux, Git, Kubernetes, Apache Airflow, Ray, OpenCV,
PCL, CasADi, SymPy, CUDA Profiling

## Research Interests

- Robotics Perception
- Autonomous Driving
- Computer Vision
- 3D Scene Understanding
- Sim-to-Real Learning
- Motion Prediction
- Human-Centered Autonomy

## Contact

- Email: [jiheeh2@illinois.edu](mailto:jiheeh2@illinois.edu)
- LinkedIn: [Jihee Han](https://www.linkedin.com/in/jihee-han-410459212)
- GitHub: [github.com/jiheehan](https://github.com/jiheehan)
