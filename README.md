# FastAPI Text Summarization

## Summary

This project provides a FastAPI application with an endpoint `/summarize` that takes text input and returns a summarized version using the OpenAI API. It leverages the capabilities of large language models (LLMs) to condense information efficiently, making it a valuable tool for developers and users looking to quickly digest large volumes of text.

## Setup & Usage Instructions

### Prerequisites

- Python 3.7 or higher
- An OpenAI API key (sign up at [OpenAI](https://www.openai.com/) if you don't have one)

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/fastapi-text-summarization.git
   cd fastapi-text-summarization
   ```

2. Create a virtual environment and activate it:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows use `venv\Scripts\activate`
   ```

3. Install the required packages:
   ```bash
   pip install -r requirements.txt
   ```

4. Set your OpenAI API key as an environment variable:
   ```bash
   export OPENAI_API_KEY='your_openai_api_key'  # On Windows use `set OPENAI_API_KEY='your_openai_api_key'`
   ```

### Running the Application

To start the FastAPI server, run the following command:
```bash
uvicorn main:app --reload
```

The API will be accessible at `http://127.0.0.1:8000`.

### Example API Calls

You can use tools like `curl`, Postman, or any HTTP client to make requests to the API. Here are some example calls:

1. **Summarizing a short text:**
   ```bash
   curl -X POST "http://127.0.0.1:8000/summarize" -H "Content-Type: application/json" -d '{"text": "FastAPI is a modern web framework for building APIs with Python 3.6+ based on standard Python type hints."}'
   ```

2. **Summarizing a longer article:**
   ```bash
   curl -X POST "http://127.0.0.1:8000/summarize" -H "Content-Type: application/json" -d '{"text": "In recent years, the field of artificial intelligence has seen tremendous growth. From self-driving cars to advanced natural language processing, AI technologies are reshaping various industries and creating new opportunities for innovation."}'
   ```

3. **Summarizing a research paper abstract:**
   ```bash
   curl -X POST "http://127.0.0.1:8000/summarize" -H "Content-Type: application/json" -d '{"text": "This paper explores the implications of deep learning on the future of automated systems. We analyze the current state of the technology and predict its impact on various sectors."}'
   ```

### Key Files

- `main.py`: The main application file where the FastAPI app is instantiated and the `/summarize` endpoint is defined.
- `requirements.txt`: A list of dependencies required to run the application, including FastAPI and OpenAI SDK.
- `README.md`: This documentation file that provides an overview and instructions for the project.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more information.

---

For more detailed API documentation or a demo, please visit our GitHub Pages site at [GitHub Pages URL].