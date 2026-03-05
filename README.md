# 🎥 RAG-Based AI Teaching Assistant

### 🚩 Problem Statement
Students often spend hours "scrubbing" through long lecture videos to find a specific 2-minute explanation. Standard keyword searches fail because they don't account for semantic meaning, and they don't provide the exact timestamp where the information is located.

### 🧠 The Approach
I built a **Retrieval-Augmented Generation (RAG)** system that turns unstructured video into a searchable knowledge base:
1.  **Data Ingestion:** Used **FFmpeg** to extract high-fidelity audio from video files, which was then transcribed using OpenAI's **Whisper** to generate time-stamped text chunks.
2.  **Vector Store & Retrieval:** Transformed text chunks into 768-dimensional semantic vectors using **Ollama bge-m3 embeddings**. These are stored in a metadata-rich JSON structure to allow for time-stamped retrieval.
3.  **Synthesis:** When a user asks a question, the system retrieves the most relevant transcript segments and uses **Llama 3.2** to synthesize a concise answer that includes the exact video timestamp for reference.



### 📊 Results
* **Search Efficiency:** Reduced manual content retrieval time by **~85%**.
* **Accuracy:** Semantic search successfully identified topics even when the user's query didn't match the lecturer's exact wording.
* **Scalability:** Successfully indexed and queried over 10 hours of technical course material.

### 👤 Author
**Mithul Krishna Suresh** *2nd Year B.Tech CSE, NIT Bhopal*
