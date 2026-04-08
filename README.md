## CNN Image Classification – Animals-10 Dataset

This project implements and optimizes a Deep Convolutional Neural Network (CNN) for multi-class image classification using the Animals-10 dataset.


---

## Dataset

The model was trained on the Animals-10 dataset, which contains natural RGB images across 10 different animal categories.

Characteristics:
- 10 classes
- Real-world images
- Variations in lighting, pose, background, and scale
- Multi-class classification problem

The variability in image conditions makes generalization an important challenge.

---

## Model Development Strategy

### 1️⃣ Baseline Model
Started with a standard CNN architecture:

- 3 Convolutional layers (ReLU)
- MaxPooling after each convolution block
- Fully connected Dense layer
- Softmax output layer

This served as the reference model for comparison.

---

### 2️⃣ Architectural Improvements

To improve performance and reduce overfitting, the following enhancements were introduced:

- Increased network depth (additional convolutional layers)
- Batch Normalization for training stability
- Dropout (0.25–0.5) for regularization
- Data augmentation to improve robustness
- Early stopping to prevent overfitting
- Learning rate reduction on plateau

---

## Training Configuration

- Loss Function: Sparse Categorical Crossentropy
- Optimizers tested:
  - Adam
  - SGD (with momentum)
- Regularization:
  - Dropout in convolution and dense layers
- Callbacks:
  - EarlyStopping
  - ReduceLROnPlateau

---

## Results

Key observations:

- Deeper CNN improved validation accuracy over the baseline model
- Batch Normalization stabilized training and accelerated convergence
- Dropout reduced overfitting gap between training and validation accuracy
- Data augmentation improved generalization performance
- SGD with momentum provided competitive and stable results

Final model achieved strong validation performance with stable learning curves.

---

## 🛠 Technologies Used

- Python
- TensorFlow / Keras
- NumPy
- Matplotlib
---

