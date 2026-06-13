# CIFAR-10-Image-Classification-Using-CNN.
# CIFAR-10 Image Classification (Simple CNN)

This project is about building a Deep Learning model to classify images into 10 different categories (like cars, planes, cats, and dogs) using the CIFAR-10 dataset.

## 📝 What I Did In This Project
I built **two different models** to see how updating the architecture can improve the final score:

1. **Model 1 (The Basic Model):** A simple network with a few layers. It got decent results but started to memorize the training data (Overfitting).
2. **Model 2 (The Improved Model):** I upgraded Model 1 by adding:
   * `padding='same'`: To keep the image size stable and not lose edge details.
   * `Dropout`: To randomly turn off some neurons during training, forcing the model to truly understand the images instead of just memorizing them.

---

## 📊 Final Results Comparison

* **Model 1 Accuracy:** 69.1%
* **Model 2 Accuracy:** **76.0% (A 7% improvement! 🚀)**

Model 2 is much more stable, stronger, and performs better on new images.

---

## 🔍 What the Model Learned (Key Insights)
By looking at the Confusion Matrix of Model 2, we can see exactly where it succeeds and where it struggles:
* **The Best:** The model is excellent at detecting **Automobiles** and **Airplanes**.
* **The Mistakes:** The model sometimes gets confused between **Cats and Dogs** (because they look similar), and between **Airplanes and Ships** (because both often have a blue sky or ocean background).

---
Technical Skills Demonstrated

In this project, I applied core Computer Vision and Deep Learning techniques:

* **CNN Architecture Design:** Built stacked Convolutional layers, Max-Pooling for downsampling, and Dense layers for final classification.
* **Feature Preservation:** Used `padding='same'` to handle boundary and edge information in images correctly.
* **Regularization & Anti-Overfitting:** Implemented `Dropout` strategies to enforce generalization and stabilize training curves.
* **Data Diagnostics & Evaluation:** Analyzed training vs. validation `Loss` and `Accuracy` histories to detect model behavior.
* **Advanced Error Analysis:** Generated and interpreted a **Confusion Matrix** to discover class-specific weaknesses (e.g., Cat vs. Dog confusion).
* **Data Pipelines:** Processed imagery data arrays using `NumPy` and prepared target labels using categorical encoding.


https://colab.research.google.com/drive/185mS2N3xvq4j-YCqQweYG1WyVwyzirSi?authuser=1#scrollTo=Vcmi9esD27FY


## 🛠️ Tools Used
* Python
* TensorFlow / Keras
* Google Colab
* Matplotlib & Seaborn (for drawing the result charts)
