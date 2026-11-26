
# VulnAgent - AI-Based Vulnerability Assessment and Prioritization Agent

## Day 3 - Agent Development and Testing

## Overview

VulnAgent is an AI-powered cybersecurity assistant developed using Python, LangChain, and Groq.

On Day 3, the project was extended by implementing a prompt-based LLM chain, conversation memory, CSV-based testing, and a basic LangChain agent.

The agent analyzes user-provided vulnerability descriptions and provides structured security recommendations.

## Day 3 Implementation

- Connected Day 2 code with the Day 3 notebook to avoid duplicate code.
- Integrated the Groq LLM using ChatGroq.
- Created a cybersecurity system prompt for VulnAgent.
- Implemented ChatPromptTemplate for structured prompting.
- Used MessagesPlaceholder to support conversation history.
- Created an LLM chain using the prompt, model, and output parser.
- Implemented conversation memory to remember previous questions.
- Created a cybersecurity test dataset using CSV.
- Implemented automated keyword-based response testing.
- Calculated test pass rate.
- Created a basic LangChain agent using create_agent().

## Technologies Used

- Python
- Google Colab
- LangChain
- LangChain-Groq
- Groq API
- CSV
- ChatPromptTemplate
- StrOutputParser

## Features

- Vulnerability identification
- Basic severity and impact analysis
- Remediation recommendations
- Structured vulnerability reports
- Conversation history
- CSV-based testing
- Automated test pass-rate calculation

## Testing

VulnAgent was tested using cybersecurity-related questions such as:

- SQL Injection
- Weak Passwords
- Security Headers
- Remote Code Execution
- SQL Injection Prevention

The responses were evaluated using expected keywords stored in a CSV file.

## Concepts Learned

- LLM Integration
- Prompt Engineering
- ChatPromptTemplate
- LangChain Chains
- Conversation Memory
- CSV Data Handling
- Automated Testing
- LangChain Agent Creation
- Error Handling

## Project Status

Day 3 Completed - Under Development

## Future Scope

- Add cybersecurity tools to the agent.
- Integrate vulnerability scanning tools.
- Analyze security logs.
- Improve vulnerability prioritization.
- Generate automated security reports.
- Implement advanced response evaluation.

## Day 3 Summary

During Day 3, VulnAgent was developed further by connecting the LLM with structured prompts and conversation memory. A CSV-based testing system was implemented to evaluate responses, and a basic LangChain agent was created as an introduction to agent development.
