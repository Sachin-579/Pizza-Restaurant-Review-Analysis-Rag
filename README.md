# Pizza-Restaurant-Review-Analysis-Rag
A Retrieval-Augmented Generation (RAG) system for Pizza Restaurant Review Analysis using Ollama and ChromaDB. Combines local LLM inference with mxbai-embed-large embeddings to analyze, summarize, and answer customer feedback — completely offline and privacy-friendly. 🍕🤖
🍕 Pizza Restaurant Review Analysis using RAG and Ollama
📖 Overview

This project implements a Retrieval-Augmented Generation (RAG) pipeline for analyzing and summarizing restaurant reviews, specifically focused on a pizza restaurant 🍕.
It combines Ollama’s local LLM inference with semantic search embeddings (mxbai-embed-large) to provide meaningful insights about customer experiences — completely offline and privacy-friendly.

🚀 Features

✅ Local LLM inference via Ollama

🧠 Text embeddings using mxbai-embed-large

🔍 Vector-based retrieval using ChromaDB

💬 Context-aware Q&A over restaurant reviews

📊 Includes a realistic restaurant review dataset

🔒 100% offline — no API keys or cloud dependency

🧠 System Architecture

RAG Pipeline Flow:

Document Ingestion – Reads and cleans restaurant review data

Embedding Generation – Encodes text using mxbai-embed-large

Vector Storage & Retrieval – Stores embeddings in ChromaDB for semantic similarity search

LLM Response Generation – Uses Ollama (e.g., llama3, mistral) to generate contextual answers

📁 pizza-restaurant-review-analysis/
│
├── 📄 main.py                     # Main entry point for the RAG pipeline
├── 📄 vector.py                   # Handles embedding and vector storage (mxbai-embed-large)
├── 📁 realistic_restaurant_reviews/  # Folder containing sample restaurant review data
├── 📁 chrome_langchain_db/        # ChromaDB vector database
│   ├── chroma.sqlite3
│   └── 8b8d4954a... (vector data)
├── 📄 requirements.txt            # Python dependencies
├── 📁 venv/                       # Virtual environment
└── ⚙️ pyvenv.cfg

🧩 Installation
1️⃣ Clone the Repository
git clone https://github.com/yourusername/pizza-restaurant-review-analysis.git
cd pizza-restaurant-review-analysis

2️⃣ Create and Activate Virtual Environment
python -m venv venv
# Windows
venv\Scripts\activate
# macOS/Linux
source venv/bin/activate

3️⃣ Install Dependencies
pip install -r requirements.txt

4️⃣ Install and Run Ollama

Download Ollama from 👉 https://ollama.ai

Start the Ollama service:

ollama serve


Pull the required models:

ollama pull llama3
ollama pull mxbai-embed-large

▶️ Running the Application

To start the RAG system:

python main.py


You’ll be prompted to enter a question, for example:

“What do customers say about pizza quality?”

The system will:

Retrieve the most relevant reviews using mxbai-embed-large

Generate a natural-language summary using Ollama

💬 Example Usage
🧠 Input:
Enter your query: What do customers think about pizza delivery service?

⚙️ Internal Steps:

Retrieves similar reviews from ChromaDB

Uses mxbai-embed-large embeddings to find related text chunks

Sends context + question to the Ollama LLM (llama3)

💡 Output:
Most customers appreciated the quick and warm delivery of pizzas. 
Several reviews mentioned that orders arrived within 25–30 minutes, 
while a few noted slight delays during weekends. 
Overall, the delivery service is rated highly for reliability and speed.

🧰 Requirements

Python 3.10+

Ollama installed locally

Models:

llama3 (or any local LLM supported by Ollama)

mxbai-embed-large (embedding model)

Dependencies listed in requirements.txt

📈 Future Enhancements

📊 Add Streamlit dashboard for visual insights

🤖 Integrate sentiment classification per review

🍽️ Extend to multiple restaurant datasets

🐳 Add Docker support for deployment
