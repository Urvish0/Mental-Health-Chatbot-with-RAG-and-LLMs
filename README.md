# Mental Health Chatbot with RAG and LLMs

This project implements a mental health chatbot that provides emotional support using a Retrieval-Augmented Generation (RAG) model with HuggingFace embeddings and ChatGroq. The bot helps users navigate challenging times by providing empathetic responses and maintaining context across conversations through memory integration.

## Overview

The Mental Health Chatbot is designed to simulate supportive conversations for users experiencing difficult emotional periods. It can offer guidance, reassurance, and emotional support by accessing a conversational memory stored in Astra DB.

## Features

- **Generative AI-Powered Responses**: Utilizes the `llama-3.1-70b-versatile` model from HuggingFace for intelligent, contextually appropriate responses.
- **Memory Integration**: Conversation history is stored and retrieved from Astra DB, maintaining context across sessions.
- **Custom SearchTool**: Implemented using BeautifulSoup for fetching relevant information.
- **Data-Driven Training**: Trained on mental health-related datasets to provide empathetic conversations.

## Datasets Used

1. **[Amod Mental Health Counseling Conversations Dataset](https://huggingface.co/datasets/Amod/mental_health_counseling_conversations?row=15)**:
   - This dataset includes mental health counseling conversations and provides the foundation for the chatbot's dialogue generation.
   
2. **Reddit Mental Health Discussions Dataset**:
   - Extracted from Reddit, this dataset was cleaned post-collection and consists of mental health conversations, enriching the chatbot’s ability to understand and respond empathetically.

## Setup Instructions

### Prerequisites

- Python 3.x
- [Astra DB Account](https://astra.datastax.com/register)
- HuggingFace Account and API key
- Groq Account and API key
- Langchain Account and API key

### Clone the Repository

```bash
git clone https://github.com/Urvish0/Mental-Health-Chatbot-with-RAG-and-LLMs.git
cd Mental-Health-Chatbot-with-RAG-and-LLMs
```

### Create Astra DB Instance

1. [Sign up for Astra DB](https://astra.datastax.com/register) and create a database.
2. Obtain your **Astra DB API Key** from the dashboard.
3. **Important**: You must revisit your Astra DB within 48 hours to avoid the database being paused automatically.

### Install Dependencies

```bash
pip install -r requirements.txt
```

### Run the Chatbot

```bash
mentalhealth_chatbot.ipynb
```

### Memory Implementation

- Conversations are stored in Astra DB for contextual understanding in future interactions.

## How It Works

1. **Embeddings**: The chatbot uses the HuggingFace `sentence-transformers/all-MiniLM-L6-v2` model for embeddings.
2. **RAG Model**: Retrieves relevant information from Astra DB to maintain context and provide better responses.
3. **Custom Search Tool**: Implemented using BeautifulSoup for enhanced search capabilities.

## Project Files

- `mentalhealth_chatbot.ipynb`: Jupyter notebook with main script and implementation steps to run the chatbot.
- `requirements.txt`: List of dependencies.

## Contributing

Feel free to open an issue or submit a pull request.
