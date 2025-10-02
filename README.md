# 🐶🐱 Cats vs Dogs Image Classification

## 📌 Project Overview
This project builds a **Convolutional Neural Network (CNN)** to classify images of cats and dogs.  
Using the popular **PetImages** dataset, the model is trained to distinguish between the two classes with the help of **TensorFlow/Keras** and **data augmentation** techniques.  

---

## 📂 Dataset
- Source: [Microsoft Cats vs Dogs Dataset](https://www.microsoft.com/en-us/download/details.aspx?id=54765)  
- Folder Structure:
PetImages/
Cat/
Dog/

- Preprocessing steps:
- Removed corrupted files (`Thumbs.db`, `11702.jpg`, `666.jpg`).
- Validated image integrity with **PIL**.
- Balanced dataset into a Pandas DataFrame with image paths and labels.

---

## 🔍 Exploratory Data Analysis (EDA)
- Random grid plots of cat and dog images.
- Class distribution checked using **Seaborn**.
- Labels converted into categorical format.

---

## ⚙️ Data Preprocessing
- Used **Keras ImageDataGenerator** for:
- **Rescaling** pixel values  
- **Augmentation**: rotation, zoom, shift, flip  
- Split into:
- **80% Training set**
- **20% Testing set**

---

## 🧠 Model Architecture
Built using `tensorflow.keras`:
- **Convolutional Layers (Conv2D + MaxPooling2D)**
- **Flatten Layer**
- **Dense Layers**
- **Output Layer** with **sigmoid activation** (binary classification)

**Loss & Optimizer**:
- Loss: `binary_crossentropy`
- Optimizer: `Adam`
- Metric: `accuracy`

---

## 📊 Training & Evaluation
- Trained CNN with augmented training data.
- Plotted training vs validation **accuracy** and **loss**.
- Evaluated on test set for final accuracy.

---

## 🖼️ Results
- Model achieves **high accuracy** on test data (exact % depends on training run).
- Predictions visualized with sample images:
- ✅ Correct predictions highlighted
- ❌ Misclassifications analyzed

<img width="511" height="782" alt="image" src="https://github.com/user-attachments/assets/4086979c-8a8a-41e1-a372-663cb9cce89f" />

---

## 🚀 How to Run
1. Clone the repository:
 ```bash
 git clone https://github.com/MaqdadShow/Image-Classification.git
 cd cats-vs-dogs-classification
```
```bash
pip install -r requirements.txt
```
```bash
jupyter notebook Image_Classification.ipynb
```
