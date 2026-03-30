# 🔥 Fire Detection using YOLOv8

This project uses a custom-trained YOLOv8 model to detect fire in real-time using a live camera feed. 

---

## 🚀 Features
- **Real-Time Detection:** Processes live video feed using OpenCV.
- **Custom AI Model:** Powered by a YOLOv8 model trained specifically on fire datasets.
- **Adjustable Confidence:** Easily tweak the detection threshold for strict or loose detection.
- **Lightweight & Fast:** Designed to run efficiently on local hardware.

---

## 📦 Setup & Installation

### 1. Clone the repository
`git clone https://github.com/YOUR_USERNAME/fire-detection-yolov8.git`
`cd fire-detection-yolov8`

### 2. Install dependencies
Make sure you have Python installed, then run:
`pip install -r requirements.txt`

### 3. Run the Project
`python main.py`
*(Press 'q' to quit the video stream).*

---

## ⚙️ How to Adjust Confidence
Inside `detect.py`, you can change the confidence threshold to make the AI more or less strict.
`results = model(frame, conf=0.5)` 

---

## 📊 Dataset & Training
- **Dataset Source:** Roboflow Fire Dataset (includes diverse fire and non-fire images to prevent false positives)
- **url link for dataset:** https://universe.roboflow.com/-jwzpw/continuous_fire
- **Format:** YOLOv8
- **Hardware Used:** Trained on Google Colab using a Tesla T4 GPU.
- **Training Command:** `yolo task=detect mode=train model=yolov8n.pt data=data.yaml epochs=80`
- **Model Output:** `best.pt` (This is the weights file driving the detection).

---

## 🚨 HOW I USED IT
I used it in my project where I developed a fire fighting system
This model serves as the vision system for autonomous fire-fighting robots. 
When the camera in the main fire station continuously scans an area and detects fire, it triggers an alert and deploys the main truck and smaller water-spraying cars to the target location.


---
**Author:** Muhammad Ahmed
