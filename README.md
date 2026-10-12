# StyleGAN-Inspired Image Generator using TensorFlow

A from-scratch implementation of a compact **StyleGAN-inspired Generative Adversarial Network (GAN)** trained on the CIFAR-10 dataset. The project explores style-based image synthesis, style mixing, and latent-space interpolation using TensorFlow and Keras.

## 📌 Project Overview

This project implements a simplified StyleGAN-style architecture to generate synthetic color images. It uses a mapping network to transform random latent vectors into a style space and a synthesis network to progressively generate images at a resolution of 32 × 32 pixels.

The model is trained on a subset of the CIFAR-10 training dataset and demonstrates fundamental concepts in generative deep learning.

## 🎯 Objectives

- Understand the architecture and working principles of StyleGAN.
- Implement mapping and synthesis networks using TensorFlow and Keras.
- Generate synthetic images from random latent vectors.
- Explore style mixing to combine features from different latent codes.
- Visualize latent-space interpolation between generated images.
- Monitor generator and discriminator losses during training.

## 🧠 Model Architecture

The project consists of the following components:

1. **Mapping Network:** Transforms a random latent vector \(z\) into an intermediate latent representation \(w\) through eight dense layers.
2. **Synthesis Network:** Generates images from a learned constant using styled convolutional layers at multiple resolutions.
3. **Adaptive Instance Normalization (AdaIN):** Applies style-dependent scaling and bias to feature maps.
4. **Noise Injection:** Adds stochastic variation to generated image features.
5. **Discriminator:** Distinguishes real CIFAR-10 images from generated images.
6. **GAN Training:** Trains the generator and discriminator using non-saturating logistic loss.

## 📊 Dataset

**CIFAR-10**

- Dataset: CIFAR-10
- Training subset: 20,000 images
- Original image dimensions: 32 × 32 pixels
- Image channels: 3 (RGB)
- Pixel normalization: [-1, 1]
- Dataset classes: Airplanes, automobiles, birds, cats, deer, dogs, frogs, horses, ships, and trucks

The notebook loads CIFAR-10 using the TensorFlow/Keras dataset API.

## 🛠️ Technologies Used

- Python
- TensorFlow
- Keras
- NumPy
- Matplotlib
- Jupyter Notebook

## ⚙️ Implementation Details

| Parameter | Value |
|---|---|
| Latent dimension | 128 |
| Intermediate style dimension | 128 |
| Mapping network depth | 8 dense layers |
| Image resolution | 32 × 32 |
| Batch size | 64 |
| Training epochs | 10 |
| Optimizer | Adam |
| Learning rate | 0.0002 |
| Random seed | 42 |

## ✨ Key Features

### 1. Synthetic Image Generation
Generates new RGB images from randomly sampled latent vectors.

### 2. Style Mixing
Combines style representations from two latent vectors at different synthesis stages to explore how styles influence generated images.

### 3. Latent-Space Interpolation
Interpolates between two latent vectors to visualize gradual changes in generated images.

### 4. Training Loss Visualization
Tracks generator and discriminator losses throughout training.

### 5. Generated Image Grid
Displays multiple generated samples in a grid for qualitative inspection.

## 🚀 Getting Started

### Prerequisites

Install Python and the required libraries:

```bash
pip install tensorflow numpy matplotlib jupyter
```

### Run the Project

**Step 1:** Clone the repository.

```bash
git clone https://github.com/YOUR-USERNAME/YOUR-REPOSITORY.git
```

**Step 2:** Navigate to the project directory.

```bash
cd YOUR-REPOSITORY
```

**Step 3:** Launch Jupyter Notebook.

```bash
jupyter notebook
```

**Step 4:** Open the `Style_GAN.ipynb` notebook.

**Step 5:** Run the notebook cells in order. The CIFAR-10 dataset will be downloaded automatically when required, and the model will train before running the generation and visualization experiments.

> Training time depends on the available hardware. The notebook's training configuration is intended as a manageable educational experiment, not a full-scale StyleGAN implementation.

## 📈 Results and Observations

The notebook demonstrates:

- Generated image samples after training.
- Style-mixing comparisons using different latent codes.
- Latent-space interpolation across generated images.
- Generator and discriminator loss histories.

The model produces learned color and texture patterns, although the generated images may remain blurry and may not consistently resemble recognizable objects. This is expected from a compact model trained for a limited number of epochs at low image resolution.

## 🔬 Future Improvements

- Train for more epochs and experiment with hyperparameters.
- Increase image resolution and model capacity.
- Implement techniques such as the style-based architecture's noise and style controls in greater detail.
- Evaluate generated-image quality using suitable quantitative metrics.
- Experiment with larger datasets and GPU acceleration.

## 📚 Learning Outcomes

This project provides practical experience with GAN training, neural network architecture design, latent representations, style-based synthesis, and visualization of generated images.

## 👤 Author

**Harish Srinivasan T**

B.Tech – Artificial Intelligence and Data Analytics

## 📄 License

This project is intended for educational and learning purposes. Add a license file if you plan to distribute or reuse the project publicly.
