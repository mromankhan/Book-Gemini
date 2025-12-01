# Quickstart for Interactive Book with RAG Chatbot

## Frontend (Docusaurus)

1.  **Navigate to the `frontend` directory:**
    ```bash
    cd frontend
    ```
2.  **Install dependencies:**
    ```bash
    npm install
    ```
3.  **Run the development server:**
    ```bash
    npm start
    ```
    The book will be available at `http://localhost:3000`.

## Backend (FastAPI)

1.  **Navigate to the `backend` directory:**
    ```bash
    cd backend
    ```
2.  **Create a virtual environment:**
    ```bash
    python -m venv venv
    ```
3.  **Activate the virtual environment:**
    -   **Windows:**
        ```bash
        venv\Scripts\activate
        ```
    -   **macOS/Linux:**
        ```bash
        source venv/bin/activate
        ```
4.  **Install dependencies:**
    ```bash
    pip install -r requirements.txt
    ```
5.  **Run the development server:**
    ```bash
    uvicorn main:app --reload
    ```
    The API will be available at `http://localhost:8000`.

## Deployment

The book will be deployed to GitHub Pages using Docusaurus's deployment command. The backend will need to be deployed separately. [NEEDS CLARIFICATION: Backend deployment strategy].
