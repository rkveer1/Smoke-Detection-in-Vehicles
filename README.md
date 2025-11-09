# Vehicle Smoke Emission Detection System

This project aims to detect smoke-emitting vehicles using Object Detection (YOLO) to support pollution control and enable greener and sustainable transportation. It identifies vehicles in real-time from video feeds, laying the foundation for detecting harmful smoke emissions in upcoming development phases.

## Week 1 Progress 
- Finalized project idea and problem statement
- Decided the tech stack (Python, YOLOv8, OpenCV)
- Created initial folder structure and GitHub repository
- Basic YOLO setup added for vehicle detection (to be enhanced in Week 2)

## Tech Stack
- Python
- YOLOv8
- OpenCV
- NumPy

Week 2 Milestone

Dataset prepared, annotations organized, initial training completed, and inference tested on sample images. The repository includes scripts and steps to reproduce training and inference results.

Key Features

YOLOv8-based object detection for vehicles and smoke

Structured project layout with dedicated scripts for training, inference, and evaluation

Works on both CPU and GPU environments

Fully reproducible setup using requirements.txt

Command-line and Python script-based execution support

Project Structure Smoke-Detection-in-Vehicles/ │ ├── src/ │ ├── train.py # Training wrapper for Ultralytics YOLO │ ├── infer.py # Run inference on images/videos │ ├── evaluate.py # Model validation and metric evaluation │ └── init.py │ ├── datasets/ │ └── smoke/ # Custom dataset (YOLO format) │ ├── data.yaml │ ├── train/ │ │ ├── images/ │ │ └── labels/ │ ├── val/ │ │ ├── images/ │ │ └── labels/ │ └── test/ # Optional │ ├── images/ │ └── labels/ │ ├── results/ # Training and inference outputs ├── README.md └── requirements.txt

Running Inference

Run prediction on a single image or an entire folder: yolo predict model="runs/train//weights/best.pt"
source="path/to/image_or_folder" save=True

Model Validation Using YOLO CLI: yolo task=detect mode=val model="runs/train//weights/best.pt"
data=datasets/smoke/data.yaml Using script: python src/evaluate.py --weights runs/train//weights/best.pt
--data datasets/smoke/data.yaml

Results (Sample Outputs) results/ ├── sample_train_batch.jpg └── sample_prediction.jpg


<img width="1536" height="1024" alt="ChatGPT Image Nov 10, 2025, 04_00_39 AM" src="https://github.com/user-attachments/assets/b85ba6df-deb9-44d7-83fe-14089f22fcb0" />
