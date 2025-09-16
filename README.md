# 🧠 Brain Tumor Classification

A full‑stack deep learning project for **classifying brain MRI scans** into tumor types.  
It combines a **ResNet50 CNN model**, a **FastAPI backend**, and a **Next.js + Tailwind frontend**.

---

## 🚀 Features
- Multi‑class classification: **glioma, meningioma, pituitary, normal**.
- Deep learning model built on **ResNet50** (transfer learning).
- REST API powered by **FastAPI** for inference (`/infer` endpoint).
- Modern **Next.js frontend** with interactive pages:
  - Upload new scans (`/new-scan`)
  - View results (`/result`)
  - Explore tumor details (`/tumor-details`)
  - Inspect model insights (`/model-insights`)
- PDF report generation for predictions.

---

## 📂 Project Structure
```
Brain-Tumor-Classification/
├── backend/              # FastAPI backend
│   ├── main.py           # API with /infer endpoint
│   ├── requirements.txt  # Backend dependencies
│   └── best_model.h5     # Trained ResNet50 model
├── frontend/             # Next.js + Tailwind app
│   ├── app/              # Pages & components
│   │   ├── new-scan/     # Upload MRI scan
│   │   ├── result/       # Show prediction result
│   │   ├── tumor-details # Info about tumor type
│   │   └── model-insights# Accuracy, loss, metrics
│   └── package.json      # Frontend dependencies
├── brain-tumor-types/    # Dataset (glioma, meningioma, pituitary, normal)
├── ResNet50.ipynb        # Training notebook
└── README.md
```

---

## ⚙️ Installation

### Backend
```bash
cd backend
pip install -r requirements.txt
python main.py
```

### Frontend
```bash
cd frontend
npm install
npm run dev
```

---

## ▶️ Usage

1. Start the backend server:
   ```bash
   python main.py 
   ```
   - Endpoint: `POST /infer` (accepts image, returns prediction).

2. Start the frontend:
   ```bash
   npm run dev
   ```
   - Open browser at `http://localhost:3000`.

3. Upload MRI scans, view predictions, and download reports.

---

## 📊 Model Training
- Implemented in **ResNet50.ipynb**.
- Transfer learning on ImageNet weights.
- Achieves high accuracy on test dataset.
- Augmentation: rotation, zoom, shift, normalization.

---

## 📊 Dataset
The dataset contains MRI scans in 4 classes:
| Class       | Description                  |
|-------------|------------------------------|
| Glioma      | Tumor from glial cells       |
| Meningioma  | Tumor from meninges          |
| Pituitary   | Tumor from pituitary gland   |
| Normal      | No tumor present             |

---

## ⚠️ Limitations
- Model trained on limited dataset size.
- May not generalize to unseen MRI formats.
- Clinical use requires further validation.

---

## 📝 License
MIT License – free to use and modify.

---

## 🙌 Acknowledgments
- Kaggle Brain MRI datasets  
- TensorFlow & Keras community  
- FastAPI and Next.js contributors  
