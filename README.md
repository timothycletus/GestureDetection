# Gesture Detection with MediaPipe

A machine learning project for detecting hand gestures (swipe left, swipe right, rotate) using MediaPipe Pose estimation.

## Project Overview

This project extracts body pose landmarks from video recordings using MediaPipe, processes the data, and prepares it for gesture classification. The preprocessing pipeline includes:

- Video processing with MediaPipe Pose
- ELAN annotation loading for ground truth labels
- Frame resampling to consistent FPS
- Feature engineering (velocity, relative positions)
- Data cleaning and smoothing

## Dataset

- **12 videos** from 5 different people
- **3 gestures**: Left Swipe, Right Swipe, Rotate
- **~6,900 frames** total
- Annotations created using ELAN software

## Project Structure

```
gesturedetect/
├── midtermsubmission.ipynb    # Main notebook with preprocessing pipeline
├── requirements.txt           # Python dependencies
├── data/
│   ├── Videos/               # Video recordings
│   ├── Text_Annotations/     # ELAN annotation files
│   ├── labeled_landmarks.csv # Raw extracted landmarks
│   └── preprocessed_landmarks.csv  # Processed data
└── env/                      # Virtual environment (not tracked)
```

## Preprocessing Steps

1. **E01**: Video processing and annotation loading
2. **E02**: Data analysis (FPS, variance, movement patterns)
3. **E03**: Findings documentation
4. **E04**: Resampling to 15 FPS
5. **E05**: Remove unnecessary features (face, lower body)
6. **E06**: Additional preprocessing:
   - Label cleaning
   - Relative position features
   - Velocity features
   - Missing value handling
   - Data smoothing

## Setup

```bash
# Create virtual environment
python3 -m venv env
source env/bin/activate

# Install dependencies
pip install -r requirements.txt

# Run Jupyter
jupyter notebook
```

## Requirements

- Python 3.10+
- OpenCV
- MediaPipe
- Pandas
- NumPy
- Matplotlib
- Jupyter

## Author

Timo
