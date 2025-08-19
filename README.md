🔍 Search Engine with NVIDIA LLMs (RAG-based)

This project demonstrates a Retrieval-Augmented Generation (RAG) pipeline built with Streamlit, LangChain, FAISS, and NVIDIA AI Endpoints.
It allows you to upload and embed PDF documents, then query them using NVIDIA Embeddings and Llama 3.3-70B Instruct for accurate question answering.

🚀 Features

Document Ingestion: Automatically loads PDFs from ./us_census/.

Text Chunking: Splits documents into smaller chunks for efficient retrieval.

Vector Store: Uses FAISS for semantic similarity search.

Embeddings: Powered by nvidia/nv-embedqa-e5-v5.

LLM Querying: Uses meta/llama-3.3-70b-instruct from NVIDIA AI endpoints.

Interactive UI: Built with Streamlit for easy querying and results display.

Response Time Tracking: Shows latency for each query.

Document Context Viewer: Lets you expand and view the document excerpts used to generate answers.

📂 Project Structure
search-engine-llm/
│── streamlit_app.py      # Main Streamlit app
│── us_census/            # Directory containing PDF documents (user-provided)
│── requirements.txt      # Dependencies (recommended)
│── README.md             # Project documentation

⚙️ Setup Instructions
1️⃣ Clone the Repository
git clone https://github.com/rohanjain1648/search-engine-llm.git
cd search-engine-llm

2️⃣ Install Dependencies
pip install -r requirements.txt


(If you don’t have a requirements.txt, install manually:)

pip install streamlit langchain langchain-nvidia-ai-endpoints langchain-community faiss-cpu

3️⃣ Get NVIDIA API Key

Sign up at NVIDIA Build
.

Copy your API Key.

Set it up either via environment variable:

export NVIDIA_API_KEY="your-key-here"


Or inside Streamlit Cloud Secrets:

NVIDIA_API_KEY = "your-key-here"

4️⃣ Add Documents

Place your PDF files inside:

./us_census/

5️⃣ Run the App
streamlit run streamlit_app.py

🖥️ Usage

Click "Create Document Embeddings" to build the FAISS vector store.

Enter your question in the input box.

Get answers powered by RAG with NVIDIA LLMs.

Expand "View relevant document excerpts" to inspect the context used.

🧰 Tech Stack

Frontend: Streamlit

LLM: NVIDIA NIM - meta/llama-3.3-70b-instruct

Embeddings: NVIDIA - nv-embedqa-e5-v5

Vector DB: FAISS

Framework: LangChain

📌 Example

⚠️ Requirements

Valid NVIDIA API Key

PDF files in ./us_census/

Stable internet connection for API calls

📜 License

MIT License. Free to use and modify.
