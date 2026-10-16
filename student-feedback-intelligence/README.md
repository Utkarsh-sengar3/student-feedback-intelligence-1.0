# Student Feedback Intelligence

An end-to-end NLP/ML project that converts student feedback into actionable
sentiment and topic intelligence.

## Objective
Build an AI system that can:
- clean and validate student feedback
- classify feedback as positive, neutral, or negative
- discover recurring feedback topics
- provide course/department analytics
- analyze newly submitted feedback
- present results through an interactive dashboard

## Architecture

Student Feedback CSV
        |
        v
Data Validation & Cleaning
        |
        v
TF-IDF Feature Engineering
        |
        +--------------------+
        |                    |
        v                    v
Sentiment Classifier      K-Means
(Logistic Regression)     Topic Discovery
        |                    |
        +---------+----------+
                  v
          Intelligence Layer
                  |
                  v
        Streamlit Dashboard

## Project Structure

- `data/raw/` - original input dataset
- `data/processed/` - cleaned/enriched dataset
- `src/clean_data.py` - preprocessing
- `src/train_models.py` - model training and evaluation
- `src/predict.py` - inference
- `app/app.py` - dashboard
- `models/` - trained artifacts
- `reports/` - evaluation reports
- `run_pipeline.py` - one-command pipeline

## Run

```bash
pip install -r requirements.txt
python run_pipeline.py
streamlit run app/app.py
```

## Current Dataset

A reproducible 1,200-record starter dataset is included so the project can
run immediately. It is intentionally synthetic and should be replaced with
real/public student-feedback data for a research-grade final version.

## ML Methods

- Text cleaning
- TF-IDF (unigrams + bigrams)
- Logistic Regression sentiment classification
- K-Means topic discovery
- Accuracy / classification report
- Interactive exploratory analytics

## Next Development Phases

1. Replace/augment starter data with a validated real dataset.
2. Add aspect-based sentiment analysis.
3. Add keyword extraction and topic labels.
4. Add teacher/course-level trend analysis.
5. Add actionable recommendations.
6. Add authentication/database/API if required.
7. Add model comparison and explainability.
8. Deploy the dashboard.
