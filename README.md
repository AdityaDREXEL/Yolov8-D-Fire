Wildfire Detection using YOLOv8
This project utilizes Ultralytics YOLOv8 for detecting wildfire-related elements (e.g., fire, smoke) in real-time image and video streams. The goal is to build an accurate and efficient object detection model that can aid in early wildfire detection and disaster response.


wildfire-detection-yolov8/
├── data/
│   ├── images/            # Training and validation images
│   └── labels/            # YOLO format labels for each image
├── runs/                  # Training output directory
├── yolov8s.pt             # Pretrained YOLOv8 model (small variant)
├── wildfire.yaml          # Dataset config file
├── train.py               # Script to launch training
├── detect.py              # Inference script on images/videos
└── README.md              # Project documentation

Model Overview
Architecture: YOLOv8 (small variant yolov8s)

Framework: Ultralytics YOLO

Task: Object Detection (Fire, Smoke)

Training Backend: PyTorch


dataset/
├── images/
│   ├── train/
│   └── val/
├── labels/
│   ├── train/
│   └── val/



path: ./dataset
train: images/train
val: images/val

names:
  0: fire
  1: smoke


Hyperparameter Tuning
You can experiment with:

lr0, lrf – learning rate and its final value

batch – batch size

imgsz – image size

weight_decay, momentum, optimizer

Data augmentations: mosaic, hsv_h, flipud, etc.

Author
Aditya Sinha
M.S. in Data Science @ Drexel University
Research Assistant, Urban Health Collaborative
Contact: as5869@drexel.edu
