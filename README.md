# **SLM-Book-QA: Small Language Model for Book-Based Question Answering**

## 📌 **Project Overview**
This repository contains a **Small Language Model (SLM)-based Question Answering (QA) system** that processes a book as context and accurately answers user queries. The model utilizes **FAISS for efficient text retrieval**, **mpnet embeddings for semantic understanding**, and **Falcon-7B-Instruct** for response generation. This project enables users to ask questions about a given book and receive **concise, accurate, and well-structured answers**.

## 🚀 **Features**
✅ Extracts and preprocesses text from a **PDF book**
✅ Uses **FAISS** for fast and **relevant text retrieval**
✅ Embeds text using `all-mpnet-base-v2` for **semantic comprehension**
✅ Generates **concise and meaningful responses** using `Falcon-7B-Instruct`
✅ **Interactive Q&A system** with Colab Notebook support
✅ Easy to run with a **simple and intuitive interface**

## 🛠 **Installation**
### **1️⃣ Clone the Repository**
```bash
git clone //link of project//
cd SLM-Book-QA
```

### **2️⃣ Install Dependencies**
```bash
pip install -r requirements.txt
```

### **3️⃣ Run colab Notebook**
```bash
colab notebook
```

Open the notebook and run all cells to start the **interactive Q&A system**.

## 📖 **How It Works**
### **1. Text Extraction & Processing**
- The model extracts **raw text** from a given PDF book.
- The text is **cleaned and tokenized** for efficient processing.
- The text is split into **1500-word chunks** to maintain coherence.

### **2. Context Retrieval with FAISS**
- The model uses **FAISS (Facebook AI Similarity Search)** to index text embeddings.
- **SentenceTransformer's `all-mpnet-base-v2`** converts text chunks into **vector embeddings**.
- When a question is asked, the **most relevant text chunks** are retrieved from FAISS.

### **3. Answer Generation with Falcon-7B-Instruct**
- The retrieved text is passed to the **Falcon-7B-Instruct model**.
- A structured **prompt ensures precise and well-formatted answers**.
- The model generates a **concise and direct answer** based on the context.

## 💡 **Usage Example**
### **Query:**
```python
answer_question("Define While Loop")
```
### **Expected Output:**
```bash
inside a nested loop ( loop inside another loop), break will terminate the innermost loop.
```

## 📌 **Project Structure**
```bash
SLM-Book-QA/
│── data/			 
│── models/			
│── notebook.ipynb		 
│── requirements.txt		 
│── README.md		 
```

## 📈 **Evaluation & Performance**
- **Retrieval Quality:** Ensured by **FAISS indexing & debugging retrieved text**.
- **Answer Accuracy:** Model fine-tuned to generate **short & informative answers**.
- **Efficiency:** Optimized query-response time for smooth user interaction.

## 🏆 **Key Learnings & Observations**
- **FAISS indexing** significantly improves retrieval speed and relevance.
- **Chunk size (1500 words)** balances **context richness & retrieval efficiency**.
- **Falcon-7B-Instruct** generates **better structured and more natural answers** than Flan-T5.
- **Interactive Jupyter interface** makes it easy to use and test the model.

## 🤝 **Contributing**
If you’d like to improve this project:
1. **Fork the repository**
2. **Create a new branch** 
3. **Commit your changes**
4. **Push to GitHub and create a Pull Request**


🚀 **Ready to take your book-based Q&A to the next level!**

