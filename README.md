# RAG-Question-Answer

This is my RAG-Question-Answer project.
In file RAG.ipnyb, we can input a pdf file or text file and ask questions about that file.
In file chatbot.ipynb, we can make a chatbot based on RAG.

## Installation

**Clone the repository**:
    ```sh
    git clone https://github.com/trhuuloc/RAG-Question-Answer
    cd RAG-Question-Answer
    ```

## Local deployment

**Run the application:**
```sh
chainlit run app.py
```

**Interact with the chatbot:**
- Upload a PDF file or text file.
- Ask questions about the content in the uploaded file.

## Public deployment

1. **Register for an ngrok account**:
    - Go to [ngrok](https://ngrok.com/) and sign up for an account.

2. **Authentication Token**:
    - After registering, get your authentication token from the ngrok dashboard.

3. **Install and Authenticate Ngrok**:
    ```sh
    pip install -q ngrok
    ngrok config add-authtoken YOUR_AUTH_TOKEN
    ```

4. **Establish a Tunnel**:
    ```python
    public_url = ngrok.connect(8000).public_url
    print(public_url)
    ```

5. **Launch the Chatbot**:
    ```sh
    chainlit run app.py 
    ```

6. **Access the Chatbot**:

    Navigate to the provided ngrok URL to interact with your chatbot remotely.