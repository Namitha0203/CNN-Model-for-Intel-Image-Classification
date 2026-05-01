# CNN-Model-for-Intel-Image-Classification
CNN-based image classification using the Intel Scene Dataset. Implements preprocessing, augmentation, model training, evaluation metrics, confusion matrix, and sample predictions using TensorFlow/Keras in Google Colab.

## 📌 Project Overview
This project builds and evaluates a Convolutional Neural Network (CNN) to classify natural scene images into six categories:

Buildings

Forest

Glacier

Mountain

Sea

Street

The model is implemented in TensorFlow/Keras and trained in Google Colab.

## 📂 Dataset
Source: Intel Image Classification Dataset (Kaggle)

The dataset contains:

Split	Images	Classes
Train	14,034	6
Test	3,000	6
Prediction	7,301	Unlabeled


Folder structure:

Code
seg_train/
seg_test/
seg_pred/
Each class has its own subfolder.

## 🧠 Model Architecture
The CNN includes:

Multiple Conv2D + MaxPooling2D layers

Flatten layer

Dense layer with 64 units

Output layer with softmax activation

Input size: 256 × 256 × 3

## 🔧 Features Implemented
Dataset loading using image_dataset_from_directory

Train/validation split (80/20)

Image resizing + rescaling

Data augmentation

Early stopping

Training curves visualization

Predictions on test images

Classification report

Confusion matrix

## 🚀 Training Details
The model was trained for up to 50 epochs with EarlyStopping enabled.

Final Test Accuracy: ~83%
Final Test Loss: ~0.48

## 📊 Evaluation Metrics
Classification Report
Includes:

Precision

Recall

F1-score

Support


Class	      Precision	  Recall	  F1-score
Buildings	  0.82	      0.80	    0.81
Forest	    0.91	      0.97	    0.93
Glacier	    0.85	      0.78	    0.81
Mountain	  0.73	      0.84	    0.78
Sea	        0.85	      0.79	    0.82
Street	    0.86	      0.82	    0.84

## 🧪 Confusion Matrix
A heatmap is generated using:

confusion_matrix

seaborn.heatmap

This helps visualize misclassifications across the six classes.

## 🖼️ Sample Predictions
The notebook includes:

Predictions for the first test batch

Prediction for a specific image

A 3×3 grid showing actual vs predicted labels with confidence scores

## 💾 Saving the Model
The trained model is saved as:

Code
model.h5
You can load it using:

python
model = tf.keras.models.load_model("model.h5")

## 🛠️ Technologies Used
Python

TensorFlow / Keras

NumPy

Matplotlib

Seaborn

Scikit‑learn

KaggleHub

Google Colab

## 📁 How to Run
1. Clone the repository
bash
git clone <your-repo-url>
cd <repo-folder>
2. Install dependencies
bash
pip install -r requirements.txt
3. Open the notebook
Upload the .ipynb file to Google Colab and run all cells.

4. Ensure Kaggle API or KaggleHub is configured
The dataset downloads automatically.

## Author
Namitha P Menon  
