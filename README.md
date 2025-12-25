# Multi-layer ANN from Scratch - MNIST Classification

This repository contains the implementation of a Deep Neural Network (DNN) built from scratch using NumPy, as part of **Assignment No. 3** in the Neural Networks course.

## Project Overview
[cite_start]The project extends the single-hidden-layer Artificial Neural Network (ANN) provided in Chapter 11 of *"Machine Learning with PyTorch and Scikit-Learn"*[cite: 2, 8]. [cite_start]The main goal was to transform the original architecture into a **Deep Neural Network** by adding a second hidden layer and evaluating its performance using advanced metrics[cite: 110, 112].

### Key Features:
* [cite_start]**Manual Implementation:** Developed the Forward and Backward propagation (Backpropagation) algorithms from scratch using NumPy to handle two hidden layers[cite: 145, 814].
* [cite_start]**Architecture:** A "Plain Deep NN" consisting of an input layer (784 nodes), two hidden layers (50 nodes each), and an output layer (10 nodes)[cite: 122, 137].
* [cite_start]**Dataset:** Utilized the MNIST dataset of handwritten digits, normalized to the range [-1, 1][cite: 203, 231].
* **Validation:** Applied a strict **70% Train / 30% Test** split procedure as required by the assignment.
* **Performance Metric:** Evaluation based on **Macro AUC** to measure the model's classification power across all 10 digits.

---

## 🔗 Links to Source Code

* **Main Assignment Notebook (Extended 2-HL Code):**
  [Deep_NN_MNIST_Assignment3.ipynb](https://github.com/shirabo/Neural-Networks-Assignment-3/blob/main/Deep_NN_MNIST_Assignment3%20(1).ipynb)

* **Original Reference Code (Chapter 11):**
  [Raschka et al. Ch11 Original Notebook](https://github.com/rasbt/machine-learning-book/blob/main/ch11/ch11.ipynb)

---

## Performance Comparison
The extended model was compared against the original single-layer implementation and a modern framework-based model (PyTorch).

| Implementation | Hidden Layers | Framework | Test Macro AUC |
| :--- | :---: | :---: | :--- |
| **Original Code (Section 3)** | 1 | NumPy | **0.9893** |
| **Revised Code (Assignment)** | 2 | NumPy | **0.9871** |
| **Framework Model** | 2 | PyTorch | **0.9036** |

---

## Insights
1. [cite_start]**Mathematical Validation:** The successful training of the 2nd hidden layer confirms the correct manual derivation of the multi-layer chain rule for backpropagation[cite: 785, 927].
2. [cite_start]**Framework vs. Scratch:** Our NumPy-based Mini-batch SGD implementation outperformed the basic PyTorch setup in the given 20-epoch training window[cite: 943, 944].
3. [cite_start]**Model Convergence:** Both NumPy implementations showed rapid convergence within the first 10-20 epochs[cite: 595, 627].

## How to Run
1. Clone this repository.
2. Ensure you have `numpy`, `torch`, `scikit-learn`, and `matplotlib` installed.
3. Open the `.ipynb` file in Jupyter Notebook or Google Colab and run all cells.
