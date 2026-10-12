# Medical-Knowledge-Assistant-using-RAG-and-LangChain

Built a medical question-answering prototype using LLaMA 2, LangChain, Sentence Transformers, and ChromaDB to retrieve relevant information from medical reference documents and generate context-grounded responses. Explored prompt engineering as a baseline and an experimental approach to evaluating answer groundedness and relevance.

## Project Overview

The **Medical Knowledge Assistant** is a Generative AI project that explores how Large Language Models (LLMs) can answer medical questions using information retrieved from external medical reference documents.

The project implements Retrieval-Augmented Generation (RAG) by combining document processing, semantic search, vector storage, and LLM-based response generation. It also explores prompt engineering to establish a baseline for answering questions without document retrieval.

## Objectives

- Develop a medical question-answering prototype using an LLM.
- Extract and preprocess text from medical reference PDFs.
- Split lengthy documents into manageable, overlapping text chunks.
- Generate semantic embeddings using Sentence Transformers.
- Store and retrieve document embeddings using ChromaDB.
- Generate context-grounded answers using RAG.
- Explore the evaluation of answer groundedness and relevance.

## Key Features

- **LLM Integration:** Uses LLaMA 2 13B Chat for natural-language response generation.
- **Prompt Engineering:** Explores baseline question answering using structured prompts.
- **Document Processing:** Extracts text from medical PDFs using PyMuPDF.
- **Text Chunking:** Splits documents into 1,000-character chunks with a 200-character overlap.
- **Semantic Embeddings:** Uses `sentence-transformers/all-MiniLM-L6-v2` to represent text as numerical vectors.
- **Vector Database:** Uses ChromaDB to store and search document embeddings.
- **Context Retrieval:** Retrieves relevant medical text based on semantic similarity to the user's question.
- **RAG Pipeline:** Combines retrieved document context with the user query to generate responses.
- **Answer Evaluation:** Explores groundedness and relevance as response evaluation criteria.

## Technologies Used

| Category                | Technologies                               |
| ----------------------- | ------------------------------------------ |
| Programming Language    | Python                                     |
| Large Language Model    | LLaMA 2 13B Chat                           |
| LLM Framework           | LangChain                                  |
| Embedding Model         | Sentence Transformers (`all-MiniLM-L6-v2`) |
| Model Ecosystem         | Hugging Face                               |
| Vector Database         | ChromaDB                                   |
| PDF Processing          | PyMuPDF                                    |
| Data Processing         | Pandas                                     |
| Development Environment | Jupyter Notebook / Google Colab            |

## Project Workflow

1. **LLM Initialization:** Configure the LLaMA 2 language model for text generation.
2. **Baseline Question Answering:** Explore prompt engineering to generate answers without external document retrieval.
3. **Document Loading:** Extract text from medical reference PDFs using PyMuPDF.
4. **Text Splitting:** Divide extracted text into chunks of 1,000 characters with a 200-character overlap.
5. **Embedding Generation:** Convert document chunks into vector representations using Sentence Transformers.
6. **Vector Storage:** Store the embeddings and associated document chunks in ChromaDB.
7. **Semantic Retrieval:** Retrieve relevant document chunks based on the user's question.
8. **Context-Grounded Generation:** Pass the retrieved context and question to the LLM to generate a response.
9. **Response Evaluation:** Explore answer groundedness and relevance using an experimental evaluation workflow.

## Evaluation

The project explores two response evaluation criteria:

- **Groundedness:** Examines whether the generated answer is supported by the retrieved medical context.
- **Relevance:** Examines whether the generated answer appropriately addresses the user's question.

The evaluation workflow is experimental. Quantitative scores and comparative performance claims should be reported only after the pipeline has been executed and the results validated.

## Future Enhancements

- Improve retrieval quality through chunking and retriever optimization.
- Include document references and page numbers in generated answers.
- Implement structured evaluation metrics and a curated test dataset.
- Compare prompt-based and RAG-based responses systematically.
- Add safeguards for questions that cannot be answered from the available documents.
- Develop an interactive interface using Streamlit.
- Add error handling, automated tests, and a reproducible dependency file.

## Disclaimer

This project is intended for educational and demonstration purposes only. It is **not a medical diagnostic tool** and must not be used as a substitute for professional medical advice, diagnosis, or treatment. Medical information generated by the system may be incomplete or inaccurate. Always consult qualified healthcare professionals for medical concerns.
