# Feedforward Neural Network

A minimal **feedforward neural network** for multiclass classification, implemented in **PyTorch** and demonstrated on the **Iris** dataset.

---

## Overview

This project implements a custom feedforward NN from scratch (using PyTorch tensors and autograd) to classify Iris flowers into three species: *setosa*, *versicolor*, and *virginica*. All details—architecture, data loading, training loop, and evaluation—are in the notebook.

---

## Features

- **Custom architecture**: Configurable layers and widths (no `nn.Linear` stack; uses `nn.Parameter` and manual forward pass).
- **Iris dataset**: Loaded via scikit-learn; 90% train / 10% test split.
- **Training**: SGD optimizer, cross-entropy loss, ReLU in hidden layers, softmax at output (via `CrossEntropyLoss`).
- **Metrics**: Training and test loss plus accuracy logged every 10 epochs.

---

## Requirements

- Python 3.x
- PyTorch
- scikit-learn
- NumPy
- Matplotlib

Install with:

```bash
pip install torch scikit-learn numpy matplotlib
```

---

## Quick Start

1. Clone the repository:
   ```bash
   git clone https://github.com/AugusGuarna/Feedforward_NN.git
   cd Feedforward_NN
   ```

2. Open and run the notebook:
   - **Locally**: Open `NN_multiclass_pred.ipynb` in Jupyter or VS Code.
   - **Online**: Use the “Open in Colab” badge at the top of the notebook.

No extra setup or data download is required; the notebook loads the Iris dataset automatically.

---

## Project Structure

```
Feedforward_NN/
├── README.md
└── NN_multiclass_pred.ipynb   # Full implementation and walkthrough
```

---

## Notebook Contents

| Section | Description |
|--------|-------------|
| **Architecture** | Input (4) → hidden (6, 8, 10) → output (3); ReLU and softmax. |
| **Data** | Iris loaded, encoded, split into train/test, wrapped in `DataLoader`s. |
| **Model** | `FeedForwardNeuralNetwork` class and parameter check. |
| **Training** | Loss, optimizer, 200-epoch loop with train/test loss and accuracy. |
| **Results** | Short discussion of performance and data size. |

---

## License

This project is open source. Use and adapt as needed.
