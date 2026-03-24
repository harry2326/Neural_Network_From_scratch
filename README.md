
#  MNIST Digit Classification from Scratch (TensorFlow)

##  Explanation Video

 [Watch Full Explanation](https://your-video-link-here)

---

##  Overview

This project implements a **digit classification model on the MNIST dataset** using **TensorFlow (low-level APIs)**.

Unlike high-level frameworks, this implementation:

* Manually defines **weights and biases**
* Uses **GradientTape for backpropagation**
* Implements **training loop from scratch**

The model classifies handwritten digits (0–9) with a simple **linear neural network (logistic regression)**.

---

##  Key Concepts Covered

* Data preprocessing & normalization
* Train / Validation split
* Batch processing
* Forward propagation
* Loss computation
* Backpropagation using GradientTape
* Stochastic Gradient Descent (SGD)
* Model evaluation

---

##  Dataset

Uses the built-in **MNIST dataset**:

* 60,000 training images
* 10,000 test images
* Image size: **28 × 28 pixels**
* Classes: **10 (digits 0–9)**

---

##  Pipeline Breakdown

### 1. Data Loading & Shuffling

* Loads dataset using TensorFlow
* Randomly shuffles training data to avoid bias

---

### 2. Train–Validation Split

* 80% → Training
* 20% → Validation

Prevents overfitting and improves generalization.

---

### 3. Preprocessing

####  Flattening

[
28 x 28 --> 784
]

####  Normalization

Pixel values scaled to range:

[
[-1, 1]
]

---

### 4. Model Architecture

A simple **linear classifier**:

[
y = Wx + b
]

* Input size: **784**
* Output size: **10 (classes)**

---

### 5. Loss Function

Uses:

[
Sparse Categorical Crossentropy}
]

* Works directly with integer labels
* `from_logits=True` (no softmax applied manually)

---

### 6. Optimization

* Optimizer: **Stochastic Gradient Descent (SGD)**
* Learning rate: **0.1**

---

### 7. Training Loop

* Batch size: **48**
* Epochs: **55**
* Uses `tf.GradientTape()` for automatic differentiation

---

### 8. Prediction

* Selects a random test image
* Displays:

  * Ground truth label
  * Model prediction

---

##  Requirements

Install dependencies:
pip install tensorflow numpy matplotlib

---

##  Usage

1. Run the script:

python mnist_classifier.py

2. Output:

* Training loss per epoch
* Random test image visualization
* Predicted digit

---

##  Project Structure
.
├── mnist_classifier.py
└── README.md


---

##  Key Parameters

* `batch_size = 48`
* `num_epochs = 55`
* `learning_rate = 0.1`

---

##  Example Output

* Loss decreasing over epochs
* Visualization of a handwritten digit
* Printed prediction vs actual label

---

##  Features

✔ From-scratch implementation (no Keras model API)
✔ Full control over training loop
✔ Educational focus on core deep learning concepts
✔ Lightweight and easy to understand

---

##  Limitations

* No hidden layers (linear model only)
* Lower accuracy compared to deep networks
* No validation metrics tracking
* No GPU optimization

---

##  Future Improvements

* Add hidden layers (Deep Neural Network)
* Use ReLU / Softmax explicitly
* Track accuracy along with loss
* Add validation evaluation per epoch
* Implement CNN for higher accuracy

---

##  Contributing

Feel free to fork and improve the project!

---

##  License

You can add an MIT License to make this project open-source.

