# Academic Support Ticket Classifier

AI-powered ticket classification system using DistilBERT to automatically categorize and route student support requests.

## Overview

Classifies student support tickets into 5 categories and automatically routes them to appropriate departments based on confidence thresholds.

MVP Screenshots
1. Admin Dashboard - Analytics Overview
The admin panel provides comprehensive platform analytics including total students, support tickets, AI resolutions, and satisfaction rates.
<img width="1920" height="991" alt="image" src="https://github.com/user-attachments/assets/30fe2436-ba4a-43c9-b996-9e7c70b4c997" />
<img width="1926" height="988" alt="image" src="https://github.com/user-attachments/assets/afcc461e-8046-4d28-9b4b-f3a2dc179bf7" />
<img width="1916" height="987" alt="image" src="https://github.com/user-attachments/assets/9666e51f-7f03-4969-abbd-bdc42d418ceb" />






4. Staff Directory - Find Your Facilitator
Browse the ALU staff directory to find facilitators by name, department, or expertise. Shows availability status and office hours with direct booking capability.
<img width="1922" height="991" alt="image" src="https://github.com/user-attachments/assets/fc709017-7e6d-40c1-a704-712b27aec9ad" />
<img width="1920" height="991" alt="image" src="https://github.com/user-attachments/assets/800548d2-5729-4e1a-a1c1-9bf84f737c85" />







**Categories:** Assignment Issues | Grade Appeals | Capstone | Administrative | General Inquiry

## Performance

- **Accuracy:** 90.2%
- **F1-Score:** 89.7%
- **Inference Time:** <500ms
- **Training Time:** ~2 minutes (GPU)

## Github repo
https://github.com/ktanguy/staffwork.git

## Tech Stack

- **Model:** DistilBERT (Hugging Face Transformers)
- **API:** Flask + Swagger UI
- **Framework:** PyTorch
- **Platform:** Google Colab
  
## video tutorial:
https://drive.google.com/file/d/1kBy5YiX6fEwhBBOXdYHrUhb6KK1nOUB8/view?usp=sharing   

## Quick Start

### Google Colab

1. Open `_fixed.ipynb` in Colab
2. Runtime → Change runtime type → GPU
3. Run all cells
4. API deploys automatically with public URL

### Local Setup
```bash
pip install torch transformers flask flask-restx scikit-learn pandas matplotlib seaborn

jupyter notebook _fixed.ipynb
```

## API Usage

**Classify a ticket:**
```bash
curl -X POST https://your-api-url.com/api/classify \
  -H "Content-Type: application/json" \
  -d '{"text": "I cant submit my assignment on Canvas"}'
```

**Response:**
```json
{
  "predicted_category": "Assignment Issues",
  "confidence": 0.95,
  "routing_action": "auto_assign",
  "assigned_to": "Academic Support"
}
```

## How It Works

1. Student submits support request
2. DistilBERT model classifies into 1 of 5 categories
3. If confidence ≥70% → Auto-assign to department
4. If confidence <70% → Flag for manual review


## Author

**Tanguy Kwizera**  

## License

MIT License
