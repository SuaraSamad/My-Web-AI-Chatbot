Personal AI Chat Assistant

This project implements a personalized AI chatbot that represents Abdulsamad Suara. It is designed to answer questions about his career, background, skills, and experience. The system uses OpenAI’s Chat Completions API, Pushover notifications, and integrates with Gradio to provide a simple web chat interface.

✨ Features

AI-powered chatbot trained on your resume, profile, and personal summary.

Tool integration:

Records user details (email, name, notes).

Records unknown/unanswered questions.

Sends push notifications via Pushover.

PDF + Text ingestion:

Reads data from Samad_Suara_Resume.pdf, Profile.pdf, and summary.txt.

Gradio chat interface for simple deployment and interaction.

📂 Project Structure
.
├── me/
│   ├── Samad_Suara_Resume.pdf   # Your resume
│   ├── Profile.pdf              # Your profile
│   ├── summary.txt              # Concise career summary
├── app.py                       # Main application (AI chatbot logic)
├── requirements.txt             # Python dependencies
└── README.md                    # Project documentation

⚙️ Requirements

Python 3.9+

OpenAI API key

Pushover account & API credentials

🔑 Environment Variables

Create a .env file in your project root with the following values:

OPENAI_API_KEY=your_openai_api_key
PUSHOVER_TOKEN=your_pushover_app_token
PUSHOVER_USER=your_pushover_user_key

📦 Installation

Clone the repository

git clone https://github.com/yourusername/ai-chat-assistant.git
cd ai-chat-assistant


Create a virtual environment (optional but recommended)

python -m venv venv
source venv/bin/activate   # On Mac/Linux
venv\Scripts\activate      # On Windows


Install dependencies

pip install -r requirements.txt

🚀 Usage

Run the chatbot with:

python app.py


Then open the Gradio interface in your browser (usually at http://127.0.0.1:7860).

🛠 How It Works

Initialization:

Loads personal data from resume, profile, and summary.

Builds a system prompt with context about Abdulsamad Suara.

Chatting:

Users send messages via the Gradio UI.

The chatbot responds using OpenAI’s chat.completions API.

Tools:

If the user provides contact info → record_user_details is called.

If the chatbot doesn’t know an answer → record_unknown_question is called.

Both send push notifications via Pushover.

🧰 Dependencies

openai

python-dotenv

pypdf

requests

gradio

📌 Notes

This app is personalized to Abdulsamad Suara but can be adapted by replacing resume/profile/summary files and updating the name in Me class.

Make sure .env and me/ folder files are correctly set up before launching.

📜 License

This project is for personal/professional use. You may adapt it for your own personal assistant use case.
