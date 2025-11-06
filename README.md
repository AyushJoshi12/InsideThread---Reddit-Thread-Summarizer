# Inside Thread: Reddit Summarization Platform

## Overview
**Inside Thread** is an intelligent Reddit summarization platform that condenses long discussion threads into **concise, context-aware summaries** using advanced Natural Language Processing (NLP) and transfer learning techniques.

The platform is designed to help users quickly digest discussions from Reddit while preserving the **emotional tone, key topics, and context** of the conversation.

---

## Dataset
- **Source:** TLDRHQ Reddit dataset  
- **Records:** ~52,000 Reddit threads  
- **Preprocessing:**  
  - Regex-based cleaning  
  - Text normalization and slang standardization  
  - Sentiment analysis using VADER  
  - Topic modeling using LDA (10 major discussion clusters)  

**Semantic Enrichment:**  
- Integrated document-topic distributions  
- Calculated cosine similarity between source threads and generated summaries

---

## Data Preprocessing & Feature Engineering
- **Cleaning & Normalization:** PySpark on Databricks for scalable processing  
- **Sentiment Analysis:** VADER to capture emotional tone of threads  
- **Topic Modeling:** LDA to identify dominant discussion themes  
- **Semantic Alignment:** Cosine similarity between thread content and generated summaries  

---

## Model Implementation
- **Abstractive Summarization:** Fine-tuned **BART** model  
  - Freezed selective encoder-decoder layers to **improve training efficiency by ~28%**  
- **Performance Metrics:**  
  - ROUGE-1: 0.79  
  - ROUGE-2: 0.66  
  - ROUGE-L: 0.72  
  - BLEU: 0.68  
  - BERTScore F1: 0.74  

> Metrics validate that the generated summaries are **high-quality and contextually accurate**.

<img width="1916" height="777" alt="image" src="https://github.com/user-attachments/assets/990b577d-e290-46ae-bb88-f9d0b82d48b0" />


## User Interface
- **Interactive Streamlit app:** “Inside Thread”  
- Features:  
  - Input Reddit threads for summarization  
  - Generate context-aware summaries  
  - Extract **RAKE-based hashtags**  
  - Directly share summaries on Twitter with automated text insertion  

**Example UI Screenshot:**  
<img width="1920" height="1812" alt="image" src="https://github.com/user-attachments/assets/7b000e93-b73d-4da2-b514-27f0f3a39231" />


---

## Tech Stack
- **Python Libraries:** PySpark, Transformers (HuggingFace), NLTK, VADER, Gensim, Scikit-learn, Streamlit  
- **Tools & Platforms:** Databricks, HuggingFace Transformers, Twitter API  
- **Visualization:** Matplotlib, Seaborn  
