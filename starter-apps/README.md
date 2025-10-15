# Cerebras Starter Applications

Welcome! This directory features ready-to-use, production-quality applications built with Cerebras models via the Cerebras Inference API. These apps are designed as templates and inspiration for your own projects—spanning education, content creation, visualization, and more.

## What You'll Find Here

- **End-to-end app examples**: Fully functional apps for real-world use cases
- **Starter templates**: Easily customizable for your own needs
- **Best practices**: Clean code, robust error handling, and secure API management

## Application Categories

### Streamlit Apps

- **Book Writer (Prompt2Prose)**: Turn ideas into full-length books with chapters using Cerebras Inference (`starter-apps/book-writer/`)
- **Multilingual Mindmap Generator**: Create interactive mindmaps from PDFs or topics in 30+ languages (`starter-apps/mindmap-generator/`)


## Prerequisites

- Python 3.9+ (for Streamlit apps)
- Cerebras Cloud account and API key: https://cloud.cerebras.ai/
- (Some apps) `python-dotenv` for `.env` loading and optional third-party libs as listed in each app’s `requirements.txt`

## How to Use

### For Streamlit Apps

1. Choose an app from above and navigate to its directory
2. Create a virtual environment (recommended)
3. Install dependencies: `pip install -r requirements.txt`
4. Export your API key: on macOS/Linux `export CEREBRAS_API_KEY=...`; on Windows PowerShell `setx CEREBRAS_API_KEY "YOUR_KEY"`
5. Run the app: `streamlit run app.py`
6. Customize as needed

### For Next.js Apps

No Next.js apps are included in this snapshot. Stay tuned.

## Application Types

- Content generation and authoring
- Document processing and visualization
- Multilingual information exploration

## App-specific Notes

- `book-writer/`: Uses the Cerebras API through agents defined in `book_writer_agent.py`. The UI collects `CEREBRAS_API_KEY` at runtime and sets it in-process.
- `mindmap-generator/`: Uses the `openai` Python SDK pointed at `https://api.cerebras.ai/v1` to call Cerebras models. Configure `CEREBRAS_API_KEY` via environment or sidebar input.
---

## Related Resources

- Cerebras Cloud: https://cloud.cerebras.ai/
- Cerebras Inference API docs: https://inference-docs.cerebras.ai/
