# NeuroFusion-Trans

**NeuroFusion-Trans: A Novel Transformer-Based EEG-EMG Fusion Model for Assistive Robotics**  
*Accepted at IEEE Access 2025*  

---

##  Overview

NeuroFusion-Trans is a transformer-based framework for upper-limb gesture recognition using EEG and EMG signals. It enhances user intent decoding for assistive robotics by:

- Dynamically synchronizing neural (EEG) and muscular (EMG) signals  
- Learning cross-modal dependencies through **cross-modality attention**  
- Adapting to user-specific signal changes via **online learning**

---

## Key Contributions

- **Temporal Synchronization**: Resampling + FFT-based cross-correlation  
- **Cross-Modality Attention**: Learns joint EEG-EMG feature space  
- **Online Adaptive Learning**: Updates model on-the-fly per user  

**Results**:  
- Dataset 1: **97% accuracy**, Cohen's Kappa = **0.97**  
- Dataset 2: **96% accuracy**, Cohen's Kappa = **0.95**

---

## Datasets

This repository uses **two publicly available datasets**:

- **Dataset 1**: [EMG-EEG Dataset for Upper-Limb Gesture Classification (IEEE DataPort)](https://ieee-dataport.org/documents/emg-eeg-dataset-upper-limb-gesture-classification)  
  - 33 subjects | 7 gestures | EEG: 8 ch (250 Hz), EMG: 8 ch (200 Hz)  

- **Dataset 2**: [8-Channel EMG-EEG Upper-Limb Gesture Data (Mendeley)](https://data.mendeley.com/datasets/m6t78vngbt/1)  
  - 11 subjects | 7 gestures + MI | EEG: 8 ch, EMG: 8 ch



---

## Model Architecture

- Dual transformer encoders for EEG and EMG  
- Cross-modal fusion layer  
- Final classification + real-time online learning



<p align="center">
  <img src="trans.png" width="500"/>
  <br>
  <em>Figure: Architecture of the NeuroFusion-Trans Transformer Model for Intent Recognition.</em>
</p>

---

## Results Summary

| Model              | Accuracy (D1) | Accuracy (D2) |
|-------------------|---------------|---------------|
| NeuroFusion-Trans | **97%**       | **96%**       |
| CNN-LSTM          | 25%           | 47%           |
| GRUNet            | 60%           | 63%           |
| ShallowConvNet    | 61%           | 62%           |

---

### 1. Citation

```bash

@ARTICLE{11028041,
  author={Sultan, Tipu and Liu, Guangping and Sikorski, Pascal and Alshathri, Samah and El-Shafai, Walid and Babaiasl, Madi},
  journal={IEEE Access}, 
  title={NeuroFusion-Trans: A Novel Transformer-Based EEG-EMG Fusion Model for Assistive Robotics}, 
  year={2025},
  volume={},
  number={},
  pages={1-1},
  keywords={Brain modeling;Electromyography;Electroencephalography;Adaptation models;Real-time systems;Synchronization;Accuracy;Transformers;Robots;Gesture recognition;Transformer;Cross-modality attention;Online learning;Gesture recognition;Assistive robotics;Temporal synchronization},
  doi={10.1109/ACCESS.2025.3577996}}


