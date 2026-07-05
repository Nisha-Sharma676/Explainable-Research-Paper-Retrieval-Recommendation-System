# Explainable Research Paper Retrieval and Recommendation System
## Semantic Search • Summarization • Keyword Extraction • Explainable AI • Difficulty Analysis

## Project Overview
This project is an AI-powered research paper analysis system designed to help users discover, understand, and analyze academic papers more effectively. It retrieves research papers based on semantic similarity and enhances results using explanations, keyword extraction, and difficulty prediction.

The system integrates Natural Language Processing (NLP), Transformer-based embeddings, and vector search techniques to create an intelligent research paper recommendation engine.


## Problem Statement
TThe number of research papers published across different domains is increasing rapidly, making it difficult for students and researchers to find relevant and understandable content.

Traditional keyword-based search systems fail to capture semantic meaning, resulting in irrelevant results and poor user experience.

Key challenges:
- Irrelevant keyword-based search results
- No explanation for recommendations
- No difficulty understanding of papers
- Time-consuming manual filtering


## Objectives

The primary objectives of this project are:

- To retrieve research papers using semantic similarity instead of keyword matching  
- To enhance search accuracy using transformer-based embeddings  
- To provide explainable AI-based recommendations  
- To extract meaningful keywords and topics from research papers  
- To classify papers based on difficulty level (Beginner, Intermediate, Advanced)  
- To improve the overall research paper discovery experience for users


## Dataset

This project uses the ML-ArXiv Papers dataset available on Hugging Face.

The dataset contains research papers from different machine learning and artificial intelligence domains.

Each record includes:
- Title of the research paper  
- Abstract of the research paper  

The dataset is used to generate embeddings, perform semantic search, and extract meaningful insights from research content.

Dataset Link:
https://huggingface.co/datasets/CShorten/ML-ArXiv-Papers


## Features Implemented

### 1. Dataset Loading
- Loaded the ML-ArXiv Papers dataset from Hugging Face  
- Extracted required fields such as title and abstract for processing  

### 2. Data Preprocessing
- Selected title and abstract columns  
- Combined them into a single `paper_text` field  
- Cleaned text by removing newline characters and extra spaces  
- Prepared structured data for embedding generation
  
### 3. Embedding Generation
- Used the `all-MiniLM-L6-v2` Sentence Transformer model  
- Converted research papers into dense vector embeddings  
- Represented semantic meaning in numerical form for similarity search  

### 4. FAISS Index Creation
- Built FAISS (Facebook AI Similarity Search) index  
- Stored all embeddings in vector form  
- Enabled fast and scalable similarity search over large dataset  

### 5. Semantic Search
- Performed query-based semantic search using embeddings  
- Retrieved top-k most relevant research papers  
- Used cosine similarity for relevance scoring  

### 6. Research Paper Summarization
- Generated concise summaries of research paper abstracts  
- Helped users quickly understand long research content  
- Improved readability and information extraction  

### 7. Keyword Extraction using KeyBERT
- Extracted important keywords and phrases from abstracts  
- Generated both single-word and multi-word key phrases  
- Helped identify core topics of research papers  

### 8. Explainable Research Paper Recommendation System
- Provided explanations for each recommendation  
- Displayed similarity scores and reasoning  
- Showed why a paper is relevant to the user query  
- Improved transparency and trust in results  

### 9. Research Paper Difficulty Analyzer
- Classified research papers into:
  - Beginner  
  - Intermediate  
  - Advanced  
- Based on:
  - Sentence complexity  
  - Readability score  
  - Keyword density  
  - Abstract length  
- Helped users understand difficulty level before reading papers  


## System Workflow

The system follows a structured pipeline to process and analyze research papers efficiently:

1. Dataset Loading  
   - Load ML-ArXiv research paper dataset from Hugging Face
     
2. Data Preprocessing  
   - Clean text by removing unwanted characters  
   - Combine title and abstract into a single text field  

3. Embedding Generation  
   - Convert research papers into vector embeddings using Sentence Transformers  

