# Gender and Age Detection Using OpenCV

This project demonstrates a Python-based implementation for detecting gender and age from images or live video streams using OpenCV and pre-trained deep learning models.

---

## Table of Contents
- [Introduction](#introduction)
- [Technologies Used](#technologies-used)
- [Project Objective](#project-objective)
- [Dataset Information](#dataset-information)
- [How It Works](#how-it-works)
- [Requirements](#requirements)
- [Setup and Installation](#setup-and-installation)
- [Usage](#usage)
- [Output Examples](#output-examples)
- [Contributing](#contributing)
- [License](#license)

---

## Introduction

Gender and Age Detection is an exciting application of deep learning and computer vision. This project uses a Convolutional Neural Network (CNN) to estimate a person's gender and classify their age into predefined age groups from an image or video feed.

---

## Technologies Used

- **Python**: Programming language.
- **OpenCV**: For image processing and face detection.
- **Deep Learning Models**: Pre-trained models for gender and age classification.
- **Argparse**: For command-line argument parsing.

---

## Project Objective

To build a system that:
1. Detects faces in an image or video.
2. Classifies gender as Male or Female.
3. Classifies age into one of the following ranges:
   - (0–2)
   - (4–6)
   - (8–12)
   - (15–20)
   - (25–32)
   - (38–43)
   - (48–53)
   - (60–100)

---

## Dataset Information

This project uses the **Adience dataset**, a publicly available benchmark dataset for facial images under real-world conditions. The dataset contains:
- **26,580 images**
- **2,284 subjects**
- Various lighting, noise, and pose conditions.

Learn more about the dataset [here](https://talhassner.github.io/home/projects/Adience/Adience-data.html).

---

## How It Works

1. **Face Detection**: Uses a DNN-based face detector from OpenCV.
2. **Feature Extraction**: Applies pre-trained models for gender and age classification.
3. **Classification**: Uses softmax layers to classify gender and age.
4. **Results Visualization**: Annotates the input image with predictions.

### CNN Architecture
- **3 Convolutional Layers**:
  - Layer 1: 96 nodes, kernel size 7
  - Layer 2: 256 nodes, kernel size 5
  - Layer 3: 384 nodes, kernel size 3
- **2 Fully Connected Layers**:
  - Each with 512 nodes.
- **Output Layer**:
  - Gender (Male/Female)
  - Age (8 classes)

---

## Requirements

Install the following Python libraries:
- OpenCV (`opencv-python`, `opencv-contrib-python`)
- NumPy
- Argparse

---

## Setup and Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/gender-age-detection.git
   cd gender-age-detection
