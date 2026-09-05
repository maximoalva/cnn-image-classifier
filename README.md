# Natural Scene Image Classification: Architecture Benchmark

> Aprendizaje Automático II  
> Tecnicatura Universitaria en Inteligencia Artificial (Universidad Nacional de Rosario)
> Máximo Alva, María Sol Aranda
> 2025

This repository contains a deep learning project designed to classify images of natural scenes from around the world. The objective is to build, evaluate, and compare different neural network architectures to accurately categorize images into one of six predefined classes: buildings, forest, glacier, mountain, sea, and street.

---

## Dataset
The project utilizes a dataset of natural scenes, which is automatically downloaded and extracted within the notebook.
*   **Training and Validation:** 14,034 images, split into 11,228 for training and 2,806 for validation.
*   **Testing:** 3,000 images used for final model evaluation.
*   **Image Dimensions:** All images are processed and resized to 150x150 pixels in RGB format.

---

## Architectures
To establish a performance baseline and analyze the evolution of computer vision models, four distinct architectures were developed and tested:

1.  **Dense Layers Model (MLP):** A baseline model relying purely on fully connected Dense layers to demonstrate the limitations of flattening spatial data without convolutional feature extraction.
2.  **Custom CNN (Convolutional + Dense Layers):** A standard Convolutional Neural Network built from scratch, utilizing `Conv2D`, `MaxPooling2D`, and `Dense` layers to capture local patterns and textures.
3.  **Residual Network:** An advanced architecture implementing residual layers and identity mappings (`Add` layers) to solve the vanishing gradient problem and train a deeper network.
4.  **Transfer Learning:** Implementation of a pre-trained backbone (`EfficientNetB0`) to leverage knowledge from massive external datasets, adapting its final layers for this specific 6-class problem.

---

## Evaluation
The project includes data augmentation techniques (`RandomFlip`, `RandomRotation`, `RandomTranslation`, `RandomContrast`) to improve model generalization. A custom plotting function is provided to visualize the loss and accuracy metrics for both the training and validation sets across epochs, allowing for a clear comparison of how each architecture performs.
