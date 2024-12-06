# Human Activity Recognition Using Multimodal Fusion

This repository contains the implementation of our project: **"Human Activity Recognition Using Multimodal Fusion"**, which aims to classify human activities by combining video and audio data. The project evaluates different fusion techniques—early, mid, and late—to determine the optimal approach for integrating multimodal data effectively.

## Table of Contents
- [Introduction](#introduction)
- [Dataset](#dataset)
- [Approach](#approach)
  - [Fusion Techniques](#fusion-techniques)
- [Results](#results)
---

## Introduction
Action recognition is a crucial task in fields like surveillance, sports analytics, and human-computer interaction. However, traditional methods relying solely on video data often struggle with challenges like occlusion, noisy environments, or ambiguous visual cues. This project leverages **multimodal fusion** of video and audio data to improve accuracy and robustness in human activity recognition.

---

## Dataset
The project utilizes the **UCF-51 dataset**, a subset of the UCF-101 dataset, containing synchronized video and audio data across 51 action classes. This dataset is ideal for evaluating the integration of multimodal inputs.

- **Video Modality**: Frames from video sequences.
- **Audio Modality**: Spectrograms generated from audio tracks.

For preprocessing:
- Video frames are resized and normalized.
- Audio spectrograms are extracted using the Librosa library.

---

## Approach
Our methodology consists of:
1. **Data Preprocessing**: Extracting features from video frames and audio spectrograms.
2. **Individual Modality Models**: Training separate models for video and audio.
3. **Fusion Techniques**: Exploring three fusion strategies to combine modalities.

### Fusion Techniques
- **Early Fusion**: Combines features at the input layer for joint processing.
- **Mid Fusion**: Processes each modality independently before merging at an intermediate layer.
- **Late Fusion**: Uses separate models for each modality, combining their outputs via a meta-classifier.


## Results
The project demonstrates the effectiveness of multimodal fusion in improving human activity recognition. Among the fusion techniques, Mid Fusion was identified as the most balanced approach, effectively leveraging the strengths of both video and audio modalities.
