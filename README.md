# Pneumonia Detection from Chest X-rays (CNN)

## 📌 Overview
This project applies **Convolutional Neural Networks (CNNs)** to detect pneumonia from chest X-ray images. The model classifies scans as **Normal** or **Pneumonia**, supporting early diagnosis and AI-assisted screening.  
It demonstrates how deep learning can be applied to medical imaging and highlights the potential of AI in healthcare.

---

## Repository Structure
```
CNN-X-Ray-Pneumonia-Detection/
│── README.md                  # Project description, dataset link, usage
│── requirements.txt           # Dependencies       
│── results/                   # Evaluation outputs
│   ├── Training_History.png
│   ├── Classification_Report.png
│   ├── Confusion_Matrix.png
│   ├── ROC_Curve.png
│   └── PR_Curve.png
│── notebooks/                 # Jupyter notebooks
   └── pneumonia_detection.ipynb
```

---
## 🔗 Model Download
Download the trained model here: [Trained model - pneumonia_cnn.h5 (Google Drive Link)](https://drive.google.com/file/d/1l2vsi5McGlmyQjoCNZR5LA2ZpQu0Sfsn/view?usp=drive_link)

---

## 📂 Dataset
- **Source**: [Chest X-ray Dataset (Google Drive)](https://drive.google.com/drive/folders/17DpoIRNuuqp4Y7IT1lhVGAcyUk5IkIch?usp=drive_link)
- Chest X-ray dataset
  - train
  - validation
  - test  
- Each dataset has 2 **Classes**: `NORMAL` and `PNEUMONIA`  
- **Preprocessing**:  
  - Images resized to 150×150 pixels  
  - Normalized to scale pixel values between 0–1  
  - Augmentation applied (zoom, vertical flip) to improve generalization  

---

## ⚙️ Approach
1. **Data Processing**
   - Image resizing, normalization, augmentation  
   - Train/validation/test generators
   - Manual test arrays prepared for evaluation  

2. **Model Architecture**
   - Convolutional layers with ReLU activation  
   - Batch Normalization for stable training  
   - MaxPooling and Dropout for regularization  
   - Dense layers for classification  
   - Sigmoid output for binary pneumonia detection  

3. **Training**
   - Optimizer: Adam  
   - Loss: Binary Crossentropy  
   - Callbacks:  
     - **EarlyStopping** to prevent overfitting  
     - **ModelCheckpoint** to save the best model (`pneumonia_cnn.h5`)  

4. **Evaluation**
   - Classification report (precision, recall, F1-score)  
   - Confusion matrix for diagnostic clarity  
   - ROC curve (sensitivity vs. specificity)  
   - Precision-Recall curve (performance on imbalanced data)  
   - Average Precision Score  

---

## 📦 Requirements

- numpy
- matplotlib
- opencv-python
- seaborn
- tensorflow
- scikit-learn
- jupyter

Install dependencies:
```bash
pip install -r requirements.txt
```

---

## 🚀 Installation & Usage
- Clone the repository :
```bash
git clone https://github.com/b-nikhileswar-reddy/CNN-X-Ray-Pneumonia-Detection.git
cd CNN-X-Ray-Pneumonia-Detection
```
- Run the Script
```
jupyter notebook notebooks/pneumonia_detection.ipynb
```
