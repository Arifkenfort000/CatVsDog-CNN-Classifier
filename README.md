# 🐾 Cats vs Dogs Image Classification using CNN

A Deep Learning-based image classification project built from scratch using TensorFlow and Keras to accurately classify images of cats and dogs. This project follows a clean directory structure and utilizes a Convolutional Neural Network (CNN) trained on local image datasets.

---

## 📂 Project Structure

The project is organized in a clean and modular way:

```text
CatVsDog/
│
├── Data/
│   ├── train/          # Training images (Cat and Dog subfolders)
│   └── test/           # Testing images (Cat and Dog subfolders)
│
├── models/             # Directory to store trained model files
│   └── cat_dog_cnn_model.keras
│
├── .gitignore          # Files and folders to ignore in Git tracking
├── README.md           # Project documentation
├── requirements.txt    # Required Python libraries
└── Train.ipynb         # Jupyter Notebook containing the training code
```

---

## 🚀 Tech Stack & Libraries

* **Python** (Programming Language)
* **TensorFlow / Keras** (Deep Learning Framework)
* **Matplotlib** (Data Visualization)
* **Pathlib** (Path Management)
* **VS Code** (Development Environment)

---

## ⚙️ Model Architecture

The CNN model consists of the following layers:
1. **Rescaling Layer:** Normalizes pixel values from `[0, 255]` to `[0.0, 1.0]`.
2. **Convolutional Blocks:** Three blocks of `Conv2D` (with `ReLU` activation) followed by `MaxPooling2D` to extract features (edges, textures, shapes).
3. **Classification Head:** 
   * `Flatten` layer to convert 2D features to 1D vector.
   * `Dense` layer (64 neurons, `ReLU`) for deep feature interpretation.
   * `Dense` output layer (1 neuron, `Sigmoid`) for binary classification (Cat vs Dog).

---

## 📦 Installation & Setup

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/your-username/CatVsDog-CNN.git
   cd CatVsDog
   ```

2. **Install Dependencies:**
   Make sure you have Python installed, then install the required packages:
   ```bash
   pip install -r requirements.txt
   ```

3. **Run the Notebook:**
   Open VS Code, open `Train.ipynb`, and run the cells sequentially to train and evaluate the model.

---

## 📊 Results & Evaluation

After training the model for a few epochs, the model is evaluated on the test dataset, and the trained weights are automatically saved inside the `models/` folder as `cat_dog_cnn_model.keras`.