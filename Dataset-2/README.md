## Implementation Update: Corrected Preprocessing and Updated Training Configuration

After reviewing the released preprocessing pipeline, we updated the filtering implementation to ensure that EEG and EMG filters are applied along the temporal axis after each signal is standardized to `channels × time` format. This update improves the clarity and reproducibility of the preprocessing code.

The NeuroFusion-Trans model architecture remains unchanged from the published paper. The implementation still follows the same core framework:

1. EEG–EMG temporal synchronization using cross-correlation-based alignment
2. Separate Transformer encoders for EEG and EMG
3. Trainable cross-modality attention weights
4. Multi-head attention-based fusion
5. Mean temporal pooling and classification
6. Online adaptation with replay and regularization

Because the preprocessing pipeline was corrected, we also updated the training hyperparameters to improve training stability and reproducibility with the corrected filtered data. These changes are training-configuration updates and do not modify the core NeuroFusion-Trans architecture.

### Updated Hyperparameters Used in the Current Repository

| Hyperparameter | Value |
|---|---:|
| EEG channels | 8 |
| EMG channels | 8 |
| Sampling rate after resampling | 200 Hz |
| Window length | 1000 ms |
| Samples per window | 200 |
| Window overlap | 80% |
| Number of classes | 7 |
| Transformer hidden dimension / `d_model` | 128 |
| Transformer layers | 2 |
| Attention heads | 4 |
| Feed-forward dimension | 256 |
| Dropout | 0.20 |
| Batch size | 32 |
| Learning rate | 0.0005 |
| Weight decay | 0.0001 |
| Maximum epochs | 150 |
| Early-stopping patience | 25 |
| Gradient clipping | 1.0 |
| Initial EEG attention weight | 0.7 |
| Initial EMG attention weight | 0.3 |
| Cross-correlation synchronization | Enabled |
| Maximum synchronization lag | ±50 samples |
| Gaussian noise augmentation | Enabled |
| Amplitude scaling augmentation | Enabled |
| Time-shift augmentation | Enabled |
| Frequency perturbation augmentation | Enabled |
| MixUp / synthetic linear combination | Enabled |
| MixUp alpha | 0.20 |
| Online adaptation samples | 400 |
| Replay samples | 400 |
| Online adaptation cycles | 5 |
| Online batch size | 16 |
| Online learning rate | 0.00001 |
| Online regularization coefficient | 0.01 |

### Note on Reproducibility

The published NeuroFusion-Trans architecture is preserved. However, due to the corrected preprocessing implementation and updated training configuration, the exact numerical results from this repository may differ slightly from the originally reported values. The updated code is intended to provide a cleaner, more stable, and more reproducible implementation of the same proposed method.
