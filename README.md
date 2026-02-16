# AI-Powered-HR-Assistant

AI-Powered HR Assistant Documentation
1. Project Overview
This project implements a Retrieval-Augmented Generation (RAG) based HR Assistant that answers questions about Nestlé’s HR policy document using OpenAI GPT-3.5 Turbo and Chroma Vector Database.It follows the required project steps:

        1. Import essential tools and set up OpenAI API.
        2. Load Nestlé HR policy using PyPDFLoader and split it into chunks.
        3. Create vector representations using OpenAI embeddings and store in Chroma DB.
        4. Build a question-answering system using GPT-3.5 Turbo.
        5. Create a prompt template to guide chatbot responses.
        6. Use Gradio to build a user-friendly chatbot interface.
        7. Deploy the chatbot locally.

2. System Architecture
The system follows a Retrieval-Augmented Generation (RAG) pipeline. The architecture diagram below illustrates the complete workflow.
                User Question
                     ↓
                Retriever (Chroma DB)
                     ↓
                Top 4 relevant chunks
                     ↓
                Prompt Template
                     ↓
                GPT-3.5 Turbo
                     ↓
                Final Answer + Page Sources
                     ↓
                Gradio Interface
 
3. Component Explanation
        • PDF Loader: Extracts text from the HR policy PDF.
        • Text Splitter: Divides document into manageable chunks.
        • OpenAI Embeddings: Converts text chunks into semantic vectors.
        • Chroma DB: Stores and retrieves vector embeddings.
        • Retriever: Fetches the most relevant chunks based on similarity search.
        • Prompt Template: Guides GPT-3.5 to answer using only retrieved context.
        • GPT-3.5 Turbo: Generates grounded responses.
        • Gradio UI: Provides an interactive chatbot interface.
4. Data Flow Explanation
User Question → Embedding Comparison → Retrieval from Chroma DB → Context inserted into Prompt Template → GPT-3.5 Turbo generates answer → Answer returned with source page citations.
5. Conclusion
This project demonstrates a complete RAG pipeline including document ingestion, text preprocessing, embedding generation, vector database storage, retrieval, LLM-based answer generation, and user interface deployment.

