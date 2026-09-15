# 🧠 Handwritten Digit Recognizer using CNN

A deep learning project that recognizes handwritten digits **(0–9)** using a **Convolutional Neural Network (CNN)** built with **PyTorch**.

The project covers the complete machine learning workflow — from image preprocessing and CNN model development to training, validation, performance evaluation, visualization, and prediction on unseen handwritten digit images.

---

## 📌 Project Overview

Handwritten digit recognition is a fundamental computer vision problem and a common application of deep learning.

In this project, a CNN is trained on **3,000 labeled handwritten digit images** and evaluated using a separate **10,000-image labeled validation dataset**.

The trained model is also used to generate predictions for **10,000 unlabeled test images**.

---

## 🎯 Objectives

* Preprocess handwritten digit images for CNN training
* Build a CNN architecture using PyTorch
* Train the model for 10 epochs
* Evaluate model performance on validation data
* Analyze predictions using classification metrics
* Visualize the confusion matrix
* Identify misclassified images
* Predict digits from new uploaded images
* Save the trained model for future inference

---

## 📊 Dataset

| Dataset    | Images | Labels      |
| ---------- | -----: | ----------- |
| Training   |  3,000 | ✅ Available |
| Validation | 10,000 | ✅ Available |
| Test       | 10,000 | ❌ Unlabeled |

### Image Properties

* Image size: **28 × 28 pixels**
* Number of classes: **10**
* Classes: **0–9**
* Image type: Grayscale
* Training images: **3,000**
* Training distribution: **300 images per digit**

The test dataset contains labels with value `-1`, indicating that it is intended for prediction rather than accuracy evaluation.

---

## 🏗️ CNN Architecture

The model consists of two convolutional blocks followed by fully connected layers.

```text
Input Image
   │
   ▼
28 × 28 × 1
   │
   ▼
Conv2D (32 filters, 3×3)
   │
   ▼
ReLU
   │
   ▼
MaxPooling
   │
   ▼
Conv2D (64 filters, 3×3)
   │
   ▼
ReLU
   │
   ▼
MaxPooling
   │
   ▼
Flatten
   │
   ▼
Fully Connected (128)
   │
   ▼
ReLU
   │
   ▼
Dropout (0.5)
   │
   ▼
Output Layer (10 classes)
```

---

## ⚙️ Technologies Used

* **Python**
* **PyTorch**
* **NumPy**
* **Matplotlib**
* **Scikit-learn**
* **Seaborn**
* **Google Colab**
* **Jupyter Notebook**

---

## 🔄 Project Workflow

```text
Dataset Loading
      ↓
Data Exploration
      ↓
Image Preprocessing
      ↓
Train / Validation Preparation
      ↓
CNN Model Development
      ↓
Loss & Optimizer Setup
      ↓
Model Training
      ↓
Validation
      ↓
Classification Report
      ↓
Confusion Matrix
      ↓
Misclassification Analysis
      ↓
Test Prediction
      ↓
Save Trained Model
      ↓
New Image Prediction
```

---

## 📈 Model Evaluation

The model was evaluated using:

* Accuracy
* Precision
* Recall
* F1-score
* Confusion Matrix
* Misclassified image analysis

The project also includes visualizations for:

* Training loss
* Training accuracy
* Validation performance
* CNN predictions
* Misclassified handwritten digits

---

## 🔍 Prediction on New Images

After training, the saved CNN can be used to recognize a new handwritten digit.

For example:

```text
Input:
digit_5.jpg

        ↓

CNN Model

        ↓

Predicted Digit: 5
```

The model also provides a confidence score for the prediction.

---

## 💾 Saved Model

The trained model is saved as:

```text
handwritten_digit_cnn.pth
```

The model can be loaded later without retraining:

```python
model = DigitCNN().to(device)

model.load_state_dict(
    torch.load(
        "handwritten_digit_cnn.pth",
        map_location=device
    )
)

model.eval()
```

---

## 📁 Repository Structure

```text
HANDWRITTEN_DIGIT_RECOGNIZER_CNN/
│
├── Handwritten_Digit_Recognizer_CNN.ipynb
├── handwritten_digit_cnn.pth
├── README.md
├── requirements.txt
│
└── results/
    ├── confusion_matrix.png
    ├── training_loss.png
    ├── accuracy_plot.png
    └── predictions.png
```

---

## 🚀 How to Run

### 1. Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/HANDWRITTEN_DIGIT_RECOGNIZER_CNN.git
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Open the notebook

Open:

```text
Handwritten_Digit_Recognizer_CNN.ipynb
```

### 4. Run the notebook

Execute the cells sequentially to:

* Load the dataset
* Preprocess images
* Train the CNN
* Evaluate the model
* Generate predictions

---

## 📦 Requirements

Create a `requirements.txt` file containing:

```text
torch
torchvision
numpy
matplotlib
scikit-learn
seaborn
Pillow
```

---

## 💡 Key Learning Outcomes

Through this project, I worked with:

* Convolutional Neural Networks
* Image preprocessing
* PyTorch model development
* Model training and optimization
* Classification metrics
* Confusion matrix analysis
* Computer vision
* Model inference
* Model serialization using `.pth`
* Prediction on unseen images

---

## 🔮 Future Improvements

Possible improvements include:

* Data augmentation
* Batch normalization
* Learning-rate scheduling
* Hyperparameter tuning
* Early stopping
* Transfer learning experiments
* Semi-supervised learning using the unlabeled training data
* Building a Streamlit web application
* Deploying the digit recognizer as an interactive application


## ⭐ Project Summary

This project demonstrates an end-to-end **computer vision and deep learning workflow** using PyTorch to recognize handwritten digits. It combines CNN-based feature extraction, model evaluation, visualization, and real-world inference on new handwritten images.
