# 🔗 Smart URL Answer Bot

A Retrieval-Augmented Generation (RAG) application built with **Streamlit**, **LangChain**, **ChromaDB**, **Groq LLM**, and **Hugging Face Embeddings**. This application allows users to provide URLs, automatically extract and index their content, and ask questions based on the information contained in those web pages.

---

## 🚀 Features

* 📥 Process multiple URLs from the web
* 🌐 Extract webpage content automatically
* ✂️ Split content into manageable chunks
* 🧠 Generate embeddings using Hugging Face models
* 🗄️ Store embeddings in Chroma Vector Database
* 🤖 Query indexed content using Groq's Llama 3.3 model
* 📚 Display answer sources for transparency
* 🎨 Simple and interactive Streamlit UI

---

## 🏗️ Project Structure

```text
rag_app/
│
├── main.py                  # Streamlit frontend
├── rag.py                   # RAG pipeline logic
├── .env                     # API keys
├── requirements.txt         # Dependencies
│
└── resources/
    └── vector_store/        # Chroma vector database
```

---

## ⚙️ Technologies Used

* Streamlit
* LangChain
* ChromaDB
* Groq LLM
* Hugging Face Embeddings
* Unstructured URL Loader
* Python

---

## 📋 Prerequisites

Before running the project, make sure you have:

* Python 3.10+
* Groq API Key
* Hugging Face Access Token

---

## 🔑 Environment Variables

Create a `.env` file in the root directory and add:

```env
GROQ_API_KEY=your_groq_api_key
HUGGINGFACEHUB_API_TOKEN=your_huggingface_token
```

---

## 📦 Installation

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/smart-url-answer-bot.git

cd smart-url-answer-bot
```

### 2. Create Virtual Environment

```bash
python -m venv venv
```

Activate the environment:

**Windows**

```bash
venv\Scripts\activate
```

**Mac/Linux**

```bash
source venv/bin/activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

---

## ▶️ Run the Application

Start the Streamlit application:

```bash
streamlit run main.py
```

The application will open in your browser.

---

## 📝 How It Works

### Step 1: Enter URLs

Provide up to three webpage URLs in the sidebar.

### Step 2: Process URLs

Click the **Process URLs** button.

The system will:

1. Load webpage content.
2. Split text into chunks.
3. Generate embeddings.
4. Store embeddings in ChromaDB.

### Step 3: Ask Questions

Enter a question related to the processed content.

Example:

```text
What are the key points discussed in the article?
```

The system retrieves relevant chunks from the vector database and generates an answer using the LLM.

---

## 🔄 Workflow

```text
URLs
  ↓
Web Scraping
  ↓
Text Chunking
  ↓
Embedding Generation
  ↓
Chroma Vector Store
  ↓
Retriever
  ↓
Groq LLM
  ↓
Answer + Sources
```

---

## 📸 User Interface

### Sidebar

* URL 1 Input
* URL 2 Input
* URL 3 Input
* Process URLs Button

### Main Section

* Question Input Box
* Generated Answer
* Source References

---

## 🧠 Embedding Model

```python
Alibaba-NLP/gte-base-en-v1.5
```

Used for converting text chunks into vector representations.

---

## 🤖 LLM Used

```python
llama-3.3-70b-versatile
```

Provided through Groq for fast inference and high-quality responses.

---

## 📚 Example Usage

### URLs

```text
https://example.com/article1
https://example.com/article2
```

### Question

```text
What are the major findings mentioned in the articles?
```

### Output

```text
The articles discuss...
```

### Sources

```text
https://example.com/article1
https://example.com/article2
```

---

## ⚠️ Limitations

* URLs must contain readable textual content.
* Large websites may take longer to process.
* The vector database is reset whenever new URLs are processed.
* Answers are limited to the information available in the processed URLs.

---

## 🔮 Future Improvements

* Support for PDF documents
* Chat history memory
* Multiple vector store collections
* URL validation
* Source highlighting
* Conversation-based Q&A
* Batch URL uploads

---

## 👨‍💻 Author

Developed using:

* LangChain
* Streamlit
* ChromaDB
* Groq
* Hugging Face

---

## 📄 License

This project is licensed under the MIT License.
