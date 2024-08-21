# Speech-Emotion-Recognition
## Overview
This project aims to build a speech emotion recognition system using audio features extracted from the Urdu Language Speech Dataset. The project leverages the VGGish model pre-trained on the AudioSet dataset for feature extraction, combined with MFCC features, and uses a Support Vector Machine (SVM) for classification.

## Dataset
The dataset used in this project is the Urdu Language Speech Dataset, which contains audio files labeled with different emotions:

Angry
Happy
Neutral
Sad
## Code Description
### 1. Load and Prepare Dataset
The code begins by loading the paths of the audio files and their corresponding labels from the specified directory structure. It handles .wav files located in class-specific folders.

### 2. Audio Preprocessing
Sampling Rate: The audio is resampled to 16 kHz to match the input requirements of the VGGish model.
Audio Trimming: Each audio file is trimmed or padded to ensure a consistent length (1.6 seconds).
### 3. Feature Extraction
VGGish Features: The VGGish model from TensorFlow Hub is used to extract high-level audio features.
MFCC Features: Mel-frequency cepstral coefficients (MFCCs) are extracted to capture additional audio characteristics.
### 4. Feature Normalization and Label Encoding
Normalization: The extracted features are normalized using StandardScaler to ensure uniformity.
Label Encoding: The emotion labels are encoded into numerical format using LabelEncoder.
### 5. Model Training and Evaluation
- SVM Model: A Support Vector Machine (SVM) with an RBF kernel is trained on the extracted features.
- Evaluation: The model's performance is evaluated using accuracy and a classification report on the test set.
## Requirements
TensorFlow
TensorFlow Hub
NumPy
Librosa
Scikit-learn
