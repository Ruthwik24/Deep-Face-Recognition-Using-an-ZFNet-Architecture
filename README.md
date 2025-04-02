# Deep Face Recognition using ZFNet Model  

<img src="https://img.shields.io/badge/Python-3.8%2B-blue" alt="Python"> <img src="https://img.shields.io/badge/TensorFlow-2.0%2B-orange" alt="TensorFlow"> <img src="https://img.shields.io/badge/Keras-API-red" alt="Keras">  

## Project Overview  
This project implements an efficient face recognition system using a **modified ZFNet architecture**, optimized for high accuracy while maintaining computational efficiency. The model achieves **96.67% validation accuracy** on the Yale Face Database with 15 distinct face classes.  

## Key Features  
✔ **Optimized ZFNet Architecture** – Modified for face recognition with efficient convolutional layers  
✔ **High Accuracy** – Achieves 96.67% validation accuracy  
✔ **Smart Training Pipeline** – Includes data augmentation and adaptive learning  
✔ **Callbacks for Efficiency** – Early stopping & dynamic learning rate adjustment  
✔ **Lightweight Model** – Balances performance and computational cost  

## Dataset  
🔹 **Yale Face Database** (165 GIF images)  
🔹 **15 subjects** with 11 facial expressions/configurations per subject:  
- Center-light, w/glasses, happy, left-light, w/no glasses  
- Normal, right-light, sad, sleepy, surprised, wink  

📥 **Dataset Source**: [Kaggle - Yale Face Database](https://www.kaggle.com/datasets/olgabelitskaya/yale-face-database/data)  

## Model Architecture  
### CNN Layers (Feature Extraction)  
- **Conv2D**: 7x7 → 5x5 → 3x3 kernels  
- **Activation**: ReLU  
- **Pooling**: MaxPooling2D  

### Classification Head  
- **Dense Layers** with Dropout regularization  
- **Output Layer**: Softmax (15 classes)  

## Training Configuration  
⚙ **Optimizer**: Adam (`lr=1e-4`)  
⚙ **Loss**: Categorical Cross-Entropy  
⚙ **Metrics**: Accuracy  
⚙ **Epochs**: 45  
⚙ **Batch Size**: 16  

## Performance  
✅ **Validation Accuracy**: 96.67%  
✅ **Classes Recognized**: 15  

## Usage  
1. Clone the repository:  
   ```bash
   git clone https://github.com/yourusername/deep-face-recognition-zfnet.git
   ```
2. Install dependencies:  
   ```bash
   pip install -r requirements.txt
   ```
3. Run training:  
   ```bash
   python train.py
   ```
4. Evaluate on test data:  
   ```bash
   python evaluate.py
   ```

## Visualization  
Sample face recognition results:  

![Prediction Examples](demo/prediction_examples.png)  

*Example outputs showing correct classifications*  