4. FAISS Index Creation  
   - Store embeddings in FAISS index for fast similarity search  

5. Semantic Search  
   - Accept user query  
   - Retrieve top-k most relevant research papers based on similarity  

6. Keyword Extraction  
   - Extract important keywords from retrieved papers using KeyBERT  

7. Explainable Recommendation  
   - Generate explanation for why a paper is relevant  
   - Show similarity score and matching concepts  

8. Difficulty Analysis  
   - Classify papers into Beginner, Intermediate, and Advanced levels  
   - Based on readability and text complexity  

Final Output includes:
- Relevant research papers  
- Similarity score  
- Keywords  
- Explanation  
- Difficulty level


## Technologies Used

- Python  
- Pandas  
- NumPy  
- Sentence Transformers  
- FAISS (Facebook AI Similarity Search)  
- Transformers (Hugging Face)  
- KeyBERT  
- Scikit-learn  
- Textstat


## Project Structure
```
Explainable-Research-Paper-Retrieval-Recommendation-System
│
├── Explainable_Research_Paper_Retrieval_Recommendation_System.ipynb
├── README.md
├── requirements.txt
```
## Note
```
- This project does NOT include `paper_embeddings.npy` and `paper_faiss.index` files in the repository.  
- These files are generated dynamically when the notebook is executed.  
- FAISS index and embeddings are created during runtime to ensure lightweight repository size.
```

## Example Output

When a user enters a query, the system retrieves top relevant research papers using semantic search and explains each result.


### Input Query
```
deep learning for medical image analysis
```
## Top-K Retrieved Results (Sample from k=5)

### Paper 1
```
TITLE: A Perspective on Deep Imaging  

Similarity Score: 0.72  

KEYWORDS:
- tomographic imaging deep  
- medical imaging  
- deep learning  

EXPLANATION:
The paper is highly relevant due to strong semantic similarity with the query and shared domain concepts in medical imaging and deep learning.

DIFFICULTY LEVEL: Intermediate  
Difficulty Score: 5.8  
```
### Paper 2
```
TITLE: Classification of MRI Data using Deep Learning  

Similarity Score: 0.69  

KEYWORDS:
- MRI classification  
- deep learning models  
- medical imaging  

EXPLANATION:
The paper matches the query context and focuses on deep learning techniques applied to medical imaging data.

DIFFICULTY LEVEL: Intermediate  
Difficulty Score: 5.2  
```

## Future Scope

This project can be improved further by:

- Building a web app using Streamlit or Flask  
- Adding user personalization in recommendations  
- Supporting full research paper PDFs instead of only abstracts  
- Improving difficulty prediction with advanced models  
- Deploying the system as a cloud-based application  

  
## Conclusion

This project demonstrates an intelligent research paper retrieval and analysis system that goes beyond traditional keyword-based search.

By combining semantic search, explainable AI, keyword extraction, and difficulty analysis, the system helps users find relevant research papers and understand them more effectively.

It improves the overall research experience by making paper discovery faster, smarter, and more meaningful.


## Key Learnings

This project helped me understand how different NLP techniques can be integrated to build an end-to-end intelligent system. Through this project, I gained practical experience in:

- Sentence Embeddings  
- Semantic Search  
- Vector Databases using FAISS  
- Transformer-based Summarization  
- Keyword Extraction  
- Explainable AI for recommendations  
- Difficulty level prediction of research papers  
- Building complete NLP pipelines

 
## Author

Nisha Sharma
B.Tech Computer Science Engineering  
Interested in Machine Learning, Artificial Intelligence, and Data Analytics  

## Acknowledgement

This project, Explainable Research Paper Retrieval and Recommendation System, was developed as part of my academic learning in Natural Language Processing and Machine Learning.
It helped me gain practical understanding of semantic search, transformer-based embeddings, vector search using FAISS, and explainable AI techniques.
The project also strengthened my knowledge of building end-to-end AI systems for real-world information retrieval problems.
