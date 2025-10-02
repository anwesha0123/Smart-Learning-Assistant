# 🤖 Smart Learning Assistant: A Multifunctional RAG Chatbot  

## 📌 Project Overview  
**Smart Learning Assistant** is a Retrieval-Augmented Generation (RAG)-based chatbot designed to help students and researchers process complex documents more efficiently.  
Users can upload research papers, textbooks, or study materials, and the system will:  
- Extract and summarize text  
- Answer questions contextually  
- Provide semantic similarity search for related content  
- Offer multilingual support  

By integrating RAG with NLP functionalities like summarization, translation and semantic search, the chatbot serves as a personalized, intelligent study companion.  

---

## 🔎 Approach  
The development pipeline follows these steps:  

1. **Document Upload & Text Extraction**  
   - Users upload PDFs, text files, or other supported documents.  
   - Text is extracted and cleaned using tools like **PyMuPDF**.  

2. **Chunking & Embedding**  
   - Documents are split into smaller text chunks using a **Text Splitter**.  
   - Each chunk is embedded using **Sentence-BERT**.  
   - Embeddings are stored in a vector database (**FAISS**).  

3. **Summarization**  
   - Summaries generated with **BART**.  
   - Summaries can be translated into multiple languages using **NLLB**.  

4. **Semantic Similarity Search**  
   - User queries retrieve the **most relevant document chunks** based on embeddings.  

5. **Question Answering with RAG**  
   - Retrieved context + user query → passed to an **LLM** (LLaMA).  
   - RAG ensures **context-aware, accurate answers**.  

6. **Chatbot Interface**  
   - Chat UI where users can:  
     - Ask questions  
     - View document summaries  
     - Switch languages  
     - Explore related documents  

---
## Flowchart
<img width="421" height="1109" align="center" alt="image" src="https://github.com/user-attachments/assets/ff5819b0-d048-4541-9fd2-d15b1486343a" />

---

## ✨ Uniqueness of the Project  
- **RAG-Enhanced Accuracy:** Combines retrieval with generation for better context-aware responses.  
- **Multilingual Support:** Summarization & Q&A in multiple languages.  
- **End-to-End Learning Tool:** Integrates summarization, semantic search, Q&A, and recommendations.  
- **Document Personalization:** Tailored for academic/research use cases (papers, notes, books).  
- **Efficient Knowledge Access:** Helps users cut through long/complex content quickly.  

---

## ⚙️ Tech Stack  
- **Programming Language:** Python  
- **NLP Models:** BART, Sentence-BERT, NLLB  
- **Libraries & Frameworks:** Hugging Face Transformers, PyMuPDF, LangChain  
- **Vector Databases:** FAISS
- **Web Interface:** Streamlit  

---

## 🏥 Applications  
- **Education:** Summarizing and questioning textbooks for students.  
- **Research:** Quickly extracting insights from lengthy research papers.  
- **Corporate Training:** Assisting employees with knowledge discovery in manuals.  
- **Healthcare & Legal:** Analyzing medical/law documents for better accessibility.  
- **Multilingual Learning:** Supporting global students with cross-language summaries.        
---

## ⚡ Installation
**1. Clone the Repository**
```
git clone https://github.com/anwesha0123/Smart-Learning-Assistant.git
cd Smart-Learning-Assistant
```

**2. Install Dependencies**
```
pip install -r requirements.txt
```

**3. Run the Chatbot**
```
streamlit run app/chatbot.py
```

