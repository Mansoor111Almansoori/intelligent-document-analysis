# Intelligent Document Analysis System (RAG-based)

An AI-powered web application that allows users to upload PDF documents and ask questions about them, with answers generated based on the document content.

The system focuses on improving how users retrieve information from long documents by using a Retrieval-Augmented Generation (RAG) pipeline.

---

## 🚀 Current Features
- Upload and process PDF documents
- Extract text from uploaded PDFs
- Ask natural language questions about documents
- AI-generated answers based on document content
- Session-based question and answer storage
- Simple single-panel Q&A interface

---

## ⚙️ System Workflow (RAG Pipeline)

1. User uploads a PDF document  
2. Text is extracted from the document  
3. Text is split into smaller chunks  
4. Each chunk is converted into embeddings (Cohere)  
5. User question is converted into embedding  
6. Relevant chunks are retrieved using vector similarity  
7. Retrieved chunks are reranked (Cohere rerank model)  
8. Top chunks are sent to LLM (Groq LLaMA 3.1)  
9. Final answer is generated based on retrieved document content  

---

## 🧠 Core Idea

The system uses **Retrieval-Augmented Generation (RAG)** where:

- The document acts as the **main source of information**
- Answers are generated using **relevant retrieved content**
- This improves accuracy compared to general AI tools

---

## 🏗️ System Architecture

The application follows the **MVC architecture**:

### 🔹 View (Frontend)
- JSP pages (Login, Upload, Q&A interface)

### 🔹 Controller
- Java Servlets handle requests and system logic

### 🔹 Model
- MySQL database (users, documents, sessions, chunks)

### 🔹 Service Layer
Handles:
- PDF processing  
- Text chunking  
- Embeddings generation  
- Retrieval and reranking  
- AI communication  

---

## 🛠 Technologies Used

### 💻 Backend
- Java (Servlets)
- JSP

### 🗄 Database
- MySQL (MAMP)

### 🤖 AI Models
- Cohere embed-v4.0 → embeddings  
- Cohere rerank-v3.5 → reranking  
- Groq LLaMA 3.1 8B → answer generation  

### ⚙️ Tools
- NetBeans IDE  
- GlassFish Server  

---

## 📊 Database Design

The system stores:
- Users  
- Documents  
- Extracted text  
- Document chunks  
- Chat sessions  
- Questions  

Each document is divided into chunks to allow efficient retrieval of relevant information.

---

## 📸 Screenshots

*(Add screenshots here later)*  
- Login Page  
- Upload Interface  
- Q&A Interface  

---

## 🚧 Current Limitations

- Answers are displayed without highlighted evidence  
- Interface is currently single-panel  
- Supports only text-based PDFs (no OCR yet)  

---

## 🔜 Future Improvements

- Two-panel interface (chat + document view)  
- Answer–evidence highlighting  
- Document summarization  
- Improved retrieval accuracy  
- UI/UX enhancements  
- Optional cloud deployment  

---

## 🎯 Project Purpose
I built this project to solve a common problem: searching through long PDF documents takes too much time.

Instead of manually reading everything, this system allows users to ask questions and get answers directly from the document using AI.

---

## 👨‍💻 About Me
I am a Computer Science student at UAEU (Expected 2026).

I enjoy building backend systems and exploring how AI can be integrated into real applications. This project is part of my senior project where I focused on implementing a working RAG pipeline using Java and cloud-based AI models.

Currently looking for internship opportunities to gain industry experience.

---
