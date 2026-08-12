# Dataset Information

This project uses publicly available datasets for facial emotion recognition on image and video data.

## 1. Human Face Emotions Dataset

The Human Face Emotions dataset is used for the image-based emotion recognition experiments.

**Dataset:**  
https://www.kaggle.com/datasets/samithsachidanandan/human-face-emotions

### Usage

The dataset is downloaded directly from Kaggle during the image-processing workflow. The images are organized according to emotion classes and are used to train and evaluate the CNN-based image emotion recognition model.

---

## 2. RAVDESS Emotional Speech Video Dataset

The RAVDESS Emotional Speech Video dataset is used for the video-based emotion recognition experiments.

**Dataset:**  
https://www.kaggle.com/datasets/adrivg/ravdess-emotional-speech-video

### Usage

The dataset is downloaded from Kaggle and extracted before video processing. Video frames are extracted and organized into sequences for the CNN+LSTM model.

---

## Dataset-to-Model Mapping

| Input Type | Dataset | Model |
|------------|---------|-------|
| Static Images | Human Face Emotions | CNN |
| Video Sequences | RAVDESS | CNN+LSTM |

## Important

The datasets themselves are **not included in this repository** because of their size.

Please download the datasets directly from their respective Kaggle pages and follow the terms and conditions specified by the dataset providers.

The repository contains the implementation and documentation required to reproduce the experiments after obtaining the datasets.
