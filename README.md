# Classification-of-Disease-Brain-Tumor
# 🧠 Brain Tumor Detection with VGG16 🔬

Welcome to one of the most impactful applications of Deep Learning in Healthcare! This project leverages **Transfer Learning** with the **VGG16** architecture to classify **brain MRI scans** into different tumor categories. Designed to be **accurate**, **scalable**, and **privacy-conscious**, this repository is a step toward smarter, AI-driven medical diagnostics.

---

## 🚀 Project Highlights

- ✅ **Transfer Learning with VGG16** (pre-trained on ImageNet)
- 🧪 Classification of MRI images into: `Glioma`, `Meningioma`, `Pituitary`, or `No Tumor`
- 📊 Confusion Matrix, Accuracy-Loss Visualization, and Real Sample Display
- 📁 Custom Data Generator for Efficient Training
- 🔒 Modular and Extensible for real-world healthcare integration

---

## 📂 Dataset Structure

The model was trained and tested on a labeled MRI image dataset organized as:

/MRI Images ├── Training/ │ ├── glioma/ │ ├── meningioma/ │ ├── pituitary/ │ └── no/ └── Testing/ ├── glioma/ ├── meningioma/ ├── pituitary/ └── no/

> 💡 Each subfolder contains MRI scans of the corresponding tumor type.

---

## 🏗️ Model Architecture

We built on the VGG16 backbone and fine-tuned the last few layers:

- 🔹 Input Image: `128x128x3`
- 🔹 Base: `VGG16 (frozen with partial fine-tuning)`
- 🔹 Layers: `Flatten → Dropout → Dense → Dropout → Softmax`

Training parameters:

```python
optimizer = Adam(learning_rate=1e-4)
loss = sparse_categorical_crossentropy
epochs = 5
batch_size = 20

📊 Results Visualization
✅ Accuracy vs. Epoch

❌ Loss vs. Epoch

🧩 Confusion Matrix

🖼️ Random MRI Sample Previews with Labels and Sizes

These visualizations offer intuitive understanding of model performance and behavior.

🛠️ How to Use
Clone the repository:

bash
Copy
Edit
git clone https://github.com/your-username/brain-tumor-vgg16.git
cd brain-tumor-vgg16
Mount your Google Drive (if using Colab):

python
Copy
Edit
from google.colab import drive
drive.mount('/content/drive')
Install dependencies:

bash
Copy
Edit
pip install tensorflow matplotlib seaborn scikit-learn
Train the model or evaluate:

python
Copy
Edit
model.fit(...)
evaluate_model(...)
📌 Future Work
🧠 Integrate Federated Learning for privacy-preserving training

🛡️ Add Blockchain-based data integrity verification

⚛️ Explore Quantum-AI fusion for model acceleration

🤝 Contributing
We love contributions! Feel free to fork, submit pull requests, or open issues. Make sure to follow our contribution guidelines and keep it constructive 🚀

📜 License
This project is licensed under the MIT License.

🙌 Acknowledgements
VGG16 - Keras Applications

Brain MRI Dataset (Kaggle)

⭐ Show Your Support
If you found this project helpful, give it a ⭐ and consider sharing it! Every star motivates me to improve and build more!

"Deep learning is not just math, it's the future of medicine." – You, after trying this out.

yaml
Copy
Edit

---

Let me know if you want badges, an animated demo, or deployment instructions added too!
