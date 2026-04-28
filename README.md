# 🍇 Raisin Classification with PyTorch

This project builds a Machine Learning model using **PyTorch** to classify raisins into two categories based on numerical features such as size and shape.

## 📌 Project Overview

- Model: Fully Connected Neural Network
- Task: Binary Classification
- Classes:
  - Kecimen
  - Besni
- Dataset: `Raisin_Dataset.csv`

---

## 📂 Project Structure

```
.
├── seperaterasin.ipynb   # Main notebook for training and evaluation
├── Raisin_Dataset.csv    # Dataset file
└── README.md             # Project documentation
```

---

## 📊 Dataset

The dataset contains 7 numerical features:

- Area  
- MajorAxisLength  
- MinorAxisLength  
- Eccentricity  
- ConvexArea  
- Extent  
- Perimeter  

Label:
- Class (Kecimen / Besni)

---

## ⚙️ Workflow

### 1. Data Preparation
- Load dataset using pandas
- Check for missing values
- Split features (X) and labels (y)

### 2. Preprocessing
- Encode labels using `LabelEncoder`
- Convert data into PyTorch tensors

### 3. Train-Test Split
- Using `train_test_split`
- Train: 20%
- Test: 80%

---

## 🧠 Model Architecture

A Fully Connected Neural Network:

- Input layer: 7 features  
- Hidden layers: 3 layers (8 neurons each)  
- Output layer: 2 classes  

Example structure:

```
Model(
  (fc1): Linear(7 → 8)
  (fc2): Linear(8 → 8)
  (fc3): Linear(8 → 8)
  (out): Linear(8 → 2)
)
```

---

## 🏋️ Training

- Loss Function: CrossEntropyLoss  
- Optimizer: Adam  
- Learning Rate: 0.001  
- Epochs: 100  
- Batch Size: 32  

---

## 📈 Evaluation

The model is evaluated on the test set using accuracy.

> Note: Accuracy may vary depending on training results.

---

## 🚀 How to Run

### 1. Install dependencies

```bash
pip install numpy pandas torch scikit-learn
```

### 2. Open the notebook

```bash
jupyter notebook seperaterasin.ipynb
```

### 3. Run all cells

---

## 📝 Notes

- Make sure to update dataset paths if necessary
- Data normalization is recommended for better performance (not included in this version)

---

## 💡 Future Improvements

- Add normalization / standardization
- Improve model architecture
- Add validation set
- Include evaluation metrics (confusion matrix, precision, recall)

---
