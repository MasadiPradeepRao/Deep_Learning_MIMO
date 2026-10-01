# Deep_Learning_MIMO

## Overview

This project explores deep-learning-based beamforming for wireless multiple-input multiple-output (MIMO) systems. It brings together ray-tracing-based channel generation, beamforming codebooks, and machine-learning tools for preparing data, training models, and studying beam-prediction performance.

The MATLAB component uses the DeepMIMOv2 dataset to construct channel information for selected users and base stations. The Python notebook contains supporting channel and beamforming examples, neural-network training code, and visualizations of system and learning metrics.

## Architecture

The project is organized around the following workflow:

1. **Scenario data** — Download a DeepMIMOv2 ray-tracing scenario and make it available to MATLAB.
2. **Channel and dataset generation** — Configure the scenario, users, base stations, antenna arrays, and OFDM settings. MATLAB reads the ray-tracing data and builds channel matrices and related channel information.
3. **Beamforming assets** — Use antenna/codebook definitions and their parameters to represent candidate beams for the learning task.
4. **Learning workflow** — Prepare model inputs and beam targets, then use Python machine-learning code to train and evaluate beam-prediction models.
5. **Evaluation** — Review predicted beams and system metrics through the notebook's visualizations and generated results.

The MATLAB implementation is in `DeepLearning_MIMO/`. Its parameter file configures the channel-generation scenario, and `DeepLearning_MIMO_functions/` contains the supporting readers, channel construction, antenna, parameter-validation, and plotting functions. `Hybrid_Deep_learning.ipynb` provides the Python-based beamforming and learning examples.

## Requirements

- MATLAB for channel and dataset generation
- Python 3.7 for the Python learning workflow
- Keras and TensorFlow
- The DeepMIMOv2 scenario data used by the selected MATLAB parameters

## Getting Started

### 1. Download a DeepMIMOv2 scenario

Download the [O1 scenario](https://deepmimo.net/scenarios/o1-scenario/) or another supported scenario. Extract the data locally.

### 2. Prepare MATLAB

Open MATLAB and add the DeepMIMOv2 folder and its subfolders to the MATLAB path. You can use MATLAB's **Add to Path → Selected Folders and Subfolders** option, or add the path from a script:

```matlab
addpath(genpath('deepmimov2_folder_directory'))
```

### 3. Configure and generate channel data

Review `DeepLearning_MIMO/parameters.m` to choose the scenario and simulation settings. Run the MATLAB dataset-generation entry point, `DeepLearning_MIMO/DeepMIMO_Dataset_Generator.m`, to construct the channel dataset.

### 4. Explore beamforming and learning

Open `Hybrid_Deep_learning.ipynb` in Jupyter to review the beamforming examples, model-training code, and visualizations. The learning workflow uses prepared channel and beam data as model inputs and targets.

## Architecture Diagram

An architecture diagram can help readers see how scenario data flows through channel generation, dataset preparation, model training, and beam-prediction evaluation. To include the supplied diagram, add the image to the repository (for example, as `docs/architecture.png`) and embed it here:

```markdown
![Deep learning MIMO project architecture](docs/architecture.png)
```

## Project Highlights

- Uses ray-tracing-based DeepMIMO channel information as the foundation for MIMO experiments.
- Exposes key scenario, antenna, and OFDM settings through a MATLAB parameter file.
- Includes channel construction and antenna utilities for building channel datasets.
- Brings beamforming codebook concepts together with neural-network training examples.
- Provides visualizations to explore beam prediction and communication-system performance.
