# Rag-Mistral-Assignmentt
This project implements a Retrieval-Augmented Generation (RAG) system using  ChromaDB, Mistral-7B-Instruct, GPT-4-All, and All-MiniLM-L6-v2 embeddings. 
The focus is on leveraging various retriever methods such as MultiQueryRetriever, BM25, Fiass, and ensemble techniques (combining Fiass and BM25 with equal and weighted configurations) to create an efficient question-answering system.

![RAG Illustration](RAG.png "RAG Workflow")

## **Project Overview**
I trained the RAG system on a dataset derived from the Drug Regulatory Authority of Pakistan (DRAP). DRAP is responsible for overseeing drug regulations in Pakistan. The dataset consisted of PDFs downloaded directly from the official DRAP website, containing valuable information relevant to the pharmaceutical domain.

The system was designed to answer Frequently Asked Questions (FAQs) based on the content of the DRAP PDFs. The implementation is particularly suited for providing concise, accurate, and context-aware responses.

## Key Achievements
### Model Performance:
- The RAG-Mistral-7B implementation, combined with All-MiniLM-L6-v2 embeddings and Fiass/BM25 retriever, performed exceptionally well in answering FAQs related to the DRAP content. #### It excelled in scenarios where:
- When relevant content was available, it provided clear, accurate, and context-specific answers, demonstrating a high level of precision.
- In cases where no relevant context existed, the model responded appropriately by acknowledging the absence of an answer in the given dataset. This prevented hallucination or the generation of misleading information, ensuring reliability and trustworthiness.

### Optimal Chunking Strategy:
- To improve retrieval and answer accuracy, I experimented with different chunk sizes:
- Using a chunk size of 2500 with a 200-word overlap significantly enhanced the model's ability to retrieve precise and relevant information.

### Retriever Insights:
- BM25 and Fiass (used individually and in combination) delivered to-the-point answers, minimizing noise and ensuring highly relevant retrievals.
- The ensemble of Fiass and BM25, with both equal and weighted configurations, further boosted performance, especially for edge cases.

## Future Applications
This project demonstrates the potential for using RAG in domain-specific applications, particularly in healthcare and pharmaceutical regulation. 
The DRAP dataset can be extended further to address broader regulatory and compliance-related queries.

