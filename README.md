# Deep Learning Across Vision, Language, and Image Generation

This repository contains implementations and experiments covering three core deep learning domains:
1. Image classification using Convolutional Neural Networks (CNNs)
2. Text generation using Recurrent Neural Networks (LSTMs)
3. Autoregressive image modeling using PixelRNN architectures

The project emphasizes systematic experimentation, hyperparameter optimization, and interpretability.

---

## 1. CNN for CIFAR-10 Image Classification

- Dataset: CIFAR-10 (32×32 RGB images, 10 classes)
- Architecture: Deep CNN with configurable depth and filter sizes
- Techniques used:
  - Data augmentation
  - Batch normalization
  - Dropout regularization
  - Adam optimizer
- Best Test Accuracy: **89.20%**

### Analysis Performed
- Confusion matrix comparison (baseline vs optimized model)
- Training and validation loss/accuracy curves
- Feature map visualization showing hierarchical feature learning
- Hyperparameter ablation study:
  - Learning rate
  - Batch size
  - Number of filters
  - Network depth

---

## 2. RNN for Shakespeare Text Generation

- Dataset: Shakespeare corpus
- Model: Character-level LSTM with custom embeddings
- Task: Next-character prediction and text generation

### Key Insights
- Compared **random vs temporal data splits**
- Demonstrated how random splits lead to misleadingly high performance due to data leakage
- Temporal split achieved realistic generalization with **~54% validation accuracy**
- Generated coherent Shakespeare-style text samples

---

## 3. Autoregressive Image Modeling (PixelRNN)

Implemented and compared three models from the PixelRNN paper:
- **PixelCNN** (masked convolutions)
- **Row LSTM**
- **Diagonal BiLSTM**

### Evaluation
- Dataset: CIFAR-10
- Metric: Negative log-likelihood (bits per dimension)
- Results followed expected performance ranking:
  1. Diagonal BiLSTM (best)
  2. Row LSTM
  3. PixelCNN

---

## Technologies Used
- Python
- PyTorch
- NumPy
- Matplotlib
- Hugging Face Datasets
- Google Colab / Kaggle (training)

---

## Author
**Muhammad Umer Khan**  
FAST National University of Computer and Emerging Sciences  

This repository is intended for educational and research purposes.
