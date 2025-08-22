# 🌱 Potato Disease Classification (Learning Project)

## 📌 Project Overview
This is a **learning project** reproducing the Codebasics potato disease classification tutorial.  
Goal: understand the end-to-end flow of a CNN model served via a small API and tested from a web UI.

The model classifies potato leaf images into:
- `Early Blight`
- `Late Blight`
- `Healthy`

---

## 🧩 Tech Stack
- **Python 3.10+**, **TensorFlow/Keras**
- **FastAPI** + **Uvicorn**
- **React** + **Material-UI (@material-ui/core v4)**
- **Axios** for HTTP
- (Optional) **Docker**

---

## ⚙️ Setup

### 1️⃣ Backend
cd backend
pip install -r requirements.txt

If needed:
`pip install python-multipart pillow fastapi uvicorn tensorflow`

Start the API (choose one):

A) With uvicorn CLI
`uvicorn main:app --host 0.0.0.0 --port 8000 --reload`

B) Or run the script if main.py calls uvicorn.run(...)
`python main.py`

Test:
`curl http://localhost:8000/ping`
 -> "Hello I am alive"

---

### 2️⃣ Frontend
`cd frontend`
`npm install`
`npm audit fix`

Create your env file
Shell
`copy .env.example .env`


Edit `.env` and set the API URL:
`REACT_APP_API_URL=http://localhost:8000/predict`

Run the dev server
`npm start`

Open: `http://localhost:3000`

---

## 🚀 Usage
1. Start backend (port 8000).
2. Start frontend (port 3000).
3. Upload a potato leaf image in the web UI.
4. You’ll see the predicted class and confidence.

---

## 🔄 Adjustments vs Tutorial
- ✅ Updated versions in `requirements.txt` to keep the project working on current environments.
- ✅ Minor fixes in `home.js`:
  - `import axios from 'axios'`
  - Material-UI v4 prop `justify="center"` in `<Grid>`
  - `<CardMedia component="img" ... />`
  - Avoid variable shadowing with the background image.

Note: This repository simplifies parts of the original tutorial; it’s mainly a reproduction for learning purposes.

---

## 🙏 Acknowledgment
Based on the excellent learning material by Codebasics.  
This repo is a learning reproduction with minimal fixes to run in 2025.
