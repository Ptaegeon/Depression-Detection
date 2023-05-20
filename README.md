# Depression-Detection

# Multi-modal learning
- Multi-modal (visual, audio, text)를 사용해서 depressed detection 
  - V, A, T -> PHQ-8 score regression (x>10 : depressed)
- Multi-modal (image, text)를 사용해서 sentimental analysis 
  - valence와 erosal의 2-dimensional score regression
  - sentimental intensity [-3,3]

# Reference model
### Multimodal Transformer for Unaligned Multimodal Language Sequences (2019)
![image](https://github.com/Ptaegeon/Depression-Detection/assets/114375142/392398e8-8c6e-474c-b71b-48b18b65fde7)

### TensorFormer: A Tensor-based Multimodal Transformer for Multimodal Sentiment Analysis and Depression Detection (2022)
![image](https://github.com/Ptaegeon/Depression-Detection/assets/114375142/d991cd95-7578-45eb-928c-db57b3d73bd3)

### Multi-Modal Adaptive Fusion Transformer Network for the Estimation of Depression Level (2021)
![image](https://github.com/Ptaegeon/Depression-Detection/assets/114375142/b2fef039-30a3-4add-a778-8b484f9f1e70)

### Multi-modal Depression Estimation based on Sub-attentional Fusion
![image](https://github.com/Ptaegeon/Depression-Detection/assets/114375142/7f321313-97c7-4004-9d96-452f368e8ee4)

### CubeMLP: An MLP-based Model for Multimodal Sentiment Analysis and Depression Estimation
![image](https://github.com/Ptaegeon/Depression-Detection/assets/114375142/e7fd69ee-e5fb-4373-b087-45c9dd277275)

### MLP-Mixer An all-MLP Architecture for Vision (2021)
![image](https://github.com/Ptaegeon/Depression-Detection/assets/114375142/94ad91d6-1a58-4155-8a2b-909213142ffa)

### Continuous Emotion Recognition using Visual-audio-linguistic Information: A Technical Report for ABAW3 (2022)
![image](https://github.com/Ptaegeon/Depression-Detection/assets/114375142/ff0b2dfc-8a62-4c43-ae04-5287a21e4c60)

### It’s Just a Matter of Time: Detecting Depression with Time-Enriched Multimodal Transformers
![image](https://github.com/Ptaegeon/Depression-Detection/assets/114375142/822bb997-f772-4ace-bc9c-f8aedf1892e9)

### A multimodal fusion model with multi-level attention mechanism for depression detection (2023)
![image](https://github.com/Ptaegeon/Depression-Detection/assets/114375142/91ac833e-830a-4dfc-b1b9-e28f3f15fa34)


# Dataset
- Depression 
  - ABEC 2017
  - AVEC 2019 - DDS
  - ABWA3
  - D-vlog

- Sentiment
  - CMU-MOSI
  - CMU-MOSEI 
  - IMOCAP
  - MuSe 2022

# Modal feature
- Visual
  - face landmark : OpenFace-facial behavior analysis toolkit
  - Head Pose, Gaze, AUs
- Audio
  - eGeMAPS : OPenSmile
  - MFCC
- Text
  - BERT
  - GLoVe 
# Data augmentation
- Visual
  - randomly shifting head pose
  - selecting specific sequence data from original sequnce data
- Audio
  - Injecting noise
  - selecting specific sequence data from original sequnce data
- Text
  - back translation
- EEG
  - 1D data augmentation for time seires
  - Data augmentation for Electrocardiogram
- Generating method
  - MixGen

# Traning methods
- Imbalanced data 
  - augmentation : oversampling with augmentation
- Lr : 1e-5
- Bs = 24

# Result
- Depression detection 
  - Depressed : PHQ-8 score > 10, Not-Depressed : PHQ-8 score <= 10
  - F1-score : 0.82
  - MAE Loss : 5.355
