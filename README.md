# cat-vs-dog-classifier
CNN model which identifies and differentiates between a cat and a dog
# 🐱🐶 Cat vs Dog Image Classifier using CNN

This project implements a **Convolutional Neural Network (CNN)** to classify images as either **cats** or **dogs**. It’s built using **Python** and **TensorFlow/Keras**, trained on the popular Kaggle Cats vs Dogs dataset.

---

## 📂 Dataset

- **Source:** [Kaggle Dogs vs Cats Dataset](https://www.kaggle.com/c/dogs-vs-cats/data)
- Contains ~25,000 labeled images of cats and dogs.
- Images vary in:
  - size
  - background
  - posture

---

## 🧠 Model Architecture

- **Input:** Images resized to 150x150 pixels
- **Layers:**
  - Convolutional layers
  - Max pooling
  - Flatten
  - Dense layers
  - Dropout layers to reduce overfitting
- **Output:** Binary classification (cat = 0, dog = 1)
- **Loss Function:** Binary Crossentropy
- **Optimizer:** Adam

---

## 🔄 Data Preprocessing

- Loaded images using Keras `ImageDataGenerator`
- Applied data augmentation:
  - rotation
  - horizontal flip
  - zoom
- Rescaled pixel values to [0,1]

---

## 📊 Training

```python
model.fit(
    train_generator,
    steps_per_epoch=100,
    epochs=20,
    validation_data=validation_generator,
    validation_steps=50
)
```
The model has the accuracy of *90%*.
