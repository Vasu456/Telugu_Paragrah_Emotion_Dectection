# Telugu Emotion Detection using BERT

This project focuses on building an Emotion Detection System for Telugu Text using a fine-tuned multilingual BERT model. It predicts the intensity (in percentages) of four core emotions: Happy, Sad, Anger, and Fear from a given paragraph or sentence written in Telugu.

## Dataset Preparation

The dataset for this project was prepared manually due to the scarcity of labeled Telugu emotion datasets. The preparation involved the following steps:

### Data Collection
Telugu paragraphs were collected from multiple online resources, including:
- Telugu blogs
- Short stories
- Folk tales
- News articles
- Quotes and motivational content

Care was taken to ensure the dataset covers a diverse range of emotional expressions in Telugu.

### Emotion Annotation
For each paragraph, four emotion labels were used: Happy, Sad, Anger, and Fear. Instead of binary labels, percentage-based labels were assigned to represent the intensity of each emotion within the paragraph.


### Verification
The dataset underwent manual verification to ensure the correctness of emotion percentages. Multiple rounds of verification were done to minimize annotation bias.

## Setup Requirements
### Recommended Hardware
- **GPU:** NVIDIA T4 (Used via Google Colab)
- **VRAM:** At least 12 GB (T4 or better)

### Required Python Libraries
Install the following packages:
```bash
pip install transformers datasets torch sentencepiece accelerate 
```
## Step-by-Step Execution Guide

### Step 1: Preparing Environment
1. Open [Google Colab](https://colab.research.google.com)
2. Select **Runtime > Change runtime type > GPU**
3. Upload code.ipynb 

### Step 2: Upload Dataset
- **Format:** CSV (e.g., `data.csv`)
- **Columns required:** `Paragraph`, `happy`, `sad`, `anger`, `fear`

### Step 3: Emotion Prediction
- The model can predict emotion percentages for any new Telugu sentence.
Example usage:
```bash
new_sentence = "అతనికి చెప్పుకోలేని కష్టం వచ్చి పడింది." #change sentence here
predicted_emotions = predict_emotions(model, tokenizer, new_sentence)
print(predicted_emotions)
```
