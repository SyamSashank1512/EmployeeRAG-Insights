# 🧠 RAG Model for Employee Information Retrieval using NVIDIA LLMs

This project implements a Retrieval-Augmented Generation (RAG) system that allows users to ask **natural language questions** about employee data. The system uses **NVIDIA Large Language Models (LLMs)** to interpret user queries, generate appropriate **SQLite queries**, execute them on a structured employee database, and return meaningful answers.

---

## 📌 Features

- ✨ Natural Language Understanding using NVIDIA LLMs
- 🛢️ SQLite database backend for storing employee data
- 🤖 Auto-generated SQL queries based on user input
- 🔄 Loop of query > execution > answer generation
- 🧪 Supports questions like:
  - "How many full-time female staff were employed in 2021?"
  - "List all academic staff from the UK in 2020."
  - "Give me the total number of part-time staff in 2019."

---

## ⚙️ How It Works

1. **User Input**  
   A user asks a question in plain English (e.g., "Show me all full-time employees from India").

2. **Prompt to LLM**  
   The input and schema are sent to the NVIDIA LLM using LangChain.

3. **SQL Query Generation**  
   The LLM returns an appropriate SQL query.

4. **Query Execution**  
   The query is run on a local SQLite database (`employment_data.db`).

5. **Answer Generation**  
   The result is fed back to the LLM, which transforms it into a human-readable response.

6. **Final Output**  
   The system prints the interpreted answer for the user.

---

## 📁 Project Structure

```bash
rag-employee-info/
├── employment_data.db        # SQLite database file
├── main.py                   # Entry point for the app
├── llm_interface.py          # Handles interaction with LLM
├── sql_runner.py             # Executes SQL queries
├── schema.json               # Schema info passed to LLM
└── README.md                 # This file



