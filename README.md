# Adversarial-Patch-Generation

# Adversarial Patch Generation

This repository contains code for generating adversarial patches designed to fool a pre-trained deep learning model, specifically a ResNet34 model. The adversarial patches are trained to mislead the model into predicting a specified target class when applied to images from the ImageNet dataset (or its smaller variants like TinyImageNet).

## Table of Contents
- [Project Overview](#project-overview)
- [Installation](#installation)
- [Dataset](#dataset)
- [Results](#results)
- [Reference](#reference)

## Project Overview

The goal of this project is to train adversarial patches that can be applied to images and trick a model into predicting a specified target class. Adversarial patches are small, intentionally perturbed regions that can be placed on images to alter the model's predictions.

### Key Features:
- Train adversarial patches using a ResNet34 model pre-trained on ImageNet.
- Evaluate the effectiveness of patches on validation datasets.
- Combine multiple patches to investigate their combined effects.
- Apply transformations like rotation and flipping to test patch robustness.

## Installation

To get started, you need to clone this repository and install the required dependencies.

### Prerequisites
- Python 3.x
- PyTorch
- Torchvision
- Matplotlib
- Seaborn
- tqdm (for progress bars)
- Pytorch
- TorchVision
- pytorch_lightning

### Steps:

1. Clone the repository:
    ```bash
    git clone https://github.com/your_username/adversarial-patch-generation.git
    cd adversarial-patch-generation
    ```

2. Install the dependencies:
    ```bash
    pip install -r requirements.txt
    ```

## Dataset

The project uses the TinyImageNet dataset as a smaller subset of ImageNet. If not already downloaded, the dataset will be automatically fetched from the provided URLs in the code. The dataset is stored in the `data/` directory.

To manually download the dataset:
- TinyImageNet: [Link to Dataset](http://cs231n.stanford.edu/tiny-imagenet-200.zip)

## Results
The project generates adversarial patches that successfully manipulate the model into misclassifying images. The effectiveness of the patch is measured by the model's accuracy and top-5 accuracy after the patch is applied.

Sample results:

- Patch Effectiveness: The patch achieved an accuracy of 5% on a specific target class, meaning it fooled the model into predicting the wrong class in 95% of the cases.
- Patch Combination: Combining two patches (e.g., overlaying) can dilute the effect or enhance the adversarial strength, depending on the method used.

Combining Two Patches
- You can experiment by combining two patches to investigate whether this increases or decreases their effectiveness. The patches can be combined by overlaying (averaging pixel values) or by concatenating them side-by-side. The combination methods are provided in the code, allowing you to analyze the behavior of combined adversarial patches.

## Reference

Github Tutorial by Prof. Bent: [GitHub Link](https://github.com/AIPI-590-XAI/Duke-AI-XAI/tree/main)
