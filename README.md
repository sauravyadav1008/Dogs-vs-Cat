# 🐶🐱 Dogs vs Cats Image Classifier

A deep learning project that classifies images of **dogs** and **cats** using a **Convolutional Neural Network (CNN)** built with **TensorFlow & Keras**.  

---

## ✨ Features
- 📂 Uses image datasets from directories (`train/` and `test/`)  
- 🖼️ Preprocessing with normalization for stable training  
- 🧠 CNN architecture with Conv2D, MaxPooling, and Dense layers  
- 📊 Trains and validates the model with accuracy tracking  
- ⚡ Output: Predicts whether an image is of a **Dog 🐶** or a **Cat 🐱**

---

## 🛠️ Tech Stack
- [TensorFlow](https://www.tensorflow.org/) 🟧  
- [Keras](https://keras.io/) 🔵  
- Python 🐍  

---

## 📁 Dataset Structure
Your dataset should be arranged like this:

📂 dataset
┣ 📂 train
┃ ┣ 📂 cats
┃ ┗ 📂 dogs
┣ 📂 test
┃ ┣ 📂 cats
┃ ┗ 📂 dogs

## 🚀 Model Architecture
```plaintext
Conv2D (32 filters) → MaxPooling  
Conv2D (64 filters) → MaxPooling  
Conv2D (128 filters) → MaxPooling  
Flatten → Dense(128) → Dense(64) → Dense(1, sigmoid)
📊 Training
Optimizer: Adam

Loss: Binary Crossentropy

Metrics: Accuracy

Epochs: 10

python
Copy code
history = model.fit(train_ds, epochs=10, validation_data=validation_ds)
🎯 Example Output
✅ Input: dog.jpg → Dog 🐶
✅ Input: cat.jpg → Cat 🐱

📈 Accuracy & Loss Visualization
You can plot training performance with:

import matplotlib.pyplot as plt

plt.plot(history.history['accuracy'], label='Train Accuracy')
plt.plot(history.history['val_accuracy'], label='Val Accuracy')
plt.xlabel("Epochs")
plt.ylabel("Accuracy")
plt.legend()
plt.show()
🌟 Results
Achieved high accuracy on validation dataset 🏆

Robust CNN model for binary classification tasks

Can be extended for multi-class image classification

🤝 Contributing
Pull requests are welcome! Feel free to fork, improve, or suggest new features.

📜 License
This project is licensed under the MIT License.

Made with ❤️ using TensorFlow & Keras
