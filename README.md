# AirQueue AI — Real-Time Crowd & Queue Intelligence Platform  
### AI-powered public safety system for airports, transport hubs & disaster relief centers  
**Tech Stack:** YOLOv8 · OpenCV · Python · CustomTkinter · Firebase · Cloud Functions · Streamlit/React

---

## 🚨 Overview
**AirQueue AI** transforms any CCTV or mobile camera into an **AI-powered crowd safety sensor**.

It provides:
- Real-time passenger/person detection  
- Queue length monitoring  
- Density analytics  
- Overcrowding Risk Score (0–100%)  
- Predictive wait-time estimation  
- Cloud alerts & live dashboard  

Originally designed for **airports**, the system adapts seamlessly to:
- Disaster relief centers  
- Emergency shelters  
- Railway/metro stations  
- Hospitals & OPDs  
- Government service queues  
- Large public events  

---

## 🎯 Key Features

### 🔵 Real-Time AI Detection
- YOLOv8 person detection (20–30 FPS on CPU)  
- Centroid tracking for movement stability  

### 🔵 Queue Intelligence
- Define queue zone with 2 clicks  
- Continuous queue-length estimation  
- Wait-time prediction based on service rate  

### 🔵 Crowd Safety Analytics
- Density % calculation  
- Overcrowding Risk Score (0–100%)  
- Heatmaps of high-traffic areas  
- Audio alert when thresholds exceed  

### 🔵 Google Cloud Integration
- Firebase Realtime Database metric sync  
- Cloud Functions for automated alerts  
- Cloud dashboard (React/Streamlit)  

### 🔵 Additional Capabilities
- Snapshot saving  
- CSV logging for analytics  
- Phone IP camera / CCTV support  
- Offline privacy-safe mode  

---

## 🛠 Technology Stack

### **AI / Computer Vision**
- YOLOv8 (Ultralytics)  
- OpenCV  
- Centroid Tracker  
- Numpy, Pillow  

### **Application Layer**
- Python  
- CustomTkinter (UI)  
- Multithreading  

### **Google Cloud**
- Firebase Realtime Database  
- Firebase Cloud Functions  
- Firebase Hosting  
- (Optional) BigQuery for long-term analytics  

---

## 🏗 System Architecture
```
Camera Feed (CCTV / Phone)
↓
YOLOv8 Detection
↓
Centroid Tracking → Queue Zone Analysis → Density Metrics
↓
Local App UI (Python)
↓
Firebase Realtime Database (metrics only)
↓
Cloud Functions → Alerts (SMS/Email/Push)
↓
Control Dashboard (React/Streamlit)
Camera Feed (CCTV / Phone)
↓
YOLOv8 Detection
↓
Centroid Tracking → Queue Zone Analysis → Density Metrics
↓
Local App UI (Python / CustomTkinter)
↓
Firebase Realtime Database (metrics only)
↓
Cloud Functions → Alerts (SMS / Push / Dashboard)
↓
Control Dashboard (Streamlit / React)
```

---

## 📦 Installation & Setup

### 1. Clone the Repository
```
git clone https://github.com/<your-username>/AirQueue-AI.git
cd AirQueue-AI
```

2. Install Dependencies
```
pip install -r requirements.txt
```
4. Run the Application
```
python main.py --source 0
```

Using Phone IP Camera:
```
python main.py --source "http://<IP>:8080/video"
```
☁️ Firebase Integration (Optional)
```
Example Database Structure
{
  "airqueue": {
    "queue_length": 12,
    "density_pct": 58,
    "risk_score": 72,
    "estimated_wait": 310
  }
}
```
Cloud Functions

Triggers alerts when:

```risk_score > threshold```

```density_pct > safe_limit```

📊 Use Cases

-- Airport queue & security control

--Railway/metro crowd analytics

--Disaster relief distribution

-- Hospital OPD queues

-- Government office service lines

-- Stadiums & events


