# Generative Models - GAN and cGAN

## Overview

This project implements two generative models on tabular data: a Generative Adversarial Network (GAN) and a Conditional Generative Adversarial Network (cGAN). These models are designed to generate synthetic data that mimics real-world data. 

The focus of the assignment is to experiment with generative architectures using the **Adult dataset** in ARFF format.

## Purpose

The primary objective of this project is to:
- Implement a **GAN** that generates synthetic data.
- Implement a **cGAN** that generates synthetic data conditioned on specific labels.
- Evaluate and compare the generated data against the real dataset using detection and efficacy metrics.

## Dataset

The dataset used in this project is the **Adult** dataset in ARFF format, which contains information on individuals' demographic attributes and income levels. The dataset will be split into an 80% training and 20% test set, maintaining label ratios for the "income" target feature.

## Instructions

1. **Preprocessing**: Normalize continuous features and use one-hot encoding for discrete features.
2. **GAN Model**:
   - The generator receives random noise and generates synthetic tabular data.
   - The discriminator attempts to distinguish between real and synthetic data.
3. **cGAN Model**:
   - The generator receives both random noise and an instruction specifying the desired label of the generated sample.
   - The discriminator also receives this instruction along with the real and synthetic samples.
4. **Metrics**:
   - **Detection**: Train a Random Forest model on mixed synthetic and real data, then evaluate it using AUC. Low performance indicates that synthetic data is similar to real data.
   - **Efficacy**: Train a Random Forest on the real training data, evaluate it on the test set, and compare it to the performance on synthetic data. The goal is a high AUC ratio indicating that synthetic data is a good substitute for the real data.

## Evaluation

- **Training Process**: Record details of training such as epochs, loss functions, learning rates, and optimizers.
- **Visualization**: Generate histograms and correlation matrices comparing the distributions of real vs synthetic data.
- **Results**: Report on AUC scores for detection and efficacy.

## Requirements

- **PyTorch**: For building and training the models.
- **Libraries**: 
  - `matplotlib` for visualizations
  - `seaborn` for additional visualizations
  - `scikit-learn` for Random Forest and metrics
  - `pandas` for data handling
- **Dataset**: **Adult dataset** in ARFF format (provided).

## Submission

Submit the project as a single ZIP file containing:
1. **Jupyter notebook** with the code and results.
2. **PDF report** detailing the methods, results, and analysis.

## Contact

For any questions or clarifications, feel free to contact the course instructors.
