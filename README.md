# Transforming Waste Management Using Transfer Learning

This project applies transfer learning to classify types of waste (e.g., trash, plastic, metal, etc.) from images. By leveraging a pre-trained deep learning model, it predicts the category of waste based on visual features, enabling smarter waste sorting systems.

## 🧠 Project Overview

The model uses a pretrained CNN architecture (MobileNetV2) and fine-tunes it on a custom waste dataset. This helps in accurately identifying waste types even with limited training data.

## 🔍 Key Features

- Image classification using PyTorch and transfer learning  
- Real-time or batch prediction of waste type  
- Confidence score for each prediction  
- Handles image loading errors gracefully  

## 📁 Directory Structure

```
.
├── predict.py                 # Main prediction script
├── train.py                  # Training script (optional)
├── model.pth                 # Trained PyTorch model (not included here)
├── dataset/                  # Folder containing image dataset
├── requirements.txt          # Python dependencies
├── .gitignore                # Git ignore file
└── README.md                 # Project documentation
```

## 🖼️ Example Prediction

```
--- Prediction for: /content/results/predicted_gettyimages-157383990-612x612.jpg
Predicted Waste Type: Trash
Confidence: 0.9834
Predicted Class Index: 2
```

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/ashok910/waste.git
cd waste
```

### 2. Install Requirements

```bash
pip install -r requirements.txt
```

### 3. Load or Train Your Model

Place your trained model file as `model.pth` in the root directory.  
You can also train your own model using `train.py`.

### 4. Predict Waste Type

Update `test_image_path` in `predict.py` with your image path, and then run:

```bash
python predict.py
```

## ⚙️ Configuration

- Image size: 224x224  
- Normalization values: `[0.485, 0.456, 0.406]`, `[0.229, 0.224, 0.225]`  
- Device: GPU or CPU (automatically detected)

## 🧪 Dataset

The dataset should be structured like this:

```
TrashType_Image_Dataset/
├── metal/
├── trash/
├── plastic/
├── paper/
└── ...
```

The folder names will automatically become class labels using `ImageFolder`.

## 👨‍💻 Author

Vikram P  
[GitHub Profile](https://github.com/Vikram-tech512)

## 📄 License

This project is licensed under the [MIT License](LICENSE).

---

Feel free to contribute or raise issues!
