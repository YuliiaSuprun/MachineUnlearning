# MachineUnlearning

This repository contains a Jupyter notebook that showcases the local scoring system developed for the MUFAC (Machine Unlearning for Facial Age Classifier) dataset as part of a machine unlearning project. It also contains the results of all experiments, used in the project.

## Overview

The notebook demonstrates the evaluation of various unlearning methods and their impact on a pre-trained ResNet-18 model's ability to "forget" certain data points while maintaining overall performance.

## Dataset

The MUFAC dataset includes over 13,000 images of Asian facial features, annotated with age group classifications. It is sourced from AI HUB in South Korea and is used here to simulate the conditions of the NeurIPS'23 competition track on machine unlearning.

## Methods Evaluated

The following unlearning methods are evaluated in the notebook:
1. Simple Fine-tuning on the Retain Set
2. Advanced NegGrad
3. Selective Synaptic Dampening (SSD)
4. Gradient-Informed Synaptic Adjustment (GISA) -- main contribution of the project!
5. Competent/Incompetent Teachers
6. Competent/Incompetent Teachers with Similarity-based Sampling: [refer to this Kaggle discussion post](https://www.kaggle.com/competitions/neurips-2023-machine-unlearning/discussion/458648)
7. Contrastive Fine-tuning (2nd place in the Kaggle competition): [refer to this Kaggle discussion post](https://www.kaggle.com/code/fanchuan/2nd-place-machine-unlearning-solution)

## Evaluation Procedure
The code for the scoring function was adopted from [Maria Gorinova's Kaggle post](https://www.kaggle.com/code/mgorinova/machine-unlearning-evaluation-on-cifar-10).

## Results

The notebook includes a detailed analysis of the results, comparing the accuracy, forgetting quality, and overall performance of each method.

## Getting Started

To get started with the notebook:
1. Clone the repository.
2. Install the necessary dependencies listed in the notebook.
3. Run the Jupyter notebook to see the results and analysis.

**Note**: you don't have to retrain the models from scratch; you can just use the provided checkpoints for the "original" and "retrained-from-scratch" models. 
