# Multi-Modal Hate Speech Detection System

A sophisticated system that detects hate speech across multiple modalities: text (English and Hinglish), images, and audio.

## Features

- **Multi-Modal Analysis**:
  - Text Analysis (English & Hinglish)
  - Image Analysis (Hate symbols detection)
  - Audio Analysis (Speech-to-text and hate content detection)

- **Advanced Pipeline**:
  1. Automatic modality detection
  2. Language detection for text
  3. External tools integration (hate detection, sentiment analysis)
  4. Chain-of-thought reasoning using Gemini LLM

## Setup

1. **Environment Setup**:
   ```bash
   pip install -r requirements.txt
   ```

2. **Configuration**:
   - Copy sample.env to .env
   - Add required API keys:
     - GEMINI_API_KEY
     - GOOGLE_API_KEY
     - LANGSMITH_API_KEY
     - OPENROUTER_API_KEY

## Project Structure

```
.
├── ML_MiniProj_Hate.ipynb    # Main project notebook
├── requirements.txt          # Project dependencies
├── .env                     # API keys (not tracked)
├── sample.env               # Template for .env
├── hate_audio.wav          # Sample audio file
└── swastika.png            # Sample image file
```

## Models

- **Text Models**:
  - Hinglish: [`dj-dawgs-ipd/IPD-Hinglish-Text-Model`](https://huggingface.space/dj-dawgs-ipd/IPD-Hinglish-Text-Model)
  - English: [`dj-dawgs-ipd/IPD-Text-English-Finetune`](https://huggingface.space/dj-dawgs-ipd/IPD-Text-English-Finetune)
- **Image Model**: [`dj-dawgs-ipd/IPD_IMAGE_PIPELINE`](https://huggingface.space/dj-dawgs-ipd/IPD_IMAGE_PIPELINE)
- **Audio Model**: [`dj-dawgs-ipd/IPD-Audio-Pipeline`](https://huggingface.space/dj-dawgs-ipd/IPD-Audio-Pipeline)
- **Sentiment Analysis**: [`distilbert-base-uncased-finetuned-sst-2-english`](https://huggingface.co/distilbert/distilbert-base-uncased-finetuned-sst-2-english)

## Usage

Open ML_MiniProj_Hate.ipynb and run the cells to:
- Set up the environment
- Initialize models and tools
- Run the hate speech detection pipeline
- Evaluate results on test examples

The system will detect the input modality and apply appropriate analysis tools to determine if hate speech is present.

## Testing

Sample test cases are included for:
- Hinglish text
- English text
- Image analysis
- Audio analysis

Each test provides a binary classification (Yes/No) and detailed reasoning.
