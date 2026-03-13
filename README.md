1️⃣ Copy This Entire README

Create or edit README.md in your GitHub repository and paste everything below.

# ✋ Air Writing & Gesture Recognition System

A real-time **Hand Gesture Recognition and Air-Writing System** built using **MediaPipe, OpenCV, and Support Vector Machines (SVM)**.  
The system allows users to interact with a computer by **performing hand gestures and writing letters in the air using their index finger**.

---

## 📌 Project Overview

Traditional computer interaction relies on keyboards, mice, or touchscreens.  
This project explores **touchless human-computer interaction** using computer vision.

The system detects hand landmarks from a webcam feed and performs:

• **Static Gesture Recognition**  
• **Air-Writing Character Recognition**

Both tasks are performed in **real time** using lightweight machine learning models.

---

## 🚀 Features

- Real-time hand tracking using MediaPipe
- Static hand gesture recognition
- Air-writing letter recognition
- Low-latency prediction
- Runs entirely on **CPU**
- Lightweight ML models (SVM)
- No deep learning required

---

## 🧠 System Architecture


Camera Input
↓
MediaPipe Hand Detection
↓
Hand Landmark Extraction (21 Points)
↓
Feature Processing

↓ ↓

Gesture Recognition Air Writing Detection
(Linear SVM) (Trajectory SVM)

↓
Prediction Output


---

## 🖼 System Pipeline


Webcam Frame
↓
Hand Landmark Detection
↓
Feature Extraction
↓
Mode Selection
↓
Gesture Classification / Air Writing Recognition
↓
Display Result


---

## 📊 Models Used

### Gesture Recognition Model
- Algorithm: **Linear Support Vector Machine (LinearSVC)**
- Features: 21 hand landmarks (x, y coordinates)
- Total features: **42**

### Air Writing Recognition Model
- Algorithm: **Support Vector Machine (RBF Kernel)**
- Features: normalized finger trajectory
- Feature length: **200**

---

## 📁 Project Structure


Air-Writing-Gesture-Recognition
│
├── dataset
│ ├── A
│ ├── L
│ ├── V
│ └── C
│
├── models
│ ├── svm_air_model.pkl
│ ├── scaler.pkl
│ └── gesture_control_svm.pkl
│
├── notebooks
│ ├── air_writing_training.ipynb
│ └── gesture_training.ipynb
│
├── src
│ └── hybrid_system.py
│
├── report
│ └── ACV_Project_Report.pdf
│
├── requirements.txt
└── README.md


---

## ⚙️ Installation

Clone the repository

```bash
git clone https://github.com/Gayathri47499/Air-Writing-Gesture-Recognition.git

Navigate to the project folder

cd Air-Writing-Gesture-Recognition

Install dependencies

pip install -r requirements.txt
▶️ Running the Project

Run the real-time system:

python src/hybrid_system.py

Controls:

Key	Action
F	Switch Mode
E	Predict Letter
C	Clear Text
Q	Quit
📈 Performance
Metric	Baseline	Improved
Gesture Accuracy	87%	90%
Air Writing Accuracy	~95%	~98–100%

The system performs real-time gesture recognition and air-writing detection using only CPU resources.

🧪 Challenges Faced

Similar gestures causing misclassification

Trajectory variation between users

Left-hand and right-hand landmark differences

Mode switching instability

Large gesture dataset training

🎓 Key Learnings

Landmark-based approaches reduce computational complexity

Feature normalization is crucial for trajectory-based models

Linear models scale better for large datasets

Dataset quality significantly impacts performance

🔮 Future Improvements

Recognize all 26 alphabets

Add dynamic gesture recognition

Integrate word prediction

Add text-to-speech output

Deploy as a web or mobile application

📚 Technologies Used

Python

MediaPipe

OpenCV

Scikit-Learn

NumPy

Matplotlib

📜 References

MediaPipe Hand Tracking Documentation

Scikit-Learn Documentation

OpenCV Computer Vision Library

👩‍💻 Author

Gayathri Sanjana
B.Tech – Data Science & Artificial Intelligence

GitHub:
https://github.com/Gayathri47499
