# Automatic Modulation Classification under Blind Scenario

## 🌟 Unique Contribution
First work to classify CPFSK and GFSK alongside analog modulation in a blind scenario, achieving 99.6% accuracy using a novel feature fusion approach.

## 🔍 Problem Statement
Automatic modulation classification (AMC) is crucial for:
- Spectrum monitoring
- Cognitive radio applications
- Signal identification and demodulation
- Electronic warfare applications
- Aircraft signal detection and interception

The challenge lies in correctly classifying modulation schemes under complex channel conditions and noise.

## 📊 Dataset
**Self-Generated Dataset Specifications:**
- Total Samples: 4000 signals
  - BPSK: 1000 signals
  - CPFSK: 1000 signals
  - DSB-AM: 1000 signals
  - GFSK: 1000 signals
- Sampling Rate: 200 kHz
- SNR: 30dB
- Generation Time: 2405 seconds

**Channel Conditions:**
- White Gaussian noise
- Phase-frequency offset
- Rician multipath

## 🔬 Methodology

### 1. Feature Extraction
**Signal Features:**
- Statistical domain features
- Spectral domain features
- Magnitude and angle features
- Total signal features: 102

**Image Features (from spectrograms):**
- BRISK (Binary Robust Invariant Scalable Keypoints)
- FAST (Features from Accelerated Segment Test)
- Harris features
- Minimum eigenvalue
- MSER (Maximally Stable Extremal Regions)
- SURF (Speeded-Up Robust Features)
- KAZE features
- Total image features: 1344

### 2. Feature Fusion & Reduction
- Serial fusion of signal and image features (1446 features)
- ANOVA-based feature reduction
- Final optimized feature set: 50 features

### 3. Classification
- Classifier: Linear Support Vector Machine (L-SVM)
- Cross-validation: 5, 10, 15, and 20 folds
- Kernel: Linear

## 📈 Results

### Performance Metrics
- Overall Accuracy: 99.6%
- Classification Performance per Class:
  ```
  BPSK:    995/1000 (99.5%)
  CPFSK:   993/1000 (99.3%)
  DSB-AM: 1000/1000 (100%)
  GFSK:    996/1000 (99.6%)
  ```

### Cross-Validation Results
Consistent 99.6% accuracy across different fold configurations:
- 5-fold CV
- 10-fold CV
- 15-fold CV
- 20-fold CV

## 📚 Publication
```bibtex
@INPROCEEDINGS{9445234,
  author={Tariq, Zain and Rehman, Abdul and Aslam, Taimoor and Khan, Muhammad Umar and Aziz, Sumair and Naqvi, Syed Zohaib Hassan},
  booktitle={2021 International Conference on Artificial Intelligence (ICAI)}, 
  title={Automatic Classification of Modulation Schemes under Blind Scenario}, 
  year={2021},
  volume={},
  number={},
  pages={203-208},
  keywords={Support vector machines;Modulation;Receivers;Feature extraction;Acoustics;Real-time systems;Reliability;Modulation;Feature fusion;ANOVA;Feature Reduction;Linear SVM},
  doi={10.1109/ICAI52203.2021.9445234}}
```

## 💡 Key Innovations
1. First successful classification of CPFSK and GFSK with analog modulation
2. Novel feature fusion approach combining signal and spectrogram features
3. Efficient feature reduction using ANOVA
4. High accuracy under complex channel conditions

## 🚀 Future Work
1. Classification of additional modulation schemes
2. Validation with real-time dataset
3. Performance optimization under varying channel conditions

---
*This research presents a novel approach to modulation classification using feature fusion and machine learning, achieving state-of-the-art results in blind scenario classification.*
