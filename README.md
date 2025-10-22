DataDive Document Retrieval System

DataDive is a Streamlit-based application that enables users to interact with a conversational AI trained on PDF documents. By uploading PDF files, users can extract text content and ask questions that are answered using contextual understanding powered by Google’s Gemini AI.

🔗 Live Demo: Launch App

🎥 Demo Video: Watch on GitHub

🚀 Features

📄 Multi-PDF Upload – Upload and process multiple PDF files.

🧠 Contextual AI Chat – Ask questions based on document content.

🔍 Text Extraction – Automatically extracts and embeds text from uploaded PDFs.

💬 Chat Interface – Interact with an AI assistant through an easy-to-use chat UI.

⚙️ Getting Started with Docker
1. Set your API Key

Create a .env file with your Google API key
:

GOOGLE_API_KEY=your_api_key_here

2. Run with Docker Compose
docker compose up --build


The app will be accessible at:
👉 http://localhost:8501

☁️ Deploying to the Cloud

To deploy the app on a remote server:

Build the Docker Image:

docker build -t datadive-app .


If deploying to a platform with a different CPU architecture (e.g., Mac M1 to amd64 server):

docker build --platform=linux/amd64 -t datadive-app .


Push to Container Registry:

docker push myregistry.com/datadive-app


More on this: Docker’s Getting Started Guide

💻 Local Development
Requirements:

Python 3.10 or higher

Steps:

Clone the Repository:

git clone https://github.com/your-username/datadive-document-retrieval.git
cd datadive-document-retrieval


Install Dependencies:

pip install -r requirements.txt


Set API Key:

Create a .env file with:

GOOGLE_API_KEY=your_api_key_here


Run the App Locally:

streamlit run main.py


Upload PDFs & Start Chatting:

Use the sidebar to upload PDFs.

Click "Submit & Process" to begin chatting with your document-based AI assistant.

📁 Project Structure
datadive-document-retrieval/
├── app.py               # Main application script
├── .env                 # Environment variable file
├── requirements.txt     # Dependency list
├── README.md            # Project documentation

📦 Dependencies

PyPDF2 – PDF parsing and extraction

langchain – LLM orchestration

Streamlit – Web interface framework

google.generativeai – Access to Gemini model

dotenv – Environment variable management

🙏 Acknowledgments

Google Gemini
 – Conversational AI backbone.

Streamlit
 – Simplified UI for ML apps.
