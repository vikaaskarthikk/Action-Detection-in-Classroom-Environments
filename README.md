# 🎯 Action Detection in Classroom Environment  
A deep learning–based real-time system that detects and classifies classroom student actions such as **sitting, standing, walking, writing, sleeping, raising hand, and phone usage** using **YOLOv8**, **FastAPI**, and **React.js**. The system supports real-time monitoring, proximity analysis, and generates automated PDF reports for classroom analytics.

---

## 📌 Project Overview
This project implements a complete pipeline for classroom action monitoring using computer vision and deep learning. It identifies student activities from video input and provides insights such as action distribution, timestamps, and behavioral patterns. The system improves classroom management, enhances engagement analysis, and supports smart learning environments.

---

## ⭐ Key Features
- 🔍 Real-time action detection (YOLOv8)  
- 🎥 Video upload & automatic processing  
- 📊 Action statistics & visualization  
- 📝 PDF report generation using jsPDF  
- 🌐 Modern React UI  
- ⚡ FastAPI backend for high-speed inference  
- 🔐 Edge-based processing + privacy-friendly  
- 🧮 Proximity-based behavior detection  

---

## 🧱 System Architecture
```
React Frontend  →  FastAPI Backend  →  YOLOv8 Model  →  Results + Reports
```

### Components:
- **Frontend:** React, Tailwind CSS, Axios  
- **Backend:** FastAPI, Python, OpenCV, PyTorch  
- **Model:** YOLOv8  
- **Report:** jsPDF + AutoTable  

---

## 🗂️ Dataset & Annotation
Dataset contains annotated classroom actions including:
- Sitting  
- Standing  
- Walking  
- Sleeping  
- Using Phone  
- Writing  
- Raising Hand  

Annotated using **CVAT / Roboflow**.  
Dataset structure:

```
dataset/
│── images/
│   ├── train/
│   ├── val/
│── labels/
│   ├── train/
│   ├── val/
│── data.yaml
```

---

## 🤖 Model Training (YOLOv8)

### Training Example
```python
from ultralytics import YOLO

model = YOLO("yolov8n.pt")
model.train(data="data.yaml", epochs=50, imgsz=640)
```

### Inference Example
```python
model = YOLO("best.pt")
model.predict("video.mp4", save=True)
```

### Performance  
- **Accuracy:** 92.3%  
- **mAP50:** 0.992  
- **F1 Score:** 0.98  
- **Inference speed:** 15–18 FPS  

---

## 🔌 Backend (FastAPI)
The backend handles:
- Receiving uploaded videos  
- Frame processing  
- Running YOLO inference  
- Sending JSON + annotated outputs  
- Storing detection results  

### Run Backend
```bash
uvicorn app:app --reload
```

---

## 💻 Frontend (React)
Frontend provides:
- Drag & drop video upload  
- Action / Proximity detection mode  
- Real-time preview  
- Statistical dashboard  
- Downloadable PDF report  

### Run Frontend
```bash
npm install
npm start
```

---

## 📝 PDF Report Generation
Reports include:
- Action timestamps  
- Action summary table  
- Keyframes of detected events  
- Total detections  
- Video duration & FPS  
- Class-wise graph & distribution  

Generated using **jsPDF + AutoTable**.

---

## 🧪 Results Summary
- **Total Frames Processed:** 700+  
- **Processing Speed:** 15.55 FPS  
- **Top Classes:**  
  - Sitting (50.8%)  
  - Bench (30.2%)  
  - Standing (19%)  

Graphs included in report:
- Loss Curve  
- F1 Confidence Curve  
- Precision-Recall Curve  
- Confusion Matrix  

---

## 📁 Project Structure
```
Action-Detection-Classroom/
│── backend/
│   ├── app.py
│   ├── models/
│   ├── utils/
│   ├── requirements.txt
│
│── frontend/
│   ├── src/
│   ├── public/
│   ├── package.json
│
│── notebooks/
│   ├── YOLO_training.ipynb
│
│── reports/
│── README.md
```

---

## 🔮 Future Enhancements
- Multi-modal fusion (audio + video)  
- Transformer-based detection models  
- On-device inference (privacy-focused)  
- Multi-camera classroom analytics  
- Real-time edge deployment  
- LMS integration for academic analytics  

---

## 👨‍💻 Contributor  
**Vikaas Karthik K – 1RV23SCN17**  
Dept. of Computer Science & Engineering  
RV College of Engineering (RVCE)

- GitHub: https://github.com/vikaaskarthikk  
- Email: vikaaskarthik.k@gmail.com  

---

## 📜 License
Licensed under the **MIT License**.
