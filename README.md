# Seave - AI-Powered Resume Screening System 

![Seave](https://img.shields.io/badge/AI--powered-Resume%20Screening-blue.svg) ![FastAPI](https://img.shields.io/badge/Backend-FastAPI-green) ![MongoDB](https://img.shields.io/badge/Database-MongoDB-red) ![Pinecone](https://img.shields.io/badge/Vector%20DB-Pinecone-yellow) ![Docker](https://img.shields.io/badge/Deployment-Docker-blue)

## 🚀 Overview
Seave is an **AI-powered Resume Screening System** that enhances candidate selection through **LLMs, Named Entity Recognition (NER), semantic search, and GPT-based scoring**. It mitigates inefficiencies, biases, and limitations of traditional resume screening methods by providing **automated parsing, ranking, and insightful candidate reports**.

## ✨ Key Features
✅ **Automated Resume Parsing** - Extracts structured data (skills, education, experience) using **NER and GPT**

✅ **Candidate Ranking & Matching** - Computes similarity scores using **vector embeddings and GPT-based scoring**

✅ **Bias Mitigation** - Uses **Candidate ID and Job ID** to eliminate personal identifiers 

✅ **HR Dashboard** - Intuitive web interface for uploading resumes, reviewing rankings, and generating reports

✅ **Scalable & Fast** - Containerized backend deployed on **Google Cloud Run** with vector search in **Pinecone**

## 🏗️ System Architecture
```
Frontend (React + Tailwind) ───> Backend (FastAPI)
                                      │
       ┌──────────────────────┬──────────────────┐
       │  Resume Parsing      │  Candidate Match │
       │ (spaCy NER + GPT)    │  (Embedding + GPT Scoring) │
       └──────────────────────┴──────────────────┘
                        │
            Vector DB (Pinecone) & Metadata DB (MongoDB)
```

## 🛠️ Technologies Used
| Component  | Technologies |
|------------|-------------|
| **Frontend** | React, Tailwind CSS, Vite |
| **Backend** | FastAPI, LangChain, Langraph |
| **NER Model** | Custom spaCy model (BERT-based) deployed on AWS SageMaker |
| **Embeddings** | OpenAI `text-embedding-3-small` |
| **Database** | MongoDB (via Beanie ORM) |
| **Vector Storage** | Pinecone for similarity search |
| **Deployment** | Google Cloud Run, Docker |

## 🔧 Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/seave.git
   cd seave
   ```
2. Set up the backend:
   ```bash
   cd backend
   pip install -r requirements.txt
   uvicorn main:app --reload
   ```
3. Start the frontend:
   ```bash
   cd frontend
   npm install
   npm run dev
   ```

## 📌 Usage
1. **Upload Resumes & Job Descriptions**: Use the HR dashboard to submit candidate resumes.
2. **Automated Parsing**: Backend extracts key resume details using **NER and GPT-powered function calling**.
3. **Candidate Matching**: The system ranks candidates using **semantic similarity & GPT-based scoring**.
4. **Review Candidates**: Hiring managers can evaluate ranked candidates and download detailed reports.

## 🚀 Future Enhancements
🔹 **Expand Bias Evaluation Metrics**: Implement advanced techniques to detect and reduce bias in AI evaluations.
🔹 **Multi-Language Support**: Enable resume parsing for multiple languages.
🔹 **Real-World ATS Integration**: Connect with existing recruitment systems to streamline hiring workflows.

## 🤝 Contributing
Pull requests are welcome! If you’d like to contribute:
1. Fork the repository
2. Create a new feature branch
3. Submit a PR with detailed explanations

## 📜 License
Seave is licensed under the MIT License.

## 📩 Contact
For any inquiries, reach out to **your.email@example.com** or open an issue in this repository. 🚀
