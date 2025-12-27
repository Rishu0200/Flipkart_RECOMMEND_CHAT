# Flipkart Product Recommender Chatbot (RAG)

This project is an e‑commerce assistant that answers Flipkart‑style product queries using Retrieval‑Augmented Generation (RAG).  
It combines Flask, LangChain, Groq LLMs, and vector search to give concise, review‑aware responses.

## Tech Stack

- Python 3.9 / 3.10  
- Flask for the web API and UI  
- LangChain (history‑aware RAG pipeline)  
- Groq LLM (ChatGroq) as the chat model  
- Vector store for product documents (Astra DB / local)  
- Docker + Gunicorn for production serving

## Features

- Chat interface for product‑related questions (e.g., comparisons, pros/cons).
- Retrieval‑Augmented Generation over product titles and reviews.
- Session‑aware answers using chat history.
- Prometheus‑compatible `/metrics` endpoint for monitoring.
- Containerized with Docker and ready for deployment on Render.

## Local Development

1. Create and activate a virtual environment.
2. Install dependencies:
3. Set environment variables (e.g. `GROQ_API_KEY`, Astra credentials) in a `.env` file.
4. Run the app:
5. Open `http://localhost:5000` in your browser.


## Docker

Build the image:

Run the container:

Visit `http://localhost:5000` to use the chatbot.

## Deployment on Render

- Connect this GitHub repository to a new Render Web Service.
- Environment: Docker (Render builds from `Dockerfile`).
- Set the port to `5000`.
- Configure environment variables in the Render dashboard.

## Project Structure

- `app.py` – Flask application factory and routes.
- `flipkart/` – Data ingestion and RAG chain builder.
- `templates/` – HTML template for the chat UI.
- `static/` – Frontend assets (CSS, JS).
- `Dockerfile` – Container image definition.
- `requirements.txt` – Python dependencies.





