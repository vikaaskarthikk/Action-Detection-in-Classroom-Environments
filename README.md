# 🎯 Action Detection in Classroom Environment  
A real-time deep-learning system for detecting student actions such as **sitting, standing, walking, writing, sleeping, raising hand, and phone usage** using **YOLOv5**, **FastAPI**, and **React.js**. The project enables automated classroom monitoring, behavior analytics, and PDF report generation.

---

## 📌 Project Overview
This project implements a complete end-to-end pipeline to detect student behaviors from classroom videos using **YOLOv5 object detection**. It processes input videos, identifies actions frame-by-frame, and provides a detailed visual dashboard along with downloadable PDF reports.

The system achieves:

- ✅ **92.3% accuracy**  
- ⚡ **18 FPS real-time performance**  
- 📊 **Action analysis & proximity detection**  

It is designed for smart classroom environments to improve engagement analysis, discipline tracking, and automated monitoring.

---

## ⭐ Key Features
- 🔍 Real-time action detection using YOLOv5  
- 🎥 Video upload + automatic processing  
- 📊 Action distribution & behavior analytics  
- 📝 PDF report generation (jsPDF)  
- 🌐 Modern React UI with Tailwind CSS  
- ⚡ FastAPI backend for high-speed inference  
- 🔐 Privacy-focused (no data stored, edge processing)  
- 📏 Proximity-based action mapping  

---

## 🧱 System Architecture
```
React Frontend  →  FastAPI Backend  →  YOLOv5 Model  →  Results + PDF Report
```

### Components:
- **Frontend:** React.js, TypeScript, Tailwind CSS  
- **Backend:** FastAPI, Python, PyTorch, OpenCV  
- **Model:** YOLOv5 (custom-trained)  
- **Reporting:** jsPDF + AutoTable  

---

## 🗂️ Dataset & Annotation
Dataset includes actions:

- Sitting  
- Standing  
- Walking  
- Using Phone  
- Writing  
- Sleeping  
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

## 🤖 Model Training (YOLOv5)

### Training Example (YOLOv5)

```bash
python train.py --img 640 --batch 16 --epochs 50 --data data.yaml --weights yolov5s.pt
```

### Resuming Training
```bash
python train.py --resume
```

### Inference Example
```bash
python detect.py --weights best.pt --source video.mp4 --save-txt --save-conf
```

### Model Performance  
- **Accuracy:** 92.3%  
- **Inference Speed:** 18 FPS  
- **Precision/Recall:** High, stable  
- **Confusion Matrix:** Strong class-wise accuracy  
- **mAP:** As per validation metrics in training logs  

---

## 🔌 Backend (FastAPI)
Backend handles:

- Uploading video  
- Running YOLOv5 inference  
- Frame-by-frame analytics  
- Sending JSON results to frontend  
- Logging timestamps & counts  

### Run Backend
```bash
uvicorn app:app --reload
```

---

## 💻 Frontend (React)
Frontend features:

- Drag-and-drop video upload  
- Select **Action Detection** or **Proximity Mode**  
- Real-time playback of annotated video  
- Statistical dashboard for each processed video  
- Generate PDF report  

### Run Frontend
```bash
npm install
npm start
```

---

## 📝 PDF Report Generation
Reports include:

- Total frames, FPS, duration  
- Action counts & timestamps  
- Graphs and summary tables  
- Keyframes from detected actions  
- Proximity analysis insights  

Generated using:

- **jsPDF**
- **jsPDF AutoTable**

---

## 🧪 Results Summary

### Processing Metrics
- **Total Frames:** 703  
- **Video Duration:** 24.24 seconds  
- **Processing Speed:** 15.55 FPS  
- **Report Mode:** Action / Proximity  

### Detection Distribution
- **Sitting:** 50.8%  
- **Bench:** 30.2%  
- **Standing:** 19.0%  

### Model Performance Graphs
- Loss curve (box loss, cls loss, dfl loss)  
- F1 curve  
- Precision-confidence curve  
- Precision-recall curve  
- Confusion matrix  

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
│   ├── YOLOv5_training.ipynb
│
│── reports/
│
│── README.md
```

---

## 🔮 Future Enhancements
- Transformer-based action recognition  
- Multi-modal fusion (audio + video)  
- Real-time deployment on GPU servers  
- On-device (mobile/edge) inference  
- Multi-camera classroom monitoring  
- LMS Integration for learning analytics  

---

## 👨‍💻 Contributor
**Vikaas Karthik K – 1RV23SCN17**  
Department of CSE  
RV College of Engineering (RVCE)

- GitHub: https://github.com/vikaaskarthikk  
- Email: vikaaskarthik.k@gmail.com  

---

## 📜 License
Licensed under the **MIT License**.
