
# Day 4 – VulnAgent: Tools, Structured Output & Google Sheets

## Project Name
**VulnAgent – AI-Based Vulnerability Assessment and Prioritization Agent**

## Overview
VulnAgent is an AI-based vulnerability assessment assistant developed as part of the Day 4 Agentic AI training.

It analyzes vulnerability descriptions provided by users, identifies possible security risks, and gives defensive recommendations. It uses LangChain tools, Pydantic structured output, and Google Sheets to store vulnerability assessment records.

The project focuses on understanding how an AI agent uses tools, generates structured responses, and interacts with external data storage.

## Technologies Used
- Python
- Google Colab
- LangChain
- LangChain Groq
- Groq LLM – `openai/gpt-oss-120b`
- Pydantic
- Google Sheets
- gspread

## Day 4 Concepts Implemented

### 1. Agent Creation
Created a VulnAgent using LangChain's `create_agent()` function.

The agent uses a Groq language model and a system prompt to guide its behavior.

### 2. Tool Integration
Implemented the following tools:

- `get_vulnerability_guidance()` – Provides defensive security recommendations for different vulnerability types.
- `get_severity_guidance()` – Explains vulnerability severity categories.
- `log_vulnerability_assessment()` – Saves vulnerability assessment details to Google Sheets.

### 3. Structured Output with Pydantic
Created a Pydantic model named `VulnerabilityAssessment`.

The model contains:
- Vulnerability
- Severity
- Impact
- Remediation
- Verification
- Confidence

The LLM converts informal vulnerability descriptions into structured assessment records.

### 4. Testing with Messy Inputs
Tested structured output using five informal vulnerability descriptions:

1. SQL Injection
2. Cross-Site Scripting (XSS)
3. Weak Password
4. Insecure Direct Object Reference (IDOR)
5. Remote Code Execution (RCE)

### 5. Google Sheets Integration
Connected VulnAgent to Google Sheets using `gspread`.

The agent can store vulnerability assessment records in a spreadsheet with the required fields.

Duplicate checking was also implemented to avoid saving identical assessment records repeatedly.

### 6. Agent Tracing
Used `pretty_print()` to observe the agent's execution messages.

The trace helps identify:
- User messages
- AI messages
- Tool calls
- Tool responses
- Final agent responses

### 7. Counting Tool and Model Calls
Implemented counters to observe the number of AI messages and tool calls during agent execution.

### 8. Tool Description Experiment
Created a temporary tool named `tool1` with the vague description `"Does stuff."`.

This experiment demonstrates how tool names and descriptions influence an AI agent's tool selection.

## Sample Test Case

**Input:**
A website stores user passwords in plain text.

**Expected Analysis:**
- Vulnerability: Insecure Password Storage
- Severity: Depends on the application and exposure
- Impact: User passwords may be exposed if the database is compromised
- Remediation: Use secure password hashing such as Argon2id or bcrypt
- Verification: Review the password-storage implementation

## Learning Outcomes
- Understood how to create an AI agent using LangChain.
- Learned how to define and integrate tools.
- Implemented structured output using Pydantic.
- Connected an AI agent to Google Sheets.
- Observed agent execution using tracing.
- Learned the importance of clear tool names and descriptions.
- Tested vulnerability assessments using different user inputs.

## Safety and Limitations
- VulnAgent analyzes only vulnerability descriptions provided by the user.
- It does not perform real system scans.
- It does not claim verified vulnerability findings.
- It does not generate official CVSS scores unless supported by provided information.
- It focuses on defensive security recommendations.

## Conclusion
Day 4 enhanced VulnAgent with tool integration, structured output, Google Sheets logging, and agent tracing.

The implementation demonstrates how an AI agent can use tools and structured data to provide organized vulnerability assessment assistance.
