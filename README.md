# Morphological Classification of Galaxies using Deep Transfer Learning
# DeepikaGopi-24099803

## Project Overview
This project investigates the efficacy of Deep Transfer Learning models in the automated morphological classification of galaxies into three primary categories: **Spiral, Elliptical, and Irregular**. Developed at the **University of Hertfordshire**, the research addresses the "Big Data" challenge in astrophysics by comparing **VGG16**, **ResNet50**, and **EfficientNetB0** architectures using the Galaxy Zoo (SDSS) dataset.

## Key Features
* **Specialized Preprocessing**: Custom pipeline using **OpenCV** for **Non-Local Means Denoising** to remove sensor noise while preserving structural edges.
* **Transfer Learning**: Utilizes ImageNet pre-trained weights to leverage general feature extraction, fine-tuned on a specialized "Galaxy Head."
* **Architectural Comparison**: Evaluation of three distinct CNN philosophies: Sequential (VGG16), Residual (ResNet50), and Compound Scaling (EfficientNetb0).
* **Diagnostic Evaluation**: Use of F1-Scores and Confusion Matrices to assess robustness against class imbalance.

## Dataset
* **Source**: Sloan Digital Sky Survey (SDSS) via the Galaxy Zoo Challenge.
* **Resolution**: Preprocessed from 424x424 to 224x224 pixels.
* **Labels**: Crowdsourced consensus probabilities mapped to three morphological classes.

## Results & Findings
* **VGG16**: Demonstrated the highest stability and most consistent generalization for astronomical imagery.
* **ResNet50**: Strong feature extraction but showed higher sensitivity to learning rate fluctuations.
* **EfficientNetB0**: Exhibited performance plateaus, suggesting higher sensitivity to specific astronomical noise profiles.
* **Primary Metric**: The **F1-Score** was utilized to ensure the rare "Irregular" class was accurately evaluated.

## Installation & Environment
* **Language**: Python 3.x
* **Frameworks**: TensorFlow, Keras, OpenCV
* **Environment**: Developed on Google Colab with NVIDIA Tesla T4 GPU.

## Dataset
* **Link**: https://www.kaggle.com/competitions/galaxy-zoo-the-galaxy-challenge/data

### How to Run
1. Clone the repository to your local machine or Colab.
2. Run the preprocessing scripts to denoise the raw imagery.
3. Execute the training notebooks for the specific architecture (VGG/ResNet/EfficientNet).

## Acknowledgments
* **University of Hertfordshire** - School of Physics, Engineering and Computer Science.
* **Sloan Digital Sky Survey (SDSS)** - For original telescope imagery.
* **Galaxy Zoo / Zooniverse** - For the crowdsourced morphological labels.