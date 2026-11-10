# ChatGroq Demo

A Streamlit application that leverages LangChain and Groq to provide document-based question answering.

## Overview

This project demonstrates a chatbot application that:
- Loads documentation from LangChain's official docs
- Uses Groq's Mixtral model for language understanding
- Implements a retrieval-augmented generation (RAG) pipeline
- Provides an interactive chat interface through Streamlit

## Features

- **Document Loading**: Automatically loads and processes documentation from LangChain's official website
- **Vector Store**: Creates a FAISS vector database for efficient document retrieval
- **RAG Pipeline**: Combines document retrieval with Groq's language model for accurate responses
- **Streamlit Interface**: Provides an interactive web interface for chatting with the documentation
- **Real-time Answers**: Get instant answers based on the loaded documentation

## Installation

### Prerequisites

- Python 3.7 or higher
- pip (Python package installer)

### Install Dependencies

```bash
pip install streamlit langchain langchain-groq langchain-community ollama python-dotenv
```

### Set Up Environment Variables

Create a `.env` file in the project root and add your Groq API key:

```env
GROQ_API_KEY=your_groq_api_key_here
```

## Usage

### Run the Application

```bash
streamlit run app.py
```

### How to Use

1. Open your web browser and navigate to the URL provided by Streamlit (usually http://localhost:8501)
2. Enter your question or prompt in the text input field
3. Click the send button or press Enter to get an answer based on the loaded documentation
4. Use the "Document Similarity Search" expander to see which documents were used to generate the answer

## Project Structure

- `app.py`: The main Streamlit application file
- `.gitignore`: Git ignore file with development environment settings
- `.env`: Environment variables file (not committed to version control)

## Dependencies

The project requires the following Python packages:

- streamlit: Web application framework
- langchain: Language model development framework
- langchain-groq: Integration with Groq's API
- langchain-community: Community contributed LangChain integrations
- ollama: Local Ollama embeddings
- python-dotenv: Environment variable management

## Notes

- The application loads documentation from [LangChain's official docs](https://docs.smith.langchain.com/) on startup
- Only the first 50 documents are processed for performance reasons
- The application uses Groq's Mixtral-8x7b-32768 model for language understanding
- All API keys and sensitive information should be stored in the `.env` file

## Troubleshooting

### Common Issues

1. **Groq API Key Not Working**
   - Ensure your API key is correctly entered in the `.env` file
   - Verify that your Groq account has the necessary permissions

2. **Streamlit Not Starting**
   - Make sure all dependencies are installed
   - Check if port 8501 is available on your system

3. **Document Loading Issues**
   - Verify that the documentation URL is accessible
   - Check network connectivity

## Contributing

If you want to contribute to this project, please follow these guidelines:

1. Fork the repository
2. Create a new branch for your feature or bug fix
3. Make your changes
4. Test your changes thoroughly
5. Submit a pull request

## License

This project is licensed under the MIT License. See the LICENSE file for more details.