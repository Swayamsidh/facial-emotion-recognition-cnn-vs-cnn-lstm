<p align="center">
  <img src="assets/project_banner.png" alt="Facial Emotion Recognition - CNN vs CNN+LSTM" width="100%">
</p>

# Facial Emotion Recognition: CNN vs CNN+LSTM for Image and Video Data

A deep learning project for facial emotion recognition using image and video data, with a comparative study of Convolutional Neural Networks (CNN) and CNN+LSTM architectures.

## Overview

This project presents a comparative study of CNN and CNN+LSTM approaches for facial emotion recognition using both static images and video data.

The primary objective is to determine which approach is more suitable for different types of input:

- **CNN for static image-based emotion recognition**
- **CNN+LSTM for sequential video-based emotion recognition**

CNN is effective at learning spatial features from individual facial images or video frames. CNN+LSTM extends this approach by using an LSTM to learn temporal dependencies across consecutive video frames.

The project therefore focuses not only on emotion recognition accuracy, but also on understanding how the nature of the input data affects the suitability of the recognition architecture.

## Objectives

The main objective of this project is to identify the most suitable emotion recognition approach for static images and video sequences.

Specifically, the project aims to:

- Compare CNN and CNN+LSTM approaches for facial emotion recognition.
- Evaluate their performance on image and video data.
- Determine the suitability of CNN for static image recognition.
- Determine the suitability of CNN+LSTM for sequential video recognition.
- Study the importance of temporal information in video-based emotion recognition.
- Evaluate model performance using Accuracy, Precision, Recall and F1-Score.
- Analyze how the nature of the input data influences model performance.
---

## CNN vs CNN+LSTM

### CNN

A Convolutional Neural Network is primarily used to learn spatial features from images or individual video frames.

The convolutional layers learn visual patterns such as:

- Edges
- Textures
- Facial structures
- Expression-related features

CNNs are particularly suitable for static image-based emotion recognition.

### CNN+LSTM

The CNN+LSTM architecture combines:

**CNN → Spatial Feature Extraction**

with

**LSTM → Temporal Sequence Learning**

For sequential video data, CNN extracts meaningful visual features from individual frames and LSTM processes the resulting sequence of features to learn temporal relationships between frames.

This makes CNN+LSTM suitable for video-based emotion recognition where emotional expressions may change across consecutive frames.

---

## Methodology

The overall workflow consists of the following stages:

1. Dataset collection
2. Data preprocessing
3. Face/frame processing
4. Feature extraction
5. Sequence generation for video data
6. Model training
7. Model testing
8. Performance evaluation
9. Comparative analysis

### Image Processing

The image-based pipeline includes preprocessing and preparation of facial images before model training.

The processed images are converted into suitable model inputs through operations such as resizing, normalization and transformation.

### Video Processing

The video pipeline extracts individual frames from video sequences.

The extracted frames are processed and organized into sequential groups before being passed through the CNN+LSTM architecture.

The CNN extracts spatial information from individual frames, while the LSTM learns temporal information across the frame sequence.

---

## Model Training

The models were developed and trained using a GPU-enabled Google Colab environment.

The project uses:

- Python
- PyTorch
- Torchvision
- OpenCV
- NumPy
- Matplotlib
- Scikit-learn

The training process uses:

- Cross-Entropy Loss
- Adam Optimizer
- Training and testing datasets
- Classification performance metrics

---

## Evaluation Metrics

The models are evaluated using standard classification metrics:

### Accuracy

Measures the overall proportion of correctly classified samples.

### Precision

Measures how accurately the model identifies samples predicted as a particular emotion.

### Recall

Measures how effectively the model identifies samples belonging to a particular emotion.

### F1-Score

Provides a combined measure of precision and recall.

### Loss

Measures the difference between the predicted output and the actual target during model training.

---

## Datasets

Two publicly available emotion-recognition datasets were used in the project:

### Human Face Emotions Dataset

Used for image-based facial emotion recognition.

### RAVDESS Emotional Speech Video Dataset

Used for video-based emotion recognition and frame-sequence processing.

The actual datasets are not included in this repository.

Dataset sources and usage information are provided in:

`data/README.md`

---

## Results

### Key Finding

The comparative analysis demonstrates that the most suitable architecture depends on the type of input data.

| Input Type | Preferred Approach | Main Reason |
|---|---|---|
| Static Images | **CNN** | Effective spatial feature extraction |
| Video Sequences | **CNN+LSTM** | Captures spatial features and temporal dependencies |

**Conclusion:** CNN is more suitable for static image-based emotion recognition, while CNN+LSTM is more suitable for sequential video-based emotion recognition.

---

## Repository Structure

```text
facial-emotion-recognition-cnn-vs-cnn-lstm/
│
├── README.md
├── requirements.txt
├── .gitignore
│
├── data/
│   └── README.md
│
├── notebooks/
│   ├── cnn_lstm_image.ipynb
│   └── cnn_lstm_video.ipynb
│
└── results/
    └── figures/
        ├── image_accuracy_comparison.png
        └── video_accuracy_comparison.png
