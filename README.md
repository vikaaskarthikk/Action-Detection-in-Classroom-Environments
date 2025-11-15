# 🎯 Action Detection in Classroom Environments  
Real-time action detection system built using **YOLO**, **FastAPI**, and **React**, designed to monitor and identify key actions in classroom environments such as raising hands, standing, sitting, writing, interacting, and more. The system supports real-time video streaming and inference for classroom behavior analysis.

---

## 📌 Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Project Architecture](#project-architecture)
- [Dataset](#dataset)
- [Model Training](#model-training)
- [Backend (FastAPI)](#backend-fastapi)
- [Frontend (React)](#frontend-react)
- [How to Run](#how-to-run)
- [Results](#results)
- [Future Improvements](#future-improvements)
- [Contributors](#contributors)
- [License](#license)

---

## 📍 Overview
This project aims to automate classroom activity monitoring by detecting various student and teacher actions using deep learning models. Built with **YOLO** for real-time object/action detection, the system captures classroom video, processes frames through a FastAPI backend, and displays the detected actions live on a React frontend.

The solution can be extended for:
- Smart classrooms  
- Behavioral analysis  
- Attendance automation  
- Classroom participation analytics  

---

## ⭐ Features
- 🎥 Real-time video stream detection  
- 🚀 Fast inference powered by YOLO  
- 🌐 FastAPI backend for model processing  
- 💻 React frontend for live view and UI  
- 📊 Supports multiple classroom-related actions  
- 🔧 Easy to extend with new actions or datasets  
- 📁 Modular and scalable folder structure  

---

## 🛠️ Tech Stack
### **Deep Learning & CV**
- YOLOv8 / YOLOv5 (depending on final model used)
- OpenCV
- Python

### **Backend**
- FastAPI  
- Uvicorn  
- Python 3.8+  

### **Frontend**
- React.js  
- Axios  
- JavaScript  

### **Others**
- Google Colab (model training)  
- Google Drive (weights & dataset storage)  

---

## 🧱 Project Architecture
