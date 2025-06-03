# 🧠 Silent Speech Recognition via Lip Reading

## 🎯 Objective
To develop a **silent speech recognition system** that can convert lip movements into text, enabling communication for individuals who are speech impaired. This system will use **machine learning**, **facial landmark detection**, and **real-time inference** to recognize speech without relying on audio input.

---

## 📦 Project Overview

### 🔁 Pipeline

```
[Webcam Input] → [Lip Landmark Detection] → [Feature Extraction] → [ML Model] → [Text Prediction]
```

### 🛠️ Tools & Libraries

| Functionality              | Tool                        |
|---------------------------|-----------------------------|
| Lip Landmark Detection     | MediaPipe / Dlib / OpenCV   |
| Machine Learning Model     | PyTorch / TensorFlow        |
| Real-Time Input & Display  | OpenCV / Tkinter            |
| Optimization (optional)    | ONNX / TensorRT             |

---

## 🔍 Core Concepts

- **Landmark Detection**: Detect and extract coordinates of mouth landmarks.
- **Sequence Modeling**: Use RNNs or Transformers to model the motion over time.
- **Text Decoding**: Predict characters or words from input features.

---

## 🧪 Step-by-Step Guide

### ✅ 1. Data Collection & Preprocessing
- Use datasets like **GRID**, **TCD-TIMIT**, or record your own video clips.
- Extract lip landmarks or crop the mouth region.
- Normalize and store sequences with text labels.

### ✅ 2. Model Training
- Model type: **CNN + LSTM**, **3D CNN**, or **Transformer**.
- Input: Sequence of frames or landmark vectors.
- Output: Sequence of characters or words.
- Loss: Use **CTC Loss** for unaligned sequence prediction.

### ✅ 3. Real-Time Inference
- Capture live webcam input.
- Detect and preprocess mouth/lip region.
- Run through trained model.
- Display predicted text in real time.

---

## 📁 Suggested Project Structure

```
silent_speech_project/
├── data/                # Video clips or landmark sequences
├── models/              # Trained models
├── scripts/
│   ├── detect.py        # Lip landmark detection
│   ├── train.py         # Model training
│   ├── predict.py       # Real-time prediction
│   └── gui.py           # Optional interface (Tkinter/OpenCV)
├── README.md
├── requirements.txt
└── config.yaml
```

---

## 💡 Tips for Success

- Start with a **limited vocabulary** (e.g., 10 common phrases).
- Ensure consistent **lighting and camera angle** for better accuracy.
- Test with **landmarks** and **raw image frames** to compare performance.
- Add **visual feedback** on screen to help the user confirm recognition.

---

## 🧠 Learning Outcomes

By completing this project, you will:
- Understand how to process video and extract facial features.
- Train a sequence model for a real-world task.
- Build a real-time inference pipeline for assistive communication.

---

## 📚 Further Reading

- [GRID Dataset](https://spandh.dcs.shef.ac.uk/gridcorpus/)
- [LRS3 Dataset](https://www.robots.ox.ac.uk/~vgg/data/lip_reading/lrs3.html)
- [CTC Loss – Distill.pub](https://distill.pub/2017/ctc/)

---

## 👩‍💻 License

This project is for educational and assistive technology research purposes.
