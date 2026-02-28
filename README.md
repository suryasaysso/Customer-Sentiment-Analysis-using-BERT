# Sentiment Analysis and Topic Modeling with BERT
This repository contains a comprehensive NLP pipeline designed to extract actionable insights from customer reviews. By combining **BERT-based Sentiment Analysis** with **BERTopic** Modeling, the project identifies not just how customers feel, but exactly what specific product attributes or categories are driving those emotions.

## 📌 Project Overview
E-commerce businesses often struggle to process thousands of text reviews manually. This project automates the process by:

**Classifying Sentiment:** Categorizing reviews into Positive, Negative, or Neutral using Transformer models.

**Discovering Topics:** Clustering reviews into distinct themes (e.g., "Sizing/Fit," "Fabric Quality," "Shipping") using BERTopic.

**Cross-Analysis:** Correlating sentiments with specific topics to identify "pain points" (e.g., high negative sentiment related to "Zippers").

## 📊 Dataset
The project utilizes the Women's E-Commerce Clothing Reviews dataset from Kaggle. It contains 23,000+ real customer reviews.

**Source:** Kaggle - Women's E-Commerce Clothing Reviews

**Key Features Used:** Review Text, Class Name, Rating.

## 🛠️ Tech Stack
Language: **Python**

Deep Learning: **Hugging Face transformers (BERT)**

Topic Modeling: **bertopic**

Data Manipulation: **pandas, numpy**

Visualization: **matplotlib, seaborn, plotly**

## 🚀 Workflow
**1. Sentiment Inference**

Using a pre-trained distilbert-base-uncased-finetuned-sst-2-english model, we process the review text in batches to extract sentiment labels and confidence scores.

**2. BERTopic Modeling**

We leverage the power of BERT embeddings to cluster reviews. Unlike traditional LDA, BERTopic uses:

Sentence Embeddings: To understand semantic context.

UMAP: For dimensionality reduction.

HDBSCAN: For dense clustering.

**3. Sentiment-Topic Correlation**

We merge the results of the two models to create a "Sentiment per Topic" heatmap. This allows us to see, for example, if the "Dresses" category has more negative feedback regarding "Length" compared to "Blouses."
