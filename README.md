# Academic Support Ticket Classifier - ML Demo

**Author:** Tanguy Kwizera  
**Course:** BSc Software Engineering  
**Institution:** African Leadership University  
**Date:** February 8, 2026  
**Supervisor:** Simeon Nsabiyumva

## Project Description

AI-powered academic support ticket classification system using fine-tuned DistilBERT to automatically categorize and route student support requests.

**Categories:**
- Assignment Issues
- Grade Appeals
- Capstone
- Administrative
- General Inquiry

## Files Included

- `academic_support_classifier.ipynb` - Complete training notebook
- `screenshots/` - Training results and visualizations
- `demo_video.mp4` - Video demonstration (or link)
- `README.md` - This file

## How to Run

### Prerequisites
- Google Colab account
- GPU runtime (free tier)

### Steps
1. Upload notebook to Google Colab
2. Runtime → Change runtime type → GPU
3. Run all cells sequentially
4. Model will train in ~2-4 minutes
5. Section 10 deploys the API with public URL

## Model Performance

- **Architecture:** DistilBERT
- **Training Epochs:** 3
- **Training Time:** ~2 minutes (Colab GPU)
- **Accuracy:** 90.2%
- **F1-Score:** 89.7%
- **Precision:** 92.1%
- **Recall:** 90.2%

## Technologies Used

- **ML Framework:** PyTorch, Transformers (Hugging Face)
- **Model:** DistilBERT
- **API:** Flask, Flask-RESTX (Swagger)
- **Deployment:** Cloudflare Tunnel (demo)
- **Visualization:** Matplotlib, Seaborn
- **Platform:** Google Colab

## Deployment

**Demo Deployment:**
- Notebook includes Flask API (Section 10)
- Cloudflare Tunnel for public access
- Swagger UI at `/docs` endpoint

**Future Production:**
- Deploy to Render/Heroku
- React frontend
- PostgreSQL database
- Full integration with university system

## Video Demo

[Link to video or note that it's included in submission]

The demo covers:
1. Notebook walkthrough
2. Model training and results
3. API deployment
4. Live classification examples

## Contact

Tanguy Kwizera  
African Leadership University
```

---

### **4. Record Quick Video (15-20 minutes)**

**Option A: Screen Record Colab (Simplest)**

Use free screen recorder:
- **Windows:** Xbox Game Bar (Win + G)
- **Mac:** QuickTime Player (Cmd + Shift + 5)
- **Chrome Extension:** Loom (free)

**Script (5-7 minutes):**
```
00:00 - 00:30 | Introduction
"Hi, I'm Tanguy Kwizera. This is my ML demo for the Academic Support Ticket Classifier using DistilBERT."

00:30 - 02:00 | Show Notebook
- Scroll through Sections 1-2 (data generation)
- "Here I generated 250 labeled training samples across 5 categories"
- Show Section 3 (visualizations)
- "Data distribution is balanced across all categories"

02:00 - 04:00 | Training Results
- Show Section 6 (evaluation)
- "The model achieved 90.2% accuracy after 3 epochs"
- Show confusion matrix
- "You can see strong performance across all categories"

04:00 - 05:30 | API Demo (if working)
- Show Section 10
- "I deployed this as a REST API with Swagger UI"
- Show the public URL
- Open Swagger in browser (if working)
- Test one classification

05:30 - 06:00 | Conclusion
"This system solves the fragmented support problem at ALU by automatically routing tickets. Next steps would be full deployment. Thank you."
```

**Option B: If API Not Working**

Just show the notebook + explain:
- "The API deployment is in Section 10"
- "It creates a public URL with Swagger UI"
- "Here's how it would work..." (explain the flow)

---

### **5. Create the ZIP File**

**On your computer:**

1. Create folder: `tanguy_kwizera_ml_demo`
2. Put all files inside
3. Right-click → Compress/Send to → Compressed folder
4. Rename to: `tanguy_kwizera_ml_demo.zip`

---

## **⚡ ABSOLUTE MINIMUM (if very rushed - 30 min total):**
```
submission.zip
├── README.md (10 min - use template above)
├── academic_support_classifier.ipynb (already have)
└── screenshots/
    ├── training_metrics.png (screenshot from notebook)
    └── confusion_matrix.png (screenshot from notebook)
