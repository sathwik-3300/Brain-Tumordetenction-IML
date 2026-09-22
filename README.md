# 🧠 Brain Tumor Detection Using Convolutional Neural Networks (CNN)

This project aims to develop an automated deep learning system using CNNs to detect brain tumors from MRI images. Our model achieves a **94.7% accuracy** on the test set, demonstrating strong potential for aiding medical diagnosis.

## 📁 Dataset & Preprocessing

- MRI images are divided into two classes: `Tumor` and `No Tumor`.
- Images resized to **128×128** pixels.
- Normalized pixel values to range [0, 1].
- Data Augmentation applied using Keras `ImageDataGenerator`.

## 🧠 Model Architecture

The CNN model was built using **TensorFlow** and **Keras**, consisting of:

- **3 Convolutional Layers** with ReLU + MaxPooling  
- **Dropout Layers** (0.25 and 0.5)  
- **2 Dense Layers** (128 and 64 units)  
- **Output Layer:** Sigmoid activation for binary classification

## ⚙️ Compilation & Training

- **Loss Function:** Binary Cross-Entropy  
- **Optimizer:** Adam  
- **Epochs:** 50  
- **Batch Size:** 32

The model was trained on an 80/20 train-validation split and evaluated on a separate test set.

## 📊 Evaluation Metrics

- **Test Accuracy:** 94.7%  
- **Precision:** 93%  
- **Recall:** 96%  
- **F1-Score:** 94.5%

A confusion matrix showed low false negatives, which is crucial in medical diagnosis scenarios.

## 📈 Training Curves

- Accuracy and loss graphs plateaued around **epoch 30**, indicating good convergence and minimal overfitting.

## 📎 Project Structure

```bash
brainTumorDetection/
│
├── brainTumorDetection.ipynb   # Jupyter Notebook with full code
├── projectReport.pdf           # Detailed report of the project
├── README.md                   # This file
└── /dataset/                   # Folder containing MRI images (not uploaded here)

# ▶️ To Run

#Clone the repository
git clone https://github.com/<your-username>/brainTumorDetection.git
cd brainTumorDetection

# Run the notebook
jupyter notebook brainTumorDetection.ipynb

# 📌 Future Work

- Hyperparameter tuning using Keras Tuner or GridSearch.
- Multi-class tumor classification (e.g., glioma, meningioma).
- Deploying the model as a web app or mobile diagnostic tool.
