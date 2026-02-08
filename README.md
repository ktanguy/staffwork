# Academic Support Ticket Classifier

AI-powered ticket classification system using DistilBERT to automatically categorize and route student support requests.

## Overview

Classifies student support tickets into 5 categories and automatically routes them to appropriate departments based on confidence thresholds.

**Categories:** Assignment Issues | Grade Appeals | Capstone | Administrative | General Inquiry

## Performance

- **Accuracy:** 90.2%
- **F1-Score:** 89.7%
- **Inference Time:** <500ms
- **Training Time:** ~2 minutes (GPU)

## Tech Stack

- **Model:** DistilBERT (Hugging Face Transformers)
- **API:** Flask + Swagger UI
- **Framework:** PyTorch
- **Platform:** Google Colab
  
## video tutorial:
https://youtu.be/8qNNNuxweME  

## Quick Start

### Google Colab

1. Open `_fixed.ipynb` in Colab
2. Runtime → Change runtime type → GPU
3. Run all cells
4. API deploys automatically with public URL

### Local Setup
```bash
pip install torch transformers flask flask-restx scikit-learn pandas matplotlib seaborn

jupyter notebook academic_support_classifier.ipynb
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
