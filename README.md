# Indoor Object Detection using YOLOv8
## This repository contains a project that implements an indoor object detection model using YOLOv8. The dataset used for training the model is sourced from Roboflow.

## Table of Contents

1. Introduction
2. Dataset
3. Installation
4. Training the Model
5. Evaluation
6. Results
7. Usage

## Introduction
Indoor object detection is an essential task in various applications such as home automation, security, and robotics. This project leverages the YOLOv8 model to detect objects in indoor environments with high accuracy and efficiency.

## Dataset
The dataset used for training the model is obtained from Roboflow, which provides a variety of labeled images for different objects typically found indoors. The dataset includes annotations in the YOLO format, making it compatible with the YOLOv8 training pipeline.

## Installation
To get started with this project, follow these steps:

## Clone the repository:


```
git clone https://github.com/vijay7425/ObjectDetectionUsingYOLOv8.git
cd indoor-object-detection
 ```

## Create a virtual environment and activate it:

```
python -m venv venv
source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
```
## Install the required dependencies:
```
pip install -r requirements.txt
```
## Training the Model

### Download the dataset:

Download the dataset from Roboflow and place it in the data directory. Ensure the dataset is in the YOLO format with the appropriate directory structure.

## Configure the training parameters:

Modify the config.yaml file to set the training parameters, such as batch size, number of epochs, and learning rate.

## Start the training process:

```
python train.py --config config.yaml
```

This command will train the YOLOv8 model on the provided dataset and save the trained weights in the weights directory.

## Evaluation
After training the model, you can evaluate its performance on the validation dataset:

```
python evaluate.py --config config.yaml
```

This script will output various metrics, including precision, recall, and mAP (mean Average Precision), to assess the model's performance.

## Results
The results of the trained model, including evaluation metrics and example predictions, can be found in the results directory. Visualizations of the detected objects in sample images are also provided.

## Usage
To use the trained model for object detection on new images, follow these steps:

Place the images in the input directory.

Run the detection script:

```
python detect.py --weights weights/best.pt --source input
```
This script will output the detected objects and save the results in the output directory.
