# Deep Learning Image Classification and Segmentation

This repository contains a deep learning project developed as part of coursework at Trinity College Dublin. The objective was to design and train high-performance models for **image classification** and **semantic segmentation** under strict parameter constraints, optimising performance and computational efficiency.

## 🧠 Project Highlights

- 🔹 **Classification Accuracy:** 90.33%
- 🔹 **Segmentation Accuracy:** 87.1%
- 🔹 **Epochs Trained:** 50 (both tasks)
- 🔹 **Framework:** TensorFlow / Keras
- 🔹 **Model Constraints:** ≤ 5M parameters (classification), ≤ 3M (segmentation)


---

## 🧪 Classification Model

- ✅ Custom-designed CNN using:
  - 6 convolutional blocks
  - Batch Normalisation, MaxPooling
  - Global Average Pooling
  - Dropout layers & L2 Regularisation
- ✅ Adaptive learning rate scheduling (ReduceLROnPlateau)
- ✅ Custom data augmentation (see below)
- ⚠️ Strict check to ensure model parameters ≤ 5 million

📊 **Result:** Achieved **90.33% accuracy** on validation data over 50 epochs.

---

## 🎯 Segmentation Model

- Built two segmentation pipelines:
  1. **Basic Encoder-Decoder** with upsampling and convolution
  2. **Residual U-Net** using skip connections via `add()` layers
- Used `sigmoid` activation for binary segmentation
- Dropout added in bottleneck for regularisation
- Validation parameter cap enforced: ≤ 3 million

📊 **Result:** Achieved **87.1% accuracy** on segmentation task.

---

## 🔁 Data Augmentation Strategy

To improve generalisation, the following augmentations were applied:

- `RandomFlip` – horizontal & vertical
- `RandomZoom` – zoom range of 0.1
- `RandomContrast` – contrast shift of 0.1
- `GaussianNoise` – added input-level noise

Augmented images were appended to the original training set, increasing diversity for both classification and segmentation.

---

## 🛠️ Technologies Used

- Python 3.x
- TensorFlow / Keras
- NumPy, Pandas, Matplotlib
- Jupyter Notebooks
- Google Colab (optional runtime)

---

## 📜 License

This project was completed as part of academic coursework and is shared for educational purposes only. For reuse or citation, please credit the author.

---

**Author**: Dhawal Patodi  
**Institution**: Trinity College Dublin  
**Student Number**: 23364336  
**Contact**: [patodid@tcd.ie](mailto:patodid@tcd.ie)
