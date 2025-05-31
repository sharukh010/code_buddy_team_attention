# 🔍 Code Buddy: An AI-Powered Documentation Query Assistant

## Overview

**Code Buddy** is an AI-driven assistant designed to answer technical questions using the latest documentation from various technologies. It leverages **RAG (Retrieval-Augmented Generation)** architecture combined with **LangGraph**, **LangChain**, and **Pinecone** to provide accurate, up-to-date responses by retrieving relevant documents and generating informed answers in real time.

This project was built during a hackathon with no prior experience in LangGraph. Everything was self-learned through documentation on the fly—demonstrating adaptability and a strong learning curve.

---

## 🔧 Features

* **LangGraph & LangChain Integration**: Modular, agentic workflow using state graphs and tools.
* **Document Ingestion**: Retrieves and stores documentation in a vector store using Pinecone.
* **Search Augmentation**: Queries search engines (via Tavily) to fetch recent, real-time content.
* **Contextual Q\&A**: Answers user queries with context from retrieved documents.
* **Powered by Cohere LLM**: Generates coherent and accurate answers using Cohere's language models.

---

## 📦 Tech Stack

* `LangGraph` - Agentic framework for composing workflows
* `LangChain` - Framework for building LLM apps
* `Pinecone` - Vector store for semantic search
* `Tavily` - Real-time web search tool
* `Cohere` - LLM for generating answers
* `Python` - Implementation language
* `Jupyter Notebook` - Prototyping environment

---

## 🚀 How It Works

1. **Document Retrieval**:

   * Uses TavilySearchResults to fetch documentation.
   * Converts fetched pages into `Document` objects.

2. **Vector Store Indexing**:

   * Extracted documentation is embedded and indexed into Pinecone.

3. **Query Handling**:

   * User inputs a query.
   * Relevant documents are retrieved from Pinecone.
   * A prompt is dynamically generated.
   * Cohere LLM processes the prompt to generate an informed answer.

4. **Agentic Execution**:

   * LangGraph handles state transitions (START → RAG → END).
   * A tools-based conditional path determines whether to fetch or generate.

---

## 🧪 Example Use Case

> **User**: "How does LangGraph manage state transitions?"

**Code Buddy**:

* Searches recent LangGraph docs using Tavily.
* Retrieves top pages and converts them into vector embeddings.
* Queries Pinecone for the most relevant chunks.
* Constructs a prompt and generates a concise, helpful answer using Cohere.

---

## 🛠️ Setup Instructions

1. **Clone the repo**

   ```bash
   git clone https://github.com/sharukh010/code_buddy_team_attention/
   cd code_buddy_team_attention
   ```

2. **Install dependencies manually**

   ```bash
   pip install langchain langgraph pinecone-client cohere python-dotenv
   ```

3. **Set environment variables**
   Create a `.env` file:

   ```env
   COHERE_API_KEY=your_cohere_key
   PINECONE_API_KEY=your_pinecone_key
   PINECONE_ENV=your_pinecone_env
   ```

4. **Run the notebook**
   Open `code_buddy.ipynb` in Jupyter and run all cells.

---

## 📈 Future Improvements

* Deploy as a web app using Streamlit or Gradio.
* Add support for multi-document summarization.
* Integrate chat history for contextual follow-ups.
* Enable fine-tuned LLM integration.

---

## 📄 License

MIT License. Feel free to fork, contribute, and build upon!

---

Would you like me to save this as a `README.md` file in your project directory?
