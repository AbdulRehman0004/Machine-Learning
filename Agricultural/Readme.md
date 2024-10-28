# Cucumber Leaf Disease Classification using LTriDP and Haralick Features

## 📊 Research Impact
- **Citations**: 8
- **Unique Contribution**: First work to combine Local Tri-directional Patterns (LTriDP) and Haralick features for robust cucumber disease classification in real-world farming conditions
- **Achievement**: 96.80% accuracy in noisy, real-world conditions

## 🔍 Problem Statement
Plant diseases cause major economic and production losses in agriculture worldwide. In Pakistan:
- 3,426 hectares used for cucumber cultivation
- 52,766 tonnes total production
- 15.4 tonnes/hectare average yield
- Punjab contributes 82% of production

Early and accurate disease detection is crucial for:
- Preventing crop losses
- Optimizing treatment timing
- Improving farm productivity
- Maintaining food security

## 📸 Dataset
**Self-Collected Dataset:**
- Location: Cucumber farms in Taxila, Pakistan
- Equipment: CANON 70D DSLR camera
- Image Format: JPEG (5184px × 3456px)
- Total Samples: 907 images
  - Anthracnose: 383 samples
  - Aphids: 223 samples
  - CYSDV: 178 samples
  - Healthy: 123 samples
  - 
<img src="images/Raw Images.png" width="400">

## 🔬 Methodology

<img src="images/Block Diagram.png" width="400">

### 1. Preprocessing
- RGB to LAB color space conversion
- Enhanced information extraction per pixel
- Better handling of real-world lighting conditions

### 2. Segmentation
- K-means clustering (K=2)
- Region of Interest (ROI) extraction
- Noise reduction in real farming conditions

### 3. Feature Extraction
**Combined Features:**
1. Haralick Features (14 texture features):
   - Contrast
   - Cluster prominence
   - Energy
   - Cluster shade
   - Autocorrelation
   - Variances
   - Other statistical measures

2. Local Tri-directional Pattern (LTriDP):
   - Extended form of Local Binary Pattern
   - Eight-pixel neighborhood analysis
   - Enhanced texture pattern extraction

3. HOG Features:
   - Shape-based features
   - Histogram binning
   - Dimensional reduction from 3000 to 100

### 4. Classification
- Classifier: Quadratic Support Vector Machine (Q-SVM)
- Validation: 10-fold cross-validation
- System Requirements: Intel Core i7 @ 2.7 GHz CPU, 8GB RAM

<img src="images/Classifier Comparision.png" width="400">

## 📈 Results

### Performance Metrics
- Overall Accuracy: 96.80%
- Features Performance:
  - LTriDP + Haralick: 96.80%
  - HOG + Haralick: 91.39%
  - LTriDP + HOG: 92.72%
  - LTriDP + HOG + Haralick: 92.94%

<img src="images/Confusion Matrix.png" width="400">


### Class-wise Performance
- Healthy: 89% True Positive Rate
- Disease Classes: 98% True Positive Rate

## 📊 Comparative Analysis
Our method outperforms existing approaches:
- K-means + Sparse Representation: 85.7%
- Hyperspectral Imaging: 90%
- Fuzzy C-Means: 86.21%
- Neural Networks: 91%

## 🚀 Key Advantages
1. Real-world robustness
2. High accuracy in noisy conditions
3. Efficient processing pipeline
4. Practical farm implementation
5. No controlled environment required

## 💡 Future Work
1. Embedded system development
2. Real-time implementation
3. Mobile application development
4. Extension to other crop diseases
5. Integration with farm management systems

## 📚 Publication
```bibtex
A. Rehman, Z. Tariq, S. u. din Memon, A. Zaib, M. U. Khan and S. Aziz, "Cucumber Leaf Disease Classification using Local Tri-directional Patterns and Haralick Features," 2021 International Conference on Artificial Intelligence (ICAI), Islamabad, Pakistan, 2021, pp. 258-263, doi: 10.1109/ICAI52203.2021.9445237. keywords: {Support vector machines;Industries;Image color analysis;Production;Feature extraction;Cameras;Real-time systems;Local tri-directional patterns;Cucumber Disease identification;Anthracnose;Aphids;CYSDV;Haralick Features;Quadratic SVM},
```

---
*This research provides a robust solution for cucumber disease classification in real farming conditions, addressing the practical challenges of agricultural disease detection.*
