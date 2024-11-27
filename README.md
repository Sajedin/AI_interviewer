AI-Powered Interview Assistant
Overview
The AI-Powered Interview Assistant is an advanced tool designed to:

Generate interview questions based on a resume.
Record audio and video answers to questions.
Transcribe audio answers into text.
Convert text to speech for seamless interaction.
This project integrates various functionalities using modern AI models and Python libraries, enabling automated and efficient interview simulation and analysis.

Features
Resume Parsing: Extracts information from resumes in PDF format.
Question Generation: Creates specific interview questions tailored to roles, leveraging AI models.
Audio and Video Recording: Captures candidate responses.
Transcription: Converts recorded audio to text using Whisper AI.
Text-to-Speech: Reads questions aloud using Google TTS.
Interactive Workflow: Allows dynamic control of recordings through keyboard inputs.
Installation
Clone this repository:

bash
Copy code
git clone <repository_url>
cd <repository_folder>
Install dependencies:

bash
Copy code
pip install -r requirements.txt
Set up environment variables:

Create a .env file in the root directory:
env
Copy code
GROQ_API_KEY=your_groq_api_key
Replace your_groq_api_key with your Groq API key.
Ensure a functional webcam and microphone are connected for video and audio recording.

File Structure
plaintext
Copy code
project/
├── transcription_module.py       # Handles audio/video recording and transcription
├── speech_module.py              # Converts text to speech and plays audio
├── ques_genera.py                # Generates interview questions from resume
├── final.py                      # Orchestrates the question-answer workflow
├── main.py                       # Entry point for the application
├── requirements.txt              # Lists required Python libraries
├── .env.example                  # Example of environment variables
└── output/                       # Stores recorded files and transcription
Usage
Prepare Your Resume: Save your resume as a .pdf file.

Generate Questions: Run main.py to extract questions based on your resume:

bash
Copy code
python main.py
Record Answers: The system will:

Read questions aloud.
Record your audio and video responses.
Transcribe your answers.
View Results:

All recordings and transcriptions are saved in the output/ directory.
JSON files with transcriptions can be used for further analysis.
Dependencies
Audio/Video Handling:

sounddevice
numpy
scipy
opencv-python
Natural Language Processing:

transformers
faster-whisper
groq
Utilities:

python-dotenv
pdfplumber
gtts
pygame
Install these dependencies via the provided requirements.txt.

Example Workflow
Resume Input: Upload a PDF of your resume.

Question Generation: Tailored questions like:

json
Copy code
[
    {
        "question": "Can you explain your project on AI development?",
        "answer": "..."
    }
]
Recording and Transcription:

The system asks, "Can you explain your project on AI development?"
You record your audio/video response.
Transcription is saved as:
json
Copy code
[
    {
        "start": 0.0,
        "end": 10.0,
        "text": "My project was focused on..."
    }
]
Output:

Audio: output/answer_0.wav
Video: output/answer_0.avi
Transcription: output/answer_0.json
Contributing
We welcome contributions to enhance this project! To contribute:

Fork the repository.
Create a feature branch: git checkout -b feature-name.
Commit changes: git commit -m "Add feature description".
Push to the branch: git push origin feature-name.
Open a pull request.
License
This project is licensed under the MIT License. See LICENSE for details.

Acknowledgments
This project uses:

Whisper AI
Google TTS
Groq API
