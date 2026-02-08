# Academic Support Ticket Classifier - ML Demo

## Project Description

AI-powered academic support ticket classification system using fine-tuned DistilBERT to automatically categorize and route student support requests across 5 categories:
- Assignment Issues
- Grade Appeals  
- Capstone
- Administrative
- General Inquiry

### Prerequisites
- Google Colab (for training)
- Python 3.8+
- GPU recommended (available free in Colab)

### Running the Notebook

1. Open the notebook in Google Colab
2. Runtime → Change runtime type → GPU
3. Run all cells sequentially
4. Section 10 will deploy the API with public URL

### Model Training
- **Training Data:** 250 labeled student support requests
- **Model:** DistilBERT (distilbert-base-uncased)
- **Training Time:** ~2-4 hours on Colab free GPU
- **Accuracy:** 85-95%

### API Deployment
The notebook includes a Flask API with Swagger UI documentation.
- Automatically deploys via Cloudflare Tunnel
- Public URL generated on run
- Interactive testing at `/docs` endpoint




## API Endpoints

- `GET /api/health` - Health check
- `GET /api/categories` - List all categories
- `GET /api/stats` - Model statistics
- `POST /api/classify` - Classify support ticket

## Deployment Plan

**Current (Demo):**
- Google Colab notebook with embedded Flask API
- Cloudflare Tunnel for public access
- Temporary deployment for demonstration

**Future (Production):**
- Deploy Flask API to Render/Heroku
- React frontend for user interface
- PostgreSQL database for ticket storage
- Integration with university support system

## Video Demo

The demo video (5-10 minutes) covers:
1. Notebook walkthrough (Sections 1-9)
2. Model training results and metrics
3. API deployment (Section 10)
4. Swagger UI demonstration
5. Live ticket classification examples
6. Routing decision logic

## Technologies Used

- **ML Framework:** PyTorch, Transformers (Hugging Face)
- **Model:** DistilBERT
- **API:** Flask, Flask-RESTX
- **Deployment:** Cloudflare Tunnel
- **Visualization:** Matplotlib, Seaborn
- **Development:** Google Colab

## Contact

