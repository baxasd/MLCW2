## **Project Overview**

This project implements a supervised image-classification system using the **Intel Image Classification Dataset**. The goal is to design, train, and evaluate a neural network capable of recognising six outdoor scene categories. The work aligns with the assessment requirements for Machine Learning Coursework 2, focusing on data preparation, CNN architecture design, training, and evaluation.

The full implementation is provided in the notebook `Z22590018_MLCW2.ipynb`.

---

## **Dataset**

The project uses the public dataset:

**Intel Image Classification Dataset**
Source: *Puneet6060 on Kaggle*

The dataset contains six labelled classes:

* Buildings
* Forest
* Glacier
* Mountain
* Sea
* Street

Images are loaded using `image_dataset_from_directory`.
Training data is drawn from *seg_train*, and evaluation uses *seg_test*.
Images are downscaled to **128×128** to reduce computational load.

---

## **Project Structure**

The notebook is organised into the following stages:

### **1. Importing Libraries**

TensorFlow/Keras, NumPy, Matplotlib, and scikit-learn are used for model construction, training, and evaluation.

### **2. Data Loading & Preprocessing**

* Automatic directory-based class labelling.
* Downscaling to 128×128 RGB.
* Batching and caching for faster I/O.
* Train/test split follows dataset structure.
* Optional data augmentation pipeline included but disabled for short training runs.

### **3. CNN Model Architecture**

A custom Convolutional Neural Network is implemented using Keras Sequential API:

* Input layer: `(128,128,3)`
* Conv + MaxPooling blocks
* GlobalAveragePooling layer for dimensionality reduction
* Dense (fully connected) layer for decision making
* Dropout for regularisation
* Final softmax output layer with 6 units (one per class)

This structure focuses on simplicity and training efficiency while retaining meaningful feature extraction.

### **4. Model Training**

* Optimiser: **Adam**
* Loss: **Categorical Crossentropy**
* Epochs: 5 (for demonstration; can be increased for full training)
* Metrics: Accuracy

Training and validation accuracy/loss metrics are recorded through `model.fit`.

### **5. Evaluation**

Model performance is assessed using:

* Accuracy & loss plots across epochs.
* Confusion matrix for per-class behaviour.
* Final evaluation on the separate **seg_test** dataset.

---

## **Results Overview**

The notebook includes plots that show learning progression and performance analysis.
The confusion matrix highlights class-wise strengths and weaknesses, allowing qualitative inspection of misclassifications.

---

## **How to Run**

1. Install Jupyter notebook and ready to run. No further setup required

---

## **Files Included**

* `Z22590018_MLCW2.ipynb` – Full implementation
* `README.md` – This file