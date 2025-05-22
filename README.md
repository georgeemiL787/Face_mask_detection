# 😷 Face Mask Detection

A deep learning project for detecting face masks in images and video streams using TensorFlow/Keras. Supports both command-line and web app interfaces.

---

## 🚀 Features

- Detects face masks in images and real-time video.
- Pre-trained models using MobileNetV2 and ResNet50V2.
- Easy-to-use web interface (Streamlit).
- Custom training on your own dataset.
- ONNX export for deployment.

---

## 🛠️ Installation

1. **Clone the repository:**
   ```sh
   git clone https://github.com/your-username/Face-Mask-Detection.git
   cd Face-Mask-Detection
   ```

2. **Create and activate a virtual environment (recommended):**
   ```sh
   python -m venv env
   # On Windows:
   .\env\Scripts\activate
   # On Unix/Mac:
   source env/bin/activate
   ```

3. **Install dependencies:**
   ```sh
   pip install -r requirements.txt
   ```

---

## 📦 Usage

### **Train a new model**
```sh
python train_mask_detector.py --dataset dataset
```

### **Detect masks in an image**
```sh
python detect_mask_image.py --image images/your_image.jpg
```

### **Detect masks in video (webcam)**
```sh
python detect_mask_video.py
```

### **Run the web app**
```sh
streamlit run app.py
```

---

## 🗂️ Project Structure

- `app.py` — Streamlit web app
- `train_mask_detector.py` — Model training script
- `detect_mask_image.py` — Image inference
- `detect_mask_video.py` — Video inference
- `model2onnx.py` — Export model to ONNX
- `dataset/` — Training data (with/without mask)
- `face_detector/` — Face detection models
- `css/` — Web app styles

---

## 🖥️ Example Output

### Training Output
```
[INFO] loading images...
[INFO] compiling model...
[INFO] training head...
[INFO] evaluating network...
              precision    recall  f1-score   support

      with_mask       0.98      0.97      0.98       138
   without_mask       0.97      0.98      0.98       138

    accuracy                           0.98       276
   macro avg       0.98      0.98      0.98       276
weighted avg       0.98      0.98      0.98       276
[INFO] saving mask detector model...
```

### Inference Output (Image/Video)
```
[INFO] loading face detector model...
[INFO] loading face mask detector model...
[INFO] computing face detections...
# The output window will display the image/video with bounding boxes and labels:
# Mask: 99.87%
# No Mask: 98.12%
```
