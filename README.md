# 🚨 Sentinel: AI Disaster Response Coordinator


### **A Multi-Agent System for Real-Time Crisis Management**


Sentinel is a **five-agent, collaborative system** designed to drastically accelerate decision-making and resource deployment during catastrophic events.

---

> ### **The Core Mission: Eliminating the Fog of War**
> **Sentinel** is an **Autonomous Multi-Agent System** that acts as an AI Crisis Commander. By leveraging **Gemini's Multimodal Intelligence** and **Conditional Logic**, it transforms chaotic, unstructured input into an **actionable, safety-optimized Incident Command Report (ICR)**. Its core safety feature is **Conditional Rerouting** based on real-time visual assessment.

### 🌍 The Problem: The Golden Hour Challenge

In a disaster, every minute counts, but centralized human command centers face significant delays due to data chaos, slow visual assessment, and resource mismatches.

### 💡 The Solution: Actionable, Optimized Orders

**Sentinel's Promise:** To drastically reduce response time and save lives by automating the synthesis of chaotic, multimodal data into **actionable, life-saving rescue orders.**

-----

## 🚀 Key Features (Agent Design Kit Principles)

* **Multimodal Triage:** Processes raw field data (text, images) using specialized agents, integrating **Gemini Vision** for rapid assessment of hazards (e.g., road blockages).
* **Long-Term Memory (RAG):** Integrates **FAISS vector search** with **Sentence Transformers** to retrieve local operational unit data (equipment, personnel) for optimized logistics planning.
* **Conditional Orchestration:** The **CommanderAgent** applies critical safety rules, executing an automatic **REROUTE** based on visual confirmation of impassable roads.
* **Autonomous Evaluation (LLM-as-a-Judge):** Includes a dedicated **EvaluatorAgent** to perform a critical self-assessment of the final report for safety and efficiency, closing the **Feedback Loop**.
* **Structured Output:** Generates a formal, verifiable JSON file containing the final safety-vetted deployment directive.

-----

## 🧠 Architectural Design

Sentinel employs a sequential, specialized workflow to ensure high reliability and clear separation of concerns, adhering to the principles of the **Agent Design Kit (ADK)**.

### **Agent Constellation**

| Agent Name | Role | Core Function | Inputs |
| :--- | :--- | :--- | :--- |
| **1. SignalAgent** | Triage & Classification | Analyzes raw text input and extracts key entities (location, needs, severity) into JSON. | Raw Text |
| **2. VisionAgent** | Visual Assessment | Analyzes input images to confirm infrastructure damage and accessibility status. | Image, Triage Data |
| **3. LogisticsAgent** | RAG-Optimized Allocation | Queries a vector store (FAISS) to match complex needs to the optimal unit capability. | Triage Data, Vision Summary |
| **4. CommanderAgent** | Strategic Orchestration | Synthesizes data and applies **Conditional Logic** to override ground units with air support if hazards are confirmed. | All Agent Outputs |
| **5. EvaluatorAgent** | Autonomous Evaluation | Critically reviews the final report for safety and efficiency (LLM-as-a-Judge). | Original Input, Final ICR |

### **Architecture Diagram**

A visual representation of the agent workflow and data pipeline.

<img width="1024" height="1024" alt="sentinel_architecture" src="https://github.com/user-attachments/assets/5077820f-2927-4914-b8b4-f77637751611" />

-----

## ⚙️ Getting Started

These instructions will get you a copy of the project up and running on your local machine or in a Kaggle environment for development and testing.

### **Prerequisites**

You will need the following installed:

* Python 3.10+
* A valid **Google Gemini API Key** (from Google AI Studio)
* The key must be set as an environment variable named `GOOGLE_API_KEY`.

### **Installation**

1.  **Clone the repository:**

    ```bash
    git clone [https://github.com/theshikhardwivedi/Sentinel-AI-Disaster-Response-Coordinator.git](https://github.com/theshikhardwivedi/Sentinel-AI-Disaster-Response-Coordinator.git)
    cd sentinel-ai-disaster-response-coordinator
    ```

2.  **Install dependencies:**
    The project relies on `google-genai` for the LLM, `sentence-transformers` for embeddings, and `faiss-cpu` for vector search.

    ```bash
    pip install -r requirements.txt
    ```

    *(Note: Ensure your `requirements.txt` file includes all necessary libraries: `google-genai`, `pandas`, `numpy`, `sentence-transformers`, `faiss-cpu`, etc.)*

### **Usage**

The entire system is executed through the main Jupyter Notebook.

1.  **Setup Environment:** Ensure your `GOOGLE_API_KEY` is set.
2.  **Open Notebook:** Open `/notebook/sentinel-ai-disaster-response-coordinator.ipynb`.
3.  **Run Cells Sequentially:** Execute the cells from top to bottom. The notebook demonstrates the full flow, from data ingestion to the final generated **Incident Command Report**.

-----

## 🤝 Contributing

Contributions are what make the open-source community an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

1.  Fork the Project
2.  Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3.  Commit your Changes (`git commit -m 'feat: Add AmazingFeature'`)
4.  Push to the Branch (`git push origin feature/AmazingFeature`)
5.  Open a Pull Request

-----

## 👤 Author

**Shikhar Dwivedi**

* Kaggle: [@theshikhardwivedi](https://www.kaggle.com/code/theshikhardwivedi/sentinel-ai-disaster-response-coordinator)
* GitHub: [@theshikhardwivedi](https://github.com/theshikhardwivedi/Sentinel-AI-Disaster-Response-Coordinator.git)
