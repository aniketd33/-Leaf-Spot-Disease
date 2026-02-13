# 🌿 Leaf Disease Detection System  

An AI-powered Leaf Disease Detection System built with **FastAPI (Backend)** and **Streamlit (Frontend)** using **Meta Llama Vision models via Groq API**.  

This system detects plant diseases from leaf images, evaluates severity, and provides actionable treatment recommendations.

---

## 🚀 Live Demo  
[🌿 Leaf Spot Disease Project](https://aniketd33.github.io/-Leaf-Spot-Disease/)

 
🔗 Streamlit App:<img width="956" height="411" alt="image" src="https://github.com/user-attachments/assets/48cc35ff-7bb4-4164-ade8-2d6b5da43e31" />


---

# 🎯 Key Features  

## 🔍 Disease Detection  
- Detects 500+ plant diseases  
- Supports fungal, bacterial, viral, pest & nutrient issues  
- AI-powered image analysis  

## 📊 Severity Assessment  
- Mild / Moderate / Severe classification  
- Confidence score (0–100%)  

## 💡 Smart Recommendations  
- Evidence-based treatment suggestions  
- Symptom explanation  
- Possible causes  

## ⚡ Fast Processing  
- 2–5 second response time  
- Optimized inference pipeline  

---

# 🏗️ Project Architecture  

## 🔹 Frontend – `main.py`  
- Streamlit Web App  
- Image Upload  
- Result Display  
- API Integration  

## 🔹 Backend – `app.py`  
- FastAPI REST API  
- File Upload Endpoint  
- JSON Response Handling  

## 🔹 Core AI Engine – `Leaf Disease/main.py`  
- LeafDiseaseDetector Class  
- Groq API Integration  
- Base64 Image Processing  
- Structured JSON Output  

## 🔹 Utilities – `utils.py`  
- Image Processing  
- Base64 Conversion  
- Helper Functions  

---

# 📁 Project Structure  

Leaf-Disease-Detection/
│
├── main.py # Streamlit Frontend
├── app.py # FastAPI Backend
├── utils.py # Utility Functions
├── test_api.py # API Testing Script
├── requirements.txt # Dependencies
├── vercel.json # Deployment Config
│
├── Leaf Disease/
│ └── main.py # Core AI Engine
│
└── Media/ # Sample Images


---

# ⚙️ Installation Guide  

## 1️⃣ Clone Repository  


git clone https://github.com/aniketd33/Leaf-Disease-Detection.git
cd Leaf-Disease-Detection
2️⃣ Create Virtual Environment
Windows
python -m venv venv
venv\Scripts\activate
Mac/Linux
python -m venv venv
source venv/bin/activate
3️⃣ Install Dependencies
pip install -r requirements.txt
4️⃣ Setup Environment Variables
Create .env file:

GROQ_API_KEY=your_groq_api_key
MODEL_NAME=meta-llama/llama-4-scout-17b-16e-instruct
DEFAULT_TEMPERATURE=0.3
DEFAULT_MAX_TOKENS=1024
▶ Running the Application
🔹 Run Backend (FastAPI)
uvicorn app:app --reload --port 8000
Open:

http://localhost:8000/docs
🔹 Run Frontend (Streamlit)
streamlit run main.py
Open:

http://localhost:8501
🔹 Run Full Stack
Terminal 1:

uvicorn app:app --reload --port 8000
Terminal 2:

streamlit run main.py
📡 API Reference
POST /disease-detection-file
Upload image for disease detection.

Request:
Type: multipart/form-data

Field: file

Response Example:
{
  "disease_detected": true,
  "disease_name": "Brown Spot",
  "disease_type": "fungal",
  "severity": "moderate",
  "confidence": 89.3,
  "symptoms": [],
  "possible_causes": [],
  "treatment": [],
  "analysis_timestamp": "2026-02-13T12:00:00"
}
🧪 Testing
Run API test:

python test_api.py
Test with cURL:

curl -X POST "http://localhost:8000/disease-detection-file" \
-H "accept: application/json" \
-F "file=@Media/brown-spot-4 (1).jpg"
🌍 Deployment
🚀 Vercel (Backend)
npm install -g vercel
vercel --prod
Add environment variable:

GROQ_API_KEY

🌐 Streamlit Cloud (Frontend)
Push repo to GitHub

Connect to https://share.streamlit.io

Add secrets

🔬 Tech Stack
Python 3.9+

FastAPI

Streamlit

Groq API

Meta Llama Vision

Uvicorn

Requests

📊 Performance
Response Time: 2–5 seconds

Accuracy: 85–95%

Max Image Size: 10MB

Supports: JPG, PNG, WebP, BMP, TIFF

🤝 Contributing
git checkout -b feature/new-feature
git commit -m "Added new feature"
git push origin feature/new-feature
Create Pull Request on GitHub.

📜 License
MIT License

👨‍💻 Maintainer
Aniket Dombale
GitHub: https://github.com/aniketd33

<div align="center">
🌱 Empowering Agriculture Through AI 🌱

If this project helped you, please ⭐ star the repository!

</div> ```
