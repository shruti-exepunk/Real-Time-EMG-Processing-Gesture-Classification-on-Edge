# Real-Time-EMG-Processing-&-Gesture-Classification-on-Edge
A complete , self-contained pipeline for real-time surface EMG signal acquisition, processing and hand gesture classification - running entirely on an Arduino UNO R3 and Raspberry Pi without any cloud dependency.

## Overview
Surface Electromyography (EMG) measures the electrical activity of muscle during contraction. This project captures those signals from the forearm, extracts time-domain features and classifies hand gestures in real time using classical machine learning.

## Gestures Classified
- Class 1 -- Rest
- Class 2 -- Fist
- (Wrist Flexion and Wrist Extension attempted in 4 - class pipeline)

## Requirements
python>=3.8
scikit-learn
numpy
pandas
matplotlib
scipy
pyserial

## Key Findings
-**ANOVA channel selection** identified channel17 as the most discriminative among 8 EMG channels
-**MAV + WL** account for 79.5% of total classification power
-All 3 classifiers hit identical 5-fold CV accuracy of 95.32% - performance is feature-limited not model-limited
-Single channel is sufficient for binary classification but insufficient for 4-class 

## Limitations
- Single channel limits reliable classification to binary gesture set ( Rest vs Fist )
- No cross-subject validation performed
- No live hardware-in-the-loop validation completed
- Fixed hyperparameters - no grid search applied
