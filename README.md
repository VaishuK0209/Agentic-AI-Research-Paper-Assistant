# 🤖 Agentic AI Research Paper Assistant

> **An intelligent multi-agent research assistant that automates the discovery, analysis, summarization, and recommendation of Machine Learning research papers using Agentic AI, Google Gemini, and FAISS-powered semantic search.**

![Python](https://img.shields.io/badge/Python-3.10+-blue?style=for-the-badge&logo=python)
![Streamlit](https://img.shields.io/badge/Streamlit-Web%20App-red?style=for-the-badge&logo=streamlit)
![Google Gemini](https://img.shields.io/badge/Google-Gemini%202.5%20Flash-blue?style=for-the-badge&logo=google)
![FAISS](https://img.shields.io/badge/FAISS-Vector%20Search-green?style=for-the-badge)
![Sentence Transformers](https://img.shields.io/badge/SentenceTransformers-Embeddings-orange?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-lightgrey?style=for-the-badge)

---

# 📖 Overview

The **Agentic AI Research Paper Assistant** is an AI-powered literature review system that transforms the way researchers discover and analyze Machine Learning papers.

Unlike traditional semantic search engines that simply retrieve similar documents, this project leverages a coordinated team of specialized AI agents to understand user intent, search relevant research papers, extract key insights, generate summaries, and recommend related work.

The system utilizes:

- 🧠 **Google Gemini 2.5 Flash** for reasoning and analysis
- 🔍 **Sentence Transformers** for semantic embeddings
- ⚡ **FAISS** for high-speed vector similarity search
- 📚 **ArXiv Machine Learning Dataset**
- 🎯 **Streamlit** for an interactive user experience

The architecture demonstrates how **Agentic AI** can automate literature review workflows that traditionally require significant manual effort.

---

# ✨ Key Features

### 🤖 Multi-Agent AI Architecture
A team of specialized AI agents collaborates to solve complex research queries.

- Planner Agent
- Search Agent
- Analysis Agent
- Summary Agent
- Recommendation Agent

---

### 🔍 Semantic Research Paper Search

Instead of keyword matching, the system performs semantic retrieval using vector embeddings to understand the meaning behind the user's query.

---

### 📑 Automated Paper Analysis

For every retrieved paper, the system automatically extracts:

- Paper Title
- Authors
- Research Keywords
- Main Contribution
- Research Domain

---

### 📝 AI-Powered Summarization

Generate concise, easy-to-read summaries of research papers using Google Gemini.

If the Gemini API is unavailable, the system automatically falls back to local transformer models.

---

### 💡 Intelligent Paper Recommendations

Discover similar research papers based on semantic similarity and extracted topics.

---

### ⚙️ Hybrid Execution Mode

Supports two execution modes:

- Google Gemini (Cloud LLM)
- Local AI Models (Offline Fallback)

This makes the project usable even without an API key.

---

### 📊 Interactive Streamlit Dashboard

Visualizes every stage of the agent pipeline in real time, allowing users to observe how each AI agent contributes to solving the research task.

---

# 🚀 Problem Statement

Researchers spend significant time:

- Searching papers using multiple keyword combinations
- Reading numerous abstracts
- Extracting important contributions manually
- Finding related work through separate searches
- Organizing literature review notes

Traditional search engines retrieve documents but do not automate the research workflow.

---

# 💡 Solution

The **Agentic AI Research Paper Assistant** automates the complete research discovery pipeline using multiple collaborative AI agents.

The system:

- Understands the user's intent
- Plans an optimized search strategy
- Retrieves semantically relevant papers
- Extracts structured research information
- Generates readable summaries
- Suggests related papers

This significantly reduces the time required for literature reviews.

---

# 🧠 Agent Workflow

```
User Query
      │
      ▼
┌────────────────────┐
│ Planner Agent      │
│ • Understand Query │
│ • Generate Strategy│
└─────────┬──────────┘
          │
          ▼
┌────────────────────┐
│ Search Agent       │
│ • FAISS Retrieval  │
│ • Merge Results    │
└─────────┬──────────┘
          │
          ▼
┌────────────────────┐
│ Analysis Agent     │
│ • Authors          │
│ • Keywords         │
│ • Contributions    │
└─────────┬──────────┘
          │
          ▼
┌────────────────────┐
│ Summary Agent      │
│ • Paper Summary    │
└─────────┬──────────┘
          │
          ▼
┌────────────────────┐
│ Recommendation     │
│ • Similar Papers   │
└────────────────────┘
```

---

# 🏗️ Project Architecture

```
User Query
      │
      ▼
Planner Agent
      │
      ▼
Search Agent
      │
      ▼
FAISS Vector Database
      │
      ▼
Relevant Papers
      │
      ▼
Analysis Agent
      │
      ▼
Summary Agent
      │
      ▼
Recommendation Agent
      │
      ▼
Streamlit Dashboard
```

---

# 📂 Project Structure

```
Agentic-AI-Research-Paper-Assistant/
│
├── README.md
├── requirements.txt
├── .gitignore
├── .env
│
├── data/
│   ├── README.md
│   ├── cleaned_arxiv_papers.csv
│   ├── arxiv_embeddings.npy
│   └── paper_faiss.index
│
├── notebooks/
│   ├── 01_EDA_and_Embeddings.ipynb
│   └── 02_Search_Engine.ipynb
│
└── src/
    ├── app.py
    ├── build_index.py
    ├── data_prep.py
    ├── search_engine.py
    │
    └── agents/
        ├── planner_agent.py
        ├── search_agent.py
        ├── analysis_agent.py
        ├── summary_agent.py
        └── recommendation_agent.py
```

---

# ⚙️ Installation

## 1️⃣ Clone the Repository

```bash
git clone https://github.com/yourusername/Agentic-AI-Research-Paper-Assistant.git

cd Agentic-AI-Research-Paper-Assistant
```

---

## 2️⃣ Create Virtual Environment

```bash
python -m venv venv
```

### Windows

```bash
venv\Scripts\activate
```

### Linux / macOS

```bash
source venv/bin/activate
```

---

## 3️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

Install SpaCy model

```bash
python -m spacy download en_core_web_sm
```

---

## 4️⃣ Configure Environment Variables

Create a `.env` file in the root directory.

```env
GEMINI_API_KEY=your_google_gemini_api_key
```

---

## 5️⃣ Prepare Dataset

Generate embeddings and build the FAISS index.

```bash
python src/data_prep.py

python src/build_index.py
```

---

# ▶️ Run the Application

```bash
streamlit run src/app.py
```

Open:

```
http://localhost:8501
```

---

# 🛠️ Technology Stack

| Category | Technology |
|-----------|------------|
| Programming Language | Python |
| LLM | Google Gemini 2.5 Flash |
| Embedding Model | all-MiniLM-L6-v2 |
| Vector Database | FAISS |
| Framework | Streamlit |
| NLP | SpaCy |
| Local Summarization | DistilBART |
| Keyword Extraction | KeyBERT |
| Environment | python-dotenv |

---

# 📊 Dataset

The project uses Machine Learning research papers from the **ArXiv** dataset.

Dataset contains:

- Research Paper Abstracts
- Titles
- Authors
- Categories
- Metadata

For faster development, the preprocessing script loads a subset of the dataset (default: 1,000 papers). This limit can be adjusted in `src/data_prep.py` for larger-scale experimentation.

---

# 🎯 Example Workflow

### User Query

> *"Recent transformer architectures for medical image segmentation."*

### Planner Agent

- Understands user intent
- Creates multiple semantic search queries

↓

### Search Agent

- Retrieves relevant papers using FAISS

↓

### Analysis Agent

Extracts:

- Authors
- Keywords
- Contributions
- Research Area

↓

### Summary Agent

Generates an easy-to-read research summary.

↓

### Recommendation Agent

Suggests related papers for deeper exploration.

---

# 🌟 Future Enhancements

- 📄 Full PDF analysis instead of abstracts
- 🔗 Citation graph exploration
- 🌐 Multi-database support (Semantic Scholar, IEEE Xplore, ACM, PubMed)
- 🧠 Memory-enabled AI agents
- 📈 Research trend visualization
- 🤝 Multi-agent collaboration using LangGraph/CrewAI
- ☁️ Cloud deployment with Docker and Kubernetes
- 🎙️ Voice-enabled research assistant
- 📊 Interactive knowledge graphs

---

# 🤝 Contributing

Contributions are welcome!

1. Fork the repository
2. Create a new feature branch

```bash
git checkout -b feature-name
```

3. Commit your changes

```bash
git commit -m "Add new feature"
```

4. Push to your branch

```bash
git push origin feature-name
```

5. Open a Pull Request

---

# 📜 License

This project is licensed under the **MIT License**.

---

# 👩‍💻 Author

**Vaishnavi Kushwah**

B.Tech Computer Science Engineering

AI • Machine Learning • Agentic AI • Research Systems • Full Stack Development

---

## ⭐ If you found this project helpful, consider giving it a Star on GitHub!
