# Dataset Information

This project uses two publicly available datasets for facial emotion recognition.

## 1. Human Face Emotions Dataset

The Human Face Emotions dataset was used for image-based facial emotion recognition.

**Kaggle:**  
https://www.kaggle.com/datasets/samithsachidanandan/human-face-emotions

The dataset contains facial images representing different emotional categories used for the image-based emotion recognition experiments.

## 2. RAVDESS Emotional Speech Video Dataset

The RAVDESS Emotional Speech Video dataset was used for video-based emotion recognition.

**Kaggle:**  
https://www.kaggle.com/datasets/adrivg/ravdess-emotional-speech-video

The video dataset was used for video processing, frame extraction and sequential input preparation for the CNN+LSTM approach.

## Dataset Usage

The datasets are not included in this repository because of their size and dataset distribution/licensing considerations.

Users should download the datasets directly from their respective source pages and follow the terms specified by the dataset providers.

## Preprocessing

Depending on the input type, preprocessing included:

- Image/frame resizing
- Normalization
- Face/frame processing
- Video frame extraction
- Sequence generation for video data
- Preparation of training and testing data

## Dataset-to-Model Mapping

| Input | Dataset | Approach |
|---|---|---|
| Static Images | Human Face Emotions | CNN |
| Video Sequences | RAVDESS | CNN+LSTM |

The purpose of this comparison is to determine which architecture is more suitable for static image emotion recognition and which is more suitable for sequential video emotion recognition.
