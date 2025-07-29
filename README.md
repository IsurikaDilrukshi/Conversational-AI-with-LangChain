 ## 💬 Skincare RAG Chatbot using LangChain & HuggingFace

This project is a **Retrieval-Augmented Generation (RAG) chatbot** built using **LangChain**, **HuggingFace Transformers**, and **Gradio UI**. It can answer questions about a skincare company and its products by retrieving information from a company profile PDF and a structured CSV dataset.

 ### 🚀 Features
-  Hybrid search using **vector similarity (Chroma)** + **keyword search (BM25)**
- Conversational memory using LangChain's `ConversationBufferMemory`
- Document parsing from PDF and CSV
- Local inference using HuggingFace models (e.g., Falcon-7B)
- Gradio-based chatbot interface

### 🧠 Models Used
- **LLM:** tiiuae/falcon-7b-instruct (4-bit quantized)
- **Embeddings:** sentence-transformers/all-mpnet-base-v2

📚 Data Sources
- lustraderm_company_profile.pdf — **Company background**
- skincare_products_synthetic_50.csv — **Product listings**

### 💡 How It Works

- Load & Split PDF and CSV data into chunks  
- Embed chunks using Sentence Transformers  
- Store in Chroma vector DB and enable hybrid retriever  
- Prompt is dynamically generated using chat history and retrieved documents  
- Generate answers via HuggingFace pipeline with quantized LLM  
- Interact via command-line or Gradio web UI  

