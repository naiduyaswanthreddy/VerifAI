# **VerfAI: AI-Powered Fake News & Deepfake Detection**

## 📌 Overview
**VerfAI** is an **AI-powered misinformation detection platform** that identifies **fake news and deepfake media** using state-of-the-art **Natural Language Processing (NLP) and Computer Vision (CV) models**. It features a **multilingual chatbot for automatic translation** and a **two-layered verification system**, ensuring high accuracy in detecting misinformation across different media formats.

## 🚀 Key Features
- ✅ **Multilingual Chatbot for Translation** – Converts regional language text into English using **mBART & self-attention mechanisms**  
- ✅ **Two-Layered Fake News Detection** – Combines **Google Fact Check API & Wikipedia API** with **DistilBERT (NLP Transformer)**  
- ✅ **Deepfake Detection with AI** – Uses **ExecutionNet (CNN-Based Model) + FastAPI** for real-time analysis  
- ✅ **User-Friendly Interface** – Supports **Web UI, Chrome Extension, and API-based integration**  
- ✅ **Optimized for Speed & Efficiency** – Deployable using **Docker, AWS/GCP**, ensuring fast and scalable processing  


## 🔬 Problem Statement
In today's digital world, misinformation spreads faster than ever. Fake news can **manipulate opinions, influence politics, and cause real-world harm.** Deepfake videos add another layer of deception, making it hard to differentiate **real from fake.**  

### 🚧 **Current Challenges & Gaps**
- ❌ **Language Barriers** – Existing fake news detection models are **English-centric**, ignoring regional misinformation  
- ❌ **Manual & Slow Verification** – Fact-checking is **time-consuming and lacks automation**  
- ❌ **Inefficient Deepfake Detection** – Many tools **fail at real-time analysis** of deepfake videos  
- ❌ **High Computational Costs** – AI-based models can be **expensive & difficult to scale**  

### ✅ **Why VerfAI?**
- ✅ **Multilingual Support** – Translates **regional language content** into English before analysis  
- ✅ **Layered Fake News Detection** – Uses **fact-checking APIs + AI model** for verification  
- ✅ **Fast & Scalable Deepfake Analysis** – Real-time **image & video deepfake detection** using ExecutionNet  
- ✅ **Low-Resource Optimized** – Balances **accuracy & efficiency** with **DistilBERT** for NLP tasks  


## 🏗 Architecture & Tech Stack  

### 🔹 **System Flow & Components**
1️⃣ **User Input Layer:**  
   - Users provide **text, URLs, or video files** via **Web UI, Chrome Extension, or API**  

2️⃣ **Multilingual Chatbot (Translation Module):**  
   - Uses **mBART (Sequence-to-Sequence Transformer Model)** for **regional language translation into English**  
   - Implements **Self-Attention Mechanism & On-the-Fly Transliteration** to maintain **tone, intent, and accuracy**  

3️⃣ **Fake News Detection (Two-Layered Approach):**  
   - **Layer 1:** **Google Fact Check API** & **Wikipedia API** for **real-time external verification**  
   - **Layer 2:** **DistilBERT Model** trained on **LIAR & IFND datasets** for deep **AI-driven credibility scoring**  
   - **Preprocessing:** Uses **NLTK for stopword removal & lemmatization**, and **DistilBertTokenizerFast for tokenization**  

4️⃣ **Deepfake Detection (Two-Layered Approach):**  
   - **Layer 1:** **FastAPI** for **efficient API-based inference**  
   - **Layer 2:** **ExecutionNet (CNN-Based AI Model)** trained on **deepfake image datasets**  
   - **Processing:** Extracts **video frames**, detects **manipulated regions**, and outputs **real or fake verdict**  

5️⃣ **Deployment & Integration:**  
   - **Backend:** Flask (Fake News API) + FastAPI (Deepfake API)  
   - **Frontend:** React.js for user interface  
   - **Database:** PostgreSQL for storing verification logs & results  
   - **Cloud & Containerization:** Docker for easy deployment, AWS/GCP for scalability  


## ⚙ Installation & Setup  

### 🔹 **Prerequisites**
- Python 3.8+  
- Flask & FastAPI  
- PostgreSQL  
- Node.js & React  
- Docker (for containerization)  

### 🔹 **Backend Setup**
```sh
# Clone the repository
git clone https://github.com/your-repo/VerfAI.git
cd VerfAI

# Install dependencies
pip install -r requirements.txt

# Run Flask API for fake news detection
python api.py

# Run FastAPI for deepfake detection
uvicorn deepfake_api:app --host 0.0.0.0 --port 8000
```

### 🔹 Frontend Setup
```sh
# Navigate to the frontend directory
cd frontend

# Install dependencies
npm install

# Start the React app
npm start
```

### 📜 API Endpoints
Fake News Detection API
🔹 Check API Status
```http
GET /api/status
```
🔹 Analyze Text for Fake News
```http
POST /api/analyze/text
```
Request Body:

```json
{ "text": "Some news content here..." }
```
🔹 Analyze URL for Fake News
```http
POST /api/analyze/url
```
Request Body:

```json
{ "url": "https://news-website.com/article" }
```
Deepfake Detection API
🔹 Upload Video for Deepfake Analysis
```http
POST /api/analyze/video
```
Request (multipart/form-data):

```sh
{ "video": "<video_file.mp4>" }
```

### 🎯 Conclusion
VerfAI is a powerful, AI-driven misinformation detection platform that leverages NLP, deep learning, and external fact-checking sources to identify fake news and deepfake media. By providing real-time, multilingual, and scalable solutions, VerfAI helps combat digital deception effectively.
