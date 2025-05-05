# 🧠 Cat vs Dog Image Classification

This project tackles the binary classification task of distinguishing between cats and dogs using deep learning. Throughout the process, multiple modeling strategies were explored, starting with custom CNNs and progressing to transfer learning and K-Fold evaluation.

---

## 📌 Project Summary

### ✅ 1. Custom CNN Models
- Built a basic convolutional neural network from scratch.
- Then modified preprocessing techniques (rescaling, augmentation).
- Observed reduced accuracy with aggressive preprocessing.

### ✅ 2. Transfer Learning
- Evaluated three pre-trained models:
  - **MobileNetV2**
  - **ResNet50**
  - **VGG16**
- Used frozen base layers with custom top layers.
- Compared training/validation accuracy across models.

### ✅ 3. K-Fold Cross Validation
- Applied **5-Fold Cross Validation** using **MobileNetV2**.
- Trained a separate model for each fold.
- Saved the best performing model using early stopping and model checkpointing.
- Final model used for evaluation and prediction on the test set.

---

## 🗂️ Dataset Structure
dataset/
├── train/
│ ├── cats/
│ └── dogs/
└── test/
├── cats/
└── dogs/

yaml
Copy
Edit

---

## 🧪 Technologies Used

- Python 3
- TensorFlow / Keras
- Matplotlib
- Transfer Learning (TL)
- K-Fold Cross Validation

---

## 🚀 How to Run

1. Unzip the dataset into a `dataset/` directory.
2. Run the notebook or script step-by-step:
   - Custom CNN training
   - Preprocessing experiments
   - Transfer Learning comparison
   - K-Fold evaluation
3. The final model will be saved and evaluated on the test set.

---

## 📊 Results

- **Best accuracy** achieved with **MobileNetV2 + K-Fold** strategy.
- Final model outperformed others in both training stability and generalization.

---

## 📈 Example Plot

Validation accuracy comparison of 3 pre-trained models:

```python
MobileNetV2 - Val Acc: 0.9763
ResNet50    - Val Acc: 0.5995
VGG16       - Val Acc: 0.85


📌 Future Work
Use full fine-tuning (unfreeze some base layers).

Experiment with EfficientNet or DenseNet.

Build an interface (e.g., Streamlit) for real-time prediction.








