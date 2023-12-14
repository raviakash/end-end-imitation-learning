# Autonomous Driving Model Training

This repository contains code for an end-to-end deep learning model for autonomous driving using PyTorch. The model utilizes images and speed data to predict 4 waypoints per forward pass. 

## Data Description
The training data consists of 2 unique 1-minute scenarios:
- Each scenario has corresponding directories for RGB images, speed, and waypoints.
- RGB directory: Contains 120 .png images for each scenario.
- Speed directory: Contains a single NumPy array of shape (120, 1).
- Waypoints directory: Contains a NumPy array of shape (120, 4, 2), where each scenario's waypoints describe 4 positions spaced 0.5s apart from the ego perspective in meters (lateral_distance, longitudinal_distance).

## Data Pipeline
- Data loading and preprocessing are handled in Python scripts.
- The provided Jupyter Notebook demonstrates how to load, preprocess, and create PyTorch data loaders for training.

## Model Architecture
- The model utilizes a Custom CNN for images and an LSTM for speed data to predict waypoints.
- The backbone of the model is based on PyTorch's built-in modules.
- Detailed explanations of the CustomCNN, HybridModel, and training functions are provided in the notebook.

## Files
- `Autonomous_Driving_Model_Training.ipynb`: Jupyter Notebook demonstrating data processing, model creation, training, and evaluation.
- `requirements.txt`: Python packages required to run the code.
- Other Python scripts for data loading, model architecture, and training functions.

## Usage
To use the code:
1. Ensure the necessary Python packages are installed using `pip install -r requirements.txt`.
2. Follow the Jupyter Notebook for step-by-step instructions on data processing, model creation, training, and evaluation.
3. To clone this repository, use the following command: git clone https://github.com/raviakash/end-end.imitation-learning.git

## License
This project is licensed under the [MIT License](LICENSE).
