
# Day 5 – RAG (Retrieval-Augmented Generation)

## Project Name
VulnAgent – AI-Based Vulnerability Assessment and Prioritization Agent

## Day 5 Objective
The objective of Day 5 is to implement Retrieval-Augmented Generation (RAG) and connect it with the existing VulnAgent developed during Days 1–4.

RAG allows the agent to retrieve relevant information from a knowledge base before generating a response.

## Project Overview
VulnAgent is a cybersecurity-focused AI agent that analyzes user-provided vulnerability descriptions and provides defensive security recommendations.

In Day 5, a cybersecurity knowledge base was created and connected to the agent using RAG.

## Technologies Used
- Python
- Google Colab
- LangChain
- Groq LLM
- Sentence Transformers
- FAISS
- NumPy

## Knowledge Base
Since a PDF was not available, a text-based knowledge file was created.

File name: `vulnagent_knowledge.txt`

The knowledge base contains information about:
- SQL Injection
- Cross-Site Scripting (XSS)
- Weak Passwords
- Insecure Direct Object Reference (IDOR)
- Remote Code Execution (RCE)

Each vulnerability contains its description, impact, remediation, and verification details.

## RAG Workflow
1. Load the cybersecurity knowledge file.
2. Split the text into smaller chunks.
3. Generate embeddings using Sentence Transformers.
4. Store the embeddings in a FAISS vector index.
5. Retrieve relevant knowledge based on the user's question.
6. Pass the retrieved context to the VulnAgent.
7. Generate a response using the Groq language model.

## Implementation
The following components were implemented:

- Text loading and preprocessing
- Text chunking with overlap
- Embedding generation using `all-MiniLM-L6-v2`
- Vector storage using FAISS
- Similarity-based knowledge retrieval
- RAG search tool
- Integration with Day 4 guidance and severity tools
- Interactive question-and-answer interface

## Day 4 and Day 5 Integration
The Day 4 vulnerability guidance and severity tools were connected with the Day 5 RAG retrieval tool.

The combined agent uses retrieved cybersecurity knowledge to support vulnerability analysis and provide defensive recommendations.

## Sample Questions
- Explain SQL Injection and its remediation.
- What is XSS and how can it be prevented?
- What are the security risks of weak passwords?
- Explain IDOR and its remediation.
- What are the defensive measures for RCE?

## Expected Output
VulnAgent provides a structured vulnerability analysis containing:

- Vulnerability Name
- Severity
- Impact
- Remediation
- Verification
- Confidence

The agent avoids claiming real system scans or inventing scan results and CVSS scores.

## Learning Outcomes
- Understanding Retrieval-Augmented Generation
- Creating and managing a knowledge base
- Generating text embeddings
- Using FAISS for vector similarity search
- Retrieving relevant context
- Connecting RAG with an AI agent
- Improving cybersecurity knowledge-based responses

## Conclusion
Day 5 successfully extended VulnAgent by integrating a cybersecurity knowledge base using RAG.

The agent can retrieve relevant defensive information and use it to support vulnerability assessment and prioritization.

This implementation demonstrates how retrieval-based knowledge can improve the usefulness and reliability of an AI agent.
