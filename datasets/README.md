
# Dataset Information

This project uses two datasets to simulate an AI-driven adaptive traffic signal system for emergency vehicle prioritization.

## 1. Traffic Vehicle Dataset
Dataset Name: UA-DETRAC-10K  
Source: Roboflow

Purpose:
- Detect vehicles in traffic scenes
- Count vehicles in each lane
- Estimate traffic density

The dataset contains labeled traffic images with bounding boxes for vehicles such as cars, buses, vans, and trucks.

## 2. Emergency Vehicle Dataset
Dataset Name: Emergency Vehicle Detection Dataset  
Source: Roboflow

Purpose:
- Detect emergency vehicles such as ambulances, police cars, and fire trucks
- Provide priority to emergency vehicles in the traffic signal scheduling algorithm.

## Dataset Usage
Datasets are not stored directly in this repository because they are large.  
Instead, they are downloaded dynamically using the Roboflow API when running the notebook in Google Colab.

This ensures that all collaborators can access the same dataset without storing large files in the reposito
