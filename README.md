# Multimodal AI Assistant

A versatile AI application with dual functionality: an HTML learning assistant and a document expert for PDF analysis.

## Features

### HTML Learning Assistant
- **Text-based Interaction**: Ask questions about HTML and receive detailed explanations
- **Image Analysis**: Upload images of HTML code or websites for visual analysis via Gemini
- **Voice Input**: Speak your questions with built-in speech-to-text using Groq's Whisper model
- **Real-time Responses**: Streaming responses for a fluid conversation experience

### Document Expert
- **PDF Analysis**: Upload PDF documents for semantic analysis
- **Question Answering**: Ask specific questions about your documents
- **RAG Implementation**: Utilizes Retrieval-Augmented Generation for accurate responses

## Installation

### Prerequisites
- Python 3.8+
- Required packages:

```bash
pip install gradio groq google-generativeai llama-index llama-index-llms-groq llama-index-embeddings-huggingface pillow sentence-transformers pypdf
```

### API Keys
You'll need to obtain API keys for:
1. **Groq** - For LLM responses and audio transcription
2. **Google Gemini** - For image analysis

Set your API keys either in the code or as environment variables:

```python
# In your code
os.environ["GROQ_API_KEY"] = "your_groq_api_key_here"
os.environ["GEMINI_API_KEY"] = "your_gemini_api_key_here"
```

Or in PowerShell:
```powershell
$env:GROQ_API_KEY = "your_groq_api_key_here"
$env:GEMINI_API_KEY = "your_gemini_api_key_here"
```

## Running the Application

```bash
python main.py
```

The application will start a Gradio web server. Access the interface at:
- Local URL: http://127.0.0.1:7860
- Or use the public share link provided in the console output

## Technical Implementation

### Models Used
- **Groq LLama 3.3 70B** - For text generation
- **Google Gemini 1.5 Flash** - For image understanding
- **Whisper Large v3** - For speech-to-text conversion
- **BAAI/bge-small-en-v1.5** - For document embeddings

### Architecture
- Gradio framework for the web UI
- LlamaIndex for document indexing and RAG
- Streaming responses for better user experience
- Multimodal inputs with text, image, and audio processing

## Possible customization

Modify the system prompt in the `chat_context` variable to change the assistant's personality or domain expertise. You can also adjust model parameters like temperature and token limits for different response styles.

