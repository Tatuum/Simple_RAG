# Personal RAG Chatbot

This project implements a Retrieval-Augmented Generation (RAG) chatbot that represents a specific person using their LinkedIn profile and personal summary. The chatbot is built using Gradio for the interface and OpenAI's GPT-4 for generating responses.

## Features

- Interactive chat interface using Gradio
- Personalized responses based on LinkedIn profile and summary
- Professional and engaging conversation style
- Context-aware responses about career, background, skills, and experience

## Prerequisites

- Python 3.8 or higher
- uv package manager
- OpenAI API key
- PDF file containing LinkedIn profile
- Text file containing personal summary

## Installation

1. Install uv package manager:
```bash
# For macOS and Linux
curl -LsSf https://astral.sh/uv/install.sh | sh

# For Windows (PowerShell)
(Invoke-WebRequest -Uri "https://astral.sh/uv/install.ps1" -UseBasicParsing).Content | pwsh -Command -
```

For more installation options and details, visit the [official uv documentation](https://github.com/astral-sh/uv).

2. Clone the repository:
```bash
git clone <repository-url>
cd <repository-name>
```

3. Install the required dependencies using uv:
```bash
uv pip install -r requirements.txt
```

4. Create a `.env` file in the root directory and add your OpenAI API key:
```
OPENAI_API_KEY=your_api_key_here
```

5. Prepare your data:
   - Place your LinkedIn profile PDF in the `me/linkedin.pdf` directory
   - Create a summary text file in `me/summary.txt`

## Project Structure

```
.
├── main.py              # Main application code
├── requirements.txt     # Project dependencies
├── .env                # Environment variables
└── me/
    ├── linkedin.pdf    # LinkedIn profile PDF
    └── summary.txt     # Personal summary
```

## Usage

Run the application:
```bash
python main.py
```

The application will start a local server and open a web interface where you can interact with the chatbot.

## Dependencies

- openai: OpenAI API client
- gradio: Web interface framework
- python-dotenv: Environment variable management
- pypdf: PDF processing
