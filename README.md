# AI Personal Assistant

A Flask-based web application that provides AI-powered assistance for answering questions and summarizing emails using OpenAI's GPT-5.4 model.

## Features

- **Ask Anything** — Submit questions and receive AI-generated responses
- **Email Summarization** — Paste email content and get concise 2-3 sentence summaries

## Project Structure

```
flask/
├── main.py              # Flask application with API endpoints
├── requirement.txt     # Python dependencies
├── static/
│   └── style.css       # Frontend styling
└── templates/
    └── index.html      # User interface
```

## Prerequisites

- Python 3.8+
- OpenAI API Key

## Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd flask
   ```

2. **Create a virtual environment**
   ```bash
   python -m venv venv
   venv\Scripts\activate    # Windows
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirement.txt
   ```

   > **Note:** Update `requirement.txt` to include all dependencies:
   > ```
   > flask
   > python-dotenv
   > openai
   > ```

4. **Configure environment variables**

   Create a `.env` file in the project root:
   ```
   OPENAI_API_KEY=your_openai_api_key_here
   ```

5. **Run the application**
   ```bash
   python main.py
   ```

6. **Open in browser**
   Navigate to `http://127.0.0.1:5000`

## API Endpoints

| Endpoint | Method | Description |
|----------|--------|-------------|
| `/` | GET | Render the main interface |
| `/ask` | POST | Submit a question to the AI assistant |
| `/summarize` | POST | Summarize an email |

### Example Request

```bash
curl -X POST http://127.0.0.1:5000/ask \
  -d "question=What is Python?"
```

## Configuration

- **Model:** GPT-5.4 (configurable in `main.py`)
- **Temperature:** 0.7 for Q&A, 0.3 for summarization
- **Max Tokens:** 512

## Technologies Used

- **Backend:** Flask (Python)
- **AI:** OpenAI API (GPT-5.4)
- **Frontend:** HTML, CSS, JavaScript

## License

MIT