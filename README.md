# Medical-Chatbot-with-Retrieval-Based-QA

This project is a Flask-based web application that integrates a medical knowledge base using a retrieval-based question-answering (QA) model. 
The chatbot answers questions by retrieving relevant context from a Pinecone vector store and then generating answers using the Llama 2 model.

## Technologies Used

- **Flask**: A lightweight WSGI web application framework for Python.
- **LangChain**: A framework for developing applications powered by LLMs (Large Language Models).
- **Pinecone**: A vector database to store and retrieve embeddings efficiently.
- **Hugging Face Transformers**: For downloading pre-trained embeddings and tokenization.
- **Llama 2**: A powerful language model used to generate responses.
- **dotenv**: A module to load environment variables from a `.env` file.
- **CTransformers**: A framework to run transformer models, such as Llama.

## Features

- **Chat Interface**: A simple web-based chat interface for users to interact with the medical chatbot.
- **Context-Aware QA**: The chatbot answers user queries by retrieving relevant information from a vector database and generating context-based responses using a Llama 2 model.
- **Customizable Prompting**: The chatbot uses a flexible prompt template to guide the model’s responses.
- **Pinecone Integration**: Efficiently stores and retrieves vectorized medical data for fast, context-aware answers.

## Project Setup

### Prerequisites

Before running the application, ensure you have the following:

- **Python 3.8+**
- **Pinecone account** to generate the API key and environment.


### Create and Activate Virtual Environment

conda create -p venv python==3.10 -y

### Install Dependencies

pip install -r requirements.txt

### Configure Environment Variables

PINECONE_API_KEY=<your_pinecone_api_key>
PINECONE_API_ENV=<your_pinecone_environment>


### Download and Set Up the Model

Download the Llama 2 model and place it in the model/ directory. You can download the model from a source like Hugging Face.
The model used in this project is llama-2-7b-chat and should be placed in the model/ folder.

### unning the Application

python app.py


## Project Structure 

![alt text](image.png)

### How It Works
Embedding: The medical documents are embedded using Hugging Face pre-trained embeddings and stored in a Pinecone vector index.
Question Answering: When the user sends a query, the chatbot retrieves relevant context from the Pinecone vector store and uses the Llama 2 model to generate a response.
Flask Web Interface: The user interacts with the chatbot through a simple HTML interface powered by Flask. Messages are sent via POST requests and responses are rendered back to the user.

### Usage

Type your medical-related query into the input field and hit "Send".
The chatbot will retrieve relevant context from Pinecone and generate a response using the Llama model.

# Acknowledgements
Pinecone: For efficient vector-based document storage and retrieval.
LangChain: For simplifying the development of LLM-powered applications.
Llama 2: For providing state-of-the-art language generation capabilities.
Hugging Face: For offering pre-trained models for text embeddings.
Thank to Krish Naik and Sunny Savita and Bappy Sir for inspiration and guidance..


### Contact

bhimrao.pawar.07@gmail.com 
