# Flask API Integrating OpenAI GPT-3 and IBM Watson Services

## 📌 Description
This repository provides a Flask-based API that integrates **OpenAI's GPT-3** and **IBM Watson services** (Speech-to-Text and Text-to-Speech). The API enables:
- Converting speech to text.
- Generating text completions using OpenAI GPT-3.
- Converting text to speech.

<p align="center">
  <img src="./Flask-API-Integrating-OpenAI-GPT-3-and-IBM-Watson-Services.jpg - RMS Titanic Dataset.jpg" alt="Asistente de voz">
</p> 

## 🚀 Features
1. **Speech-to-Text**: Converts audio files in WAV format to text using IBM Watson's Speech-to-Text API.
2. **Ask GPT-3**: Generates intelligent text completions based on prompts using OpenAI's GPT-3.
3. **Text-to-Speech**: Converts text to audio using IBM Watson's Text-to-Speech API.

## 📂 Project Structure
- `app.py`: Main Flask application file.
- `template/` and `statics/`: Placeholder folders for frontend components if needed.
- `.env`: File to store API keys and configuration variables.
- `.gitignore`: To exclude sensitive files like `.env` from version control.
- `LICENSE`: License for the repository.

## 🛠 Prerequisites
1. **Python 3.7 or higher**
2. Install dependencies:
   ```bash
   pip install flask openai ibm-watson python-dotenv
   ```
3. Create a `.env` file with the following keys:
   ```env
   OPENAI_API_KEY=your_openai_api_key
   IBM_WATSON_API_KEY=your_ibm_watson_api_key
   IBM_WATSON_URL=your_ibm_watson_url
   ```

## 📦 Installation
1. Clone this repository:
   ```bash
   git clone <repository_url>
   cd <repository_folder>
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Start the Flask server:
   ```bash
   python app.py
   ```

## 📑 API Endpoints

### 1. Speech-to-Text
- **Endpoint**: `/speech-to-text`
- **Method**: `POST`
- **Payload**: Multipart form-data with an audio file (`audio` field).
- **Response**: JSON with the transcribed text.

### 2. Ask GPT-3
- **Endpoint**: `/ask-gpt3`
- **Method**: `POST`
- **Payload**: JSON with the following structure:
  ```json
  {
    "prompt": "Your question or prompt here"
  }
  ```
- **Response**: JSON with the GPT-3 completion.

### 3. Text-to-Speech
- **Endpoint**: `/text-to-speech`
- **Method**: `POST`
- **Payload**: JSON with the following structure:
  ```json
  {
    "text": "The text you want to convert to speech"
  }
  ```
- **Response**: Audio content in WAV format.

## 🛠 Technologies Used
- **Flask**: Python web framework.
- **OpenAI GPT-3**: Natural language generation.
- **IBM Watson**: Speech-to-Text and Text-to-Speech services.
- **dotenv**: Environment variable management.

## 🛡 Security
- Ensure sensitive API keys are stored in the `.env` file and not shared publicly.
- Use HTTPS for deploying the API in production.



