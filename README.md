# YOLO Object Detection Project

A comprehensive object detection project using YOLOv8 for training custom models on annotated datasets. This project includes dataset validation, visualization tools, and automated model training with hyperparameter tuning.

## 🚀 Features

- **Dataset Validation**: Comprehensive validation of image datasets and annotations
- **Bounding Box Visualization**: Interactive plotting of bounding boxes on images
- **YOLOv8 Integration**: State-of-the-art object detection model training
- **Hyperparameter Tuning**: Automated optimization for best model performance
- **Roboflow Integration**: Seamless dataset management and downloading

## Quick Start
```bash
pip install ultralytics roboflow numpy pandas pillow matplotlib
```

```python
from ultralytics import YOLO

# Train model
model = YOLO("yolov8n.yaml")
model.train(data="data.yaml", imgsz=1280, batch=1, epochs=100)
```

## Dataset Structure
```
archive/
├── train/ (images + annotations.csv)
└── valid/ (images + annotations.csv)
```

CSV format: `filename, width, height, xmin, ymin, xmax, ymax`