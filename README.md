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
- Notebook includes Flask API 
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
