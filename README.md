# Medibot
Medibot – An AI-Powered Medical Q&A ChatbotMedibot is a smart chatbot that can answer medical-related questions using Retrieval-Augmented Generation (RAG). It utilizes natural language understanding, semantic search, and state-of-the-art large language models (LLMs) to provide accurate, contextual and trustworthy answers based on a set of medical documents curated by me. This project is capable of showcasing the potential of LLMs to work together with custom data sources to implement domain specific assistants; in this case a health care assistant.

Key Features:
LLM-Powered Responses: Generates natural and fluent answers using Hugging Face’s Mistral-7B-Instruct.
FAISS-Based Vector Search: Efficients retrieves relevant medical information from a pre-processed knowledge base.
Custom Prompt Engineering: Makes sure answers are safe, constraints, and based solely on the provided context.
Streamlit Web App Interface: Clean, interactive user interface for real-time chat.
Context-Aware and Responsible: Responsible for not providing an answer to questions based on the content of the source data.

How It Function:
User input: The user inputs a question into the chat interface.
Text embedding: The question is converted into a vector using all-MiniLM-L6-v2 from sentence-transformers.
Document retrieval: FAISS retrieves the most relevant context (top 3) from the vector store.
Prompting the LLM: The context and question retrieved are converted into a prompt using a PromptTemplate tool.
Answer generation: The LLM (hosted via HuggingFace Inference Endpoint) generates an answer using only the text based on the context.
Output: The answer will be outputted in the chat window, completed with a conversation history already built.

Tech Stack:
Python - primary programming language.
Streamlit - frontend for the chatbot interface.
LangChain - orchestration between retrieval, prompt engineering, and LLMs.
FAISS(Facebook AI Similarity Search) - fast vector-based search to retrieve relevant document chunks.
HuggingFace Transformers - whe embedding and LLM Integration.
Sentence Transformers - used to convert text to embeddings for semantic search.


