"""# BERT for Sentiment Classification (IMDB Dataset)

This model is a fine-tuned version of [bert-base-uncased](https://huggingface.co/bert-base-uncased) 
on the IMDB movie reviews dataset for **binary sentiment classification** (positive / negative).

## Model Details
- **Base model:** `bert-base-uncased`
- **Fine-tuning task:** Sentiment Analysis
- **Dataset:** IMDB
- **Language(s):** English
- **Framework:** PyTorch + Hugging Face Transformers

## Training
- **Batch size:** 16
- **Epochs:** 2
- **Optimizer:** AdamW
- **Learning rate:** 5e-5
- **Max sequence length:** 256

## Evaluation
- **Test Accuracy:** 83.6%

## Usage
```python
from transformers import pipeline

classifier = pipeline("sentiment-analysis", model="Avinash-panda/bert-sentiment-imdb")
print(classifier("The movie was fantastic!"))
