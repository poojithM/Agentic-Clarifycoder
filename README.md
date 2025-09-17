# Agentic ClarifyCoder

## Overview

Agentic ClarifyCoder is a Python-based workflow designed to generate reliable, production-ready code by leveraging a fine-tuned language model, ClarifyCoder. It follows the **Okanagan strategy**, which emphasizes a "code-when-certain, ask-when-unsure" approach. The system coordinates three agents to interpret user requirements, verify solutions, and produce executable code while minimizing errors through a disciplined clarification process.

## Features

- **Uncertainty Detection**: ClarifyCoder identifies ambiguous user prompts and asks targeted clarification questions.
- **Multi-Agent Workflow**: Three agents collaborate to ensure accurate code generation:
  - **Agent 1**: Interprets the problem and drafts an initial algorithm.
  - **Agent 2**: Reviews the draft for clarity, flagging ambiguities and posing concise questions if needed.
  - **Agent 3**: Generates complete, executable Python code based on the draft and user clarifications.
- **Okanagan Strategy**: Ensures code is generated only when requirements are clear, reducing errors and improving reliability.
- **Interactive Clarification**: Prompts users for answers to clarification questions, ensuring the final code meets their needs.
- **Production-Ready Output**: Delivers clean, executable Python code with example usage and proper edge-case handling.

## Prerequisites

- **Python**: Version 3.8 or higher
- **Dependencies**: Install required packages using the following command:
  ```bash
  pip install transformers peft langgraph langchain-core langchain-community
  ```
- **Hardware**: GPU recommended for faster model inference, but CPU is supported.
- **Model**: Uses the deepseek-ai/deepseek-coder-6.7b-instruct base model and the jie-jw-wu/clarify-coder adapter from Hugging Face.
