# Academic Support Ticket Classifier

AI-powered ticket classification system using DistilBERT to automatically categorize and route student support requests.

## Overview

Classifies student support tickets into 5 categories and automatically routes them to appropriate departments based on confidence thresholds.

MVP Screenshots
1. Admin Dashboard - Analytics Overview
The admin panel provides comprehensive platform analytics including total students, support tickets, AI resolutions, and satisfaction rates.
<img width="1680" height="865" alt="Screenshot 2026-02-16 at 3 05 42 PM" src="https://github.com/user-attachments/assets/80df88c1-8991-4795-be50-f3db0b06aecc" />
<img width="1902" height="927" alt="Screenshot 2026-02-15 at 3 23 18 PM" src="https://github.com/user-attachments/assets/7acebedd-9226-4ac6-ac80-74c983c91465" />

4. Staff Directory - Find Your Facilitator
Browse the ALU staff directory to find facilitators by name, department, or expertise. Shows availability status and office hours with direct booking capability.
<img width="1680" height="958" alt="Screenshot 2026-02-16 at 2 53 43 PM" src="https://github.com/user-attachments/assets/c004a06a-aa93-4999-8a01-095d3fa91c24" />
<img width="1919" height="929" alt="Screenshot 2026-02-15 at 3 24 40 PM" src="https://github.com/user-attachments/assets/c200d50d-55b5-4057-aec9-db00d48d58c8" />




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
https://drive.google.com/file/d/1GTxEN4jurraM7mhB14F_0OjKRi9OPy3j/view?usp=sharing  

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
