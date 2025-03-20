# NeuroFusion-Trans

Welcome to the repository for the **NeuroFusion-Trans** paper, titled **"From Thought to Motion: NeuroFusion-Trans for Assistive Robotics"**, submitted to ICML 2025. This repository contains all the resources and code used in our research, including data processing, proposed model implementation, and comparisons with traditional and deep learning methods.

## Datasets

We used two datasets for our study:

1. **Dataset 1**: EMG-EEG dataset for upper-limb gesture classification.
2. **Dataset 2**: 8-channel EMG-EEG upper-limb gesture dataset.

Both datasets include raw data, preprocessing scripts, and classification results using the NeuroFusion-Trans model, as well as deep learning and traditional machine learning baselines.

## Repository Structure

The repository is organized as follows:

### `Dataset-1 and 2.zip`

This zip file contains two directories:

1. **Dataset1**
   - `data_cleaning/`: Code for preprocessing and cleaning the Dataset 1.
   - `proposed_model/`: Implementation of the NeuroFusion-Trans model for Dataset 1.

 

2. **Dataset2**
   - `data_cleaning/`: Code for preprocessing and cleaning the Dataset 2.
   - `proposed_model/`: Implementation of the NeuroFusion-Trans model for Dataset 2.


## How to Use

1. **Extract the zip file**:
   ```
   unzip Dataset-1 and 2.zip
   ```

2. Navigate to the respective dataset directory (`Dataset1` or `Dataset2`) to access the desired functionality:
   - Preprocessing scripts are in `data_cleaning/`.
   - The NeuroFusion-Trans model code is in `proposed_model/`.
   - Deep learning and traditional ML codes are in their respective directories.

3. Follow the instructions in each subdirectory's README (if available) to run the code.

## Requirements

The project requires the following dependencies:
- Python 3.8+
- TensorFlow or PyTorch
- NumPy
- Pandas
- Scikit-learn
- Matplotlib



## Results

The results of our experiments, including the performance of the NeuroFusion-Trans model compared to baseline methods, are discussed in the paper. Refer to the `results/` directory in each dataset folder for detailed metrics and visualizations.

## Citation

If you use our work, please cite:

```bibtex
@article{your_paper,
  title={NeuroFusion-Trans: A Cross-Modality Attention and Online Adaptive Model for Real-Time User Intent Recognition for Assistive Robotics},
  author={Your Name and Collaborators},
  journal={ICML 2025},
  year={2025}
}
```

