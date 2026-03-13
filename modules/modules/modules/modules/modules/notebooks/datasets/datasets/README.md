

Datasets Used

This project uses two datasets for implementing the AI-driven adaptive traffic signal system.

1. Traffic Vehicle Dataset

Dataset: UA-DETRAC-10K
Source: Roboflow

Purpose:
	•	Detect vehicles in traffic scenes
	•	Count vehicles per lane
	•	Estimate traffic density

This dataset contains labeled images of vehicles such as cars, buses, vans, and trucks captured from traffic surveillance cameras.

2. Emergency Vehicle Dataset

Dataset: Emergency Vehicle Detection Dataset
Source: Roboflow

Purpose:
	•	Detect emergency vehicles such as ambulances, police cars, and fire trucks
	•	Assign higher priority to emergency vehicles in the traffic scheduling algorithm.

Dataset Usage

Datasets are not stored inside this repository because they are large.
Instead, they are downloaded dynamically in the notebook using the Roboflow API.

Example loading code in the notebook:!pip install roboflow

from roboflow import Roboflow
rf = Roboflow(api_key="YOUR_API_KEY")

project = rf.workspace("workspace-name").project("ua-detrac-dataset-10k")
dataset = project.version(1).download("yolov8")
Project Pipeline Using the Dataset

Traffic Frame
↓
Vehicle Detection (YOLO)
↓
Lane Division
↓
Vehicle Count per Lane (Traffic Density)
↓
Emergency Vehicle Detection
↓
Priority Scheduling Algorithm
↓
Green Signal Decision

