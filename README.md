# Agentic ClarifyCoder (Two-Agent Workflow)

## Overview
Agentic ClarifyCoder is a Python-based workflow designed to generate reliable, production-ready code using a fine-tuned language model, ClarifyCoder. It adopts a streamlined two-agent approach inspired by the Okanagan strategy’s “code-when-certain, ask-when-unsure” principle. The system coordinates two agents to interpret user requirements, clarify ambiguities, and produce executable code, minimizing errors through an efficient clarification process.

## Features
- **Uncertainty Detection**: ClarifyCoder identifies ambiguous user prompts and asks concise clarification questions.
- **Two-Agent Workflow**: Two agents collaborate to ensure accurate code generation:
  - **Agent 1**: Interprets the problem and poses clarification questions if needed.
  - **Agent 2**: Generates complete, executable Python code based on the user question and user requirements.
- **Okanagan-Inspired Strategy**: Ensures code is generated only when requirements are clear, enhancing reliability and reducing errors.
- **Interactive Clarification**: Prompts users for answers to clarification questions, ensuring the final code aligns with their needs.
- **Production-Ready Output**: Delivers clean, executable Python code with example usage and proper edge-case handling.

## Prerequisites
- **Python**: Version 3.8 or higher
- **Dependencies**: Install required packages using the following command:
  ```bash
  pip install transformers peft langgraph langchain-core langchain-community
  ```
- **Hardware**: GPU recommended for faster model inference, but CPU is supported.
- **Model**: Uses the deepseek-ai/deepseek-coder-6.7b-instruct base model and the jie-jw-wu/clarify-coder adapter from Hugging Face.

## Installation

Clone or download the repository containing the Agentic_ClarifyCoder.ipynb notebook.
Install the required dependencies:
```bash
pip install -q transformers peft langgraph langchain-core langchain-community
```
Ensure access to the Hugging Face models (deepseek-ai/deepseek-coder-6.7b-instruct and jie-jw-wu/clarify-coder).
Run the Jupyter notebook in an environment with GPU support for optimal performance.

## Usage

- **Open the Notebook**: Launch Agentic_ClarifyCoder_TwoAgent.ipynb in Jupyter Notebook or JupyterLab.
- **Run All Cells**: Execute the cells to initialize the model and set up the two-agent workflow.
- **Ask a Problem**: Call the agentic_clarify_coder function with a problem statement,
- **Answer Clarifications**: If Agent 1 detects ambiguity, it will prompt you with 1-4 questions. Provide clear answers to proceed.
- **Receive Final Code**: The workflow outputs executable Python code tailored to your requirements.

## Sample Interaction:

- **Problem**: "Write a python code to sort the array"
- **Agent 1 Output**: Generates checks if the problem is clear and asks clarifying questions if needed, such as:

        1.What type of sorting algorithm should be used?
        2.Is it necessary to use a built-in function for sorting?
        3.How should the function handle duplicate values in the array?
        4. What should the function return if the input array is empty or contains one element?


- **User Response**: "1. quick sort, 2. no, 3. like normal elements, 4. return list"
- **Agent 2 Output**: Generates final executable code incorporating the clarifications.


