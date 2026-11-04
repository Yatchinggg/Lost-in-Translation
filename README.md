# Lost in Translation

AI Thai Language Helper

This project is an AI assistant that uses local Thai language knowledge to help foreigners communicate in everyday situations in Thailand.

The AI can help users with Thai phrases for:
- Ordering food
- Taking a taxi
- Shopping
- Asking for directions
- Daily communication

## Local LLM

This project uses Qwen3:4B running locally through Ollama.
The application sends requests to http://127.0.0.1:11434/api/chat.
It does not require an OpenAI API key.

The five reference documents are loaded from the docs folder and
included as context when the local model answers a question.

## How to Run

1. Install Ollama: https://ollama.com/
2. Download the model:

   ```bash
   ollama pull qwen3:4b
   ```

3. Keep Ollama running.
4. Download and extract this repository.
5. Open Terminal in the extracted project folder.
6. Create and activate a Python virtual environment:

   ```bash
   python3 -m venv .venv
   source .venv/bin/activate
   ```

7. Install the required package:

   ```bash
   python -m pip install -r requirements.txt
   ```

8. Start the application:

   ```bash
   python -m streamlit run app.py
   ```

9. Open http://localhost:8501 in a browser.

## Example Question

How do I order food without chili?

## Limitations

Thai reference materials are project drafts and have not received
native-speaker review. Model answers may contain errors.
