# Deep_Learning_MIMO

## Overview

This repository provides the scripts to process the **DeepMIMOv2 dataset** and build, train, and test a deep learning model using the generated data. Follow the steps below to reproduce the results.

## Requirements

- **MATLAB** (for data generation)
- **Python 3.7** (for building and training the model)
  - Keras
  - TensorFlow

## Steps to Reproduce

### 1. Download the DeepMIMOv2 Dataset
Download the dataset from the following [link](https://deepmimo.net/scenarios/o1-scenario/).

### 2. Download the Repository Files
Download the required files from this repository.

### 3. Generate Input/Output Data for Deep Learning Model
To generate the input and output data for the model:

- Open **MATLAB**.
- Run the script `Generate_DL_data.m`.

Ensure that the **DeepMIMOv2 folder** and its subfolders are added to the MATLAB path by either:
- Right-clicking the DeepMIMOv2 folder in the MATLAB explorer:  
  `Add to Path -> Selected Folders and Subfolders`, or
- Adding the following command at the beginning of the script:
  ```matlab
  addpath(genpath('deepmimov2_folder_directory'))

