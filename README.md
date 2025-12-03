# 🤖 AI Text Detector

An advanced ensemble machine learning system for detecting AI-generated text using RoBERTa-based models.

## 📋 Overview

This application uses a fine-tuned RoBERTa model to classify text as either human-written or AI-generated. The system provides confidence scores and detailed predictions through an intuitive web interface.

## ✨ Features

- **Real-time Detection**: Instant analysis of text input
- **Confidence Scoring**: Probability scores for both human and AI-generated classifications
- **Ensemble Model**: Powered by RoBERTa-base transformer model
- **Web Interface**: Clean, user-friendly HTML interface
- **REST API**: Flask-based backend for easy integration

## 🛠️ Technology Stack

- **Backend**: Flask (Python)
- **ML Framework**: PyTorch, Transformers (Hugging Face)
- **Model**: RoBERTa-base (fine-tuned)
- **Deployment**: Gunicorn, Render
- **Frontend**: HTML, CSS, JavaScript

## 📦 Installation

### Prerequisites

- Python 3.11+
- pip

### Local Setup

1. Clone the repository:
```bash
git clone <your-repo-url>
cd "Ensemble model"
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

3. Run the application:
```bash
python app.py
```

4. Open browser and navigate to:
```
http://localhost:5000
```

## 🚀 Deployment

### Deploy to Render

1. Push code to GitHub
2. Connect repository to Render
3. Render will automatically detect `Procfile` and deploy
4. Environment: Python 3.11
5. Build Command: `pip install -r requirements.txt`
6. Start Command: `gunicorn app:app`

## 📁 Project Structure

```
Ensemble model/
├── app.py                      # Flask application
├── index.html                  # Frontend interface
├── requirements.txt            # Python dependencies
├── Procfile                    # Render deployment config
├── render.yaml                 # Render service config
├── .gitignore                  # Git ignore rules
└── ensemble_models/
    └── roberta-base/          # Fine-tuned RoBERTa model
        ├── model.safetensors  # Model weights (~475MB)
        ├── config.json
        ├── tokenizer.json
        └── ...
```

## 🔧 API Usage

### Endpoint: `/predict`

**Method**: POST

**Request Body**:
```json
{
  "text": "Your text to analyze here..."
}
```

**Response**:
```json
{
  "prediction": "Human" | "AI-generated",
  "confidence": 0.95,
  "probabilities": {
    "human": 0.95,
    "ai": 0.05
  }
}
```

## 🎯 Model Details

- **Base Model**: roberta-base
- **Fine-tuning**: Custom ensemble approach
- **Input**: Text sequences (up to 512 tokens)
- **Output**: Binary classification (Human/AI)
- **Performance**: High accuracy on diverse text types

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📄 License

This project is licensed under the MIT License.

## 👤 Author

Created by [Your Name]

## 🙏 Acknowledgments

- Hugging Face for the Transformers library
- RoBERTa model by Facebook AI
- Flask framework developers

## 📞 Support

For issues and questions, please open an issue on GitHub.

---

**Note**: The model files are large (~475MB). Consider using Git LFS for version control.