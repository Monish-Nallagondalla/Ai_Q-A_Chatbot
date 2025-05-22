# Simple Q&A Chatbot with Streamlit

This repository contains a simple Q&A chatbot built with Streamlit, offering two implementations: one using OpenAI's API and another using the Ollama framework. Both versions utilize LangChain for prompt management and response generation, providing a user-friendly interface to interact with the chatbot.

## Table of Contents
- [Overview](#overview)
- [Features](#features)
- [File Structure](#file-structure)
- [Setup Instructions](#setup-instructions)
- [Requirements](#requirements)
- [Usage](#usage)
- [License](#license)

## Overview
The project implements a question-answering chatbot with a Streamlit web interface. Users can input questions, select a model (OpenAI or Ollama), and adjust parameters like temperature and max tokens to customize responses. The OpenAI version integrates with OpenAI's API, while the Ollama version uses a local or server-hosted Ollama model (e.g., Mistral).

## Features
- Interactive Streamlit interface for user input and response display.
- Supports two backend models:
  - OpenAI API for cloud-based LLM inference.
  - Ollama for local or server-hosted open-source models.
- Adjustable parameters: temperature (0.0 to 1.0) and max tokens (50 to 300).
- LangChain integration for prompt templating and response parsing.
- LangSmith integration for tracking and debugging (optional).

## File Structure
```
├── openai_chatbot.py       # Chatbot implementation using OpenAI API
├── ollama_chatbot.py       # Chatbot implementation using Ollama
├── requirements.txt        # Python dependencies
├── .env.example            # Example environment file for API keys
└── LICENSE                 # License file (MIT)
```

## Setup Instructions
1. **Clone the Repository**
   ```bash
   git clone https://github.com/your-username/simple-qa-chatbot.git
   cd simple-qa-chatbot
   ```

2. **Install Dependencies**
   Ensure you have Python 3.8+ installed. Install the required packages:
   ```bash
   pip install -r requirements.txt
   ```

3. **Set Up Environment Variables**
   - Copy the `.env.example` file to `.env`:
     ```bash
     cp .env.example .env
     ```
   - Update `.env` with your credentials:
     - For OpenAI version: Add your `OPENAI_API_KEY`.
     - For LangSmith tracking (optional): Add your `LANGCHAIN_API_KEY`.
     ```plaintext
     OPENAI_API_KEY=your_openai_api_key
     LANGCHAIN_API_KEY=your_langchain_api_key
     LANGCHAIN_TRACING_V2=true
     LANGCHAIN_PROJECT=Simple Q&A Chatbot With Ollama
     ```

4. **Set Up Ollama (for `ollama_chatbot.py`)**
   - Install Ollama by following the instructions at [Ollama's official site](https://ollama.ai).
   - Pull the desired model (e.g., Mistral):
     ```bash
     ollama pull mistral
     ```
   - Ensure the Ollama server is running locally or on a hosted instance.

5. **Run the Application**
   - For the OpenAI version:
     ```bash
     streamlit run openai_chatbot.py
     ```
   - For the Ollama version:
     ```bash
     streamlit run ollama_chatbot.py
     ```

## Requirements
The dependencies are listed in `requirements.txt`:
```
streamlit
openai
langchain
langchain-openai
langchain-community
python-dotenv
```

## Usage
1. Launch the Streamlit app using the instructions above.
2. In the sidebar, select the model (e.g., Mistral for Ollama or an OpenAI model).
3. Adjust the temperature and max tokens sliders as needed.
4. Enter your question in the text input field.
5. View the chatbot's response displayed on the main interface.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
```
