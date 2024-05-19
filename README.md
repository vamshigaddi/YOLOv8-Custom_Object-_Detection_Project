# YOLOv8 Custom Object Detection

This project demonstrates how to perform custom object detection using the YOLOv8 model. YOLOv8 is the latest version of the "You Only Look Once" (YOLO) family of models, known for its speed and accuracy in real-time object detection.

## Table of Contents
- [Introduction](#introduction)
- [Features](#features)
- [Dataset structure](dataset-structure)
- [Installation](#installation)
- [Usage](#usage)
- [Model Training](#model-training)
- [License](#license)

## Introduction
YOLOv8 is a state-of-the-art object detection model that can detect multiple objects in real-time with high accuracy. This project provides a pipeline to train YOLOv8 on custom datasets and use the trained model for object detection.

## Features
- High accuracy and real-time object detection
- Customizable training on any dataset
- Easy-to-use interface for model training and prediction
- Generates detailed results in JSON format
## Dataset structure
- This dataset contains both Plastic boxes and rocks. I have downloaded both datasets from the Robolfow and combined those dataset .
- For combining both dataset you can check the jupyter notebook file.
```bash
/path/to/dataset
    /images
        image1.jpg
        image2.jpg
        ...
    /labels
        image1.txt
        image2.txt
        ...
    
    data.yaml
```
## Installation
To set up the project, follow these steps:

1. Clone the repository:

    ```bash
    git clone https://github.com/vamshigaddi/yolov8-custom-object-detection.git
    ```

2. Install the required dependencies:

    ```bash
    pip install ultralytics
    ```

## Usage
### Model Training
To train the YOLOv8 model on your custom dataset, run the following script:

```bash
from ultralytics import YOLO

# Load a model
model = YOLO('yolov8s.pt')  # load a pretrained model (recommended for training)

# Train the model 
results = model.train(data='path to the data.yaml', epochs=10, imgsz=224,plots=True)
```

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

[![MIT License](https://img.shields.io/badge/License-MIT-green.svg)](https://choosealicense.com/licenses/mit/)

