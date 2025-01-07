# AI-Integrated-Medical-Specialty-Predictor

This repository contains the implementation and results of the **AI-Powered Diagnostic Assistant**, a project designed to assist healthcare providers by predicting the most relevant medical specialty for a given case based on clinical data.

---

## Dataset

- **Source**: [Medical Transcriptions Dataset (Kaggle)](https://www.kaggle.com/datasets/tboyle10/medicaltranscriptions/data)
- **Attributes**:
  - **Description**: A summary of the patient's condition or procedure.
  - **Transcription**: Detailed clinical notes and reports.
  - **Keywords**: Extracted medical terms.

I used this dataset to train and evaluate the model's ability to classify cases into appropriate medical specialties.

---

## Methodology

### Input Structure
The tool uses three types of input:
1. **Description**
2. **Transcription**
3. **Keywords**

These inputs are combined into structured prompts for the AI model.

### Output
The output is a single word indicating the predicted medical specialty.

---

## Evaluation Methods

### 1. **Simple Prompting**
- **Description**: The AI predicts the specialty based on unconstrained text input.
- **Accuracy**: 32.8%
- **Strengths**: Straightforward approach.
- **Weaknesses**: Low accuracy due to ambiguous outputs and overlapping specialties.

### 2. **Constrained Prediction**
- **Description**: The AI selects a specialty from a predefined list.
- **Accuracy**: 51.6%
- **Strengths**: Improved relevance and consistency.
- **Weaknesses**: Predefined categories may miss nuanced specialties.

### 3. **Vector Embeddings & Cosine Similarity**
- **Description**: Converts specialties into vector embeddings and measures prediction quality using cosine similarity.
- **Accuracy**: 94%
- **Strengths**: Handles semantic relationships effectively and is scalable.

---

## Results

| Evaluation Method      | Accuracy (%) |
|-------------------------|--------------|
| Simple Prompting        | 32.8         |
| Constrained Prediction  | 51.6         |
| Vector Embeddings       | 94.0         |

### Insights
- Fine-tuning the similarity threshold can improve evaluation metrics.
- Future improvements could involve incorporating rules for partial matches and exploring additional metrics.

---

## Code Structure

### Notebook
The main implementation is provided in the Jupyter Notebook `AI_predictor.ipynb`. It includes:
- Data preprocessing steps.
- Prompt engineering techniques.
- Model evaluation using various methods.

### Key Dependencies
- Python
- OpenAI API
- Pandas, NumPy

---
