# Emotion Detection AI - Python Flask IBM Watson API

This repository contains the source code for an Emotion Detection AI application built using Python, Flask, and the IBM Watson Tone Analyzer API. The app analyzes text input to detect emotions such as joy, sadness, anger, fear, and analytical tones, providing insights into the sentiment behind conversations or written content. It's ideal for applications in customer service, mental health monitoring, social media analysis, or any scenario where understanding emotional context is valuable.

## ✨ Features

- **Text Emotion Analysis**: Submit text via a web interface, and the app uses IBM Watson's Tone Analyzer to detect and score emotions in real-time.
- **User-Friendly Web Interface**: A simple Flask-based frontend for inputting text and viewing results, including visualized tone scores (e.g., bar charts for emotion probabilities).
- **API Endpoint**: Expose a RESTful API for integrating emotion detection into other applications.
- **Error Handling**: Graceful handling of invalid inputs, API errors, or network issues.
- **Logging and History**: Optional feature to log analyzed texts and results for review.
- **Secure API Integration**: Uses environment variables for storing IBM Watson credentials to ensure security.

## 🛠 Technology Stack

- **Backend Framework**: Python with Flask
- **AI Service**: IBM Watson Tone Analyzer API
- **Frontend**: HTML/CSS with Jinja2 templating (optional JavaScript for interactivity)
- **Data Visualization**: Matplotlib or Chart.js for displaying emotion scores
- **Environment Management**: Virtualenv or Pipenv
- **Other Libraries**: Requests for API calls, JSON for data handling

## 🚀 Getting Started

### Prerequisites

- Python 3.8+
- IBM Cloud account with access to Watson Tone Analyzer (free tier available)
- Flask and other dependencies (listed in `requirements.txt`)
- API key and URL from IBM Watson Tone Analyzer service

### Installation

1. Clone the repository:

   ```
   git clone https://github.com/your-org/emotion-detection-ai-python-flask-ibm-watson.git
   cd emotion-detection-ai-python-flask-ibm-watson
   ```

2. Set up a virtual environment:

   ```
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. Install dependencies:

   ```
   pip install -r requirements.txt
   ```

4. Configure Environment Variables:  
   Create a `.env` file in the root directory and add your IBM Watson credentials:

   ```
   WATSON_API_KEY=your_api_key_here
   WATSON_URL=https://api.us-south.tone-analyzer.watson.cloud.ibm.com
   ```

5. Run the Application:  
   Start the Flask server.

   ```
   flask run
   ```

   The app will be accessible at http://127.0.0.1:5000.

## 📝 Usage Guide

1. **Access the Web Interface**: Open your browser and navigate to the root URL (e.g., http://127.0.0.1:5000). You'll see a form to input text.
2. **Submit Text for Analysis**: Enter a sentence or paragraph and click "Analyze". The app will call the IBM Watson Tone Analyzer API and display detected emotions with scores.
3. **API Usage**: Send a POST request to `/analyze` with JSON payload `{ "text": "Your text here" }`. Response will include JSON with tones and scores.
4. **View Results**: Emotions are categorized (e.g., Anger: 0.75, Joy: 0.12) and visualized for easy interpretation.
5. **Customization**: Modify the `app.py` file to adjust thresholds, add more features, or integrate with other services.

## 🔒 Security Notes

- Never hardcode API keys in your code—always use environment variables or a secure vault.
- The app uses HTTPS for IBM Watson API calls to ensure data privacy.
- For production, implement authentication (e.g., via Flask-Login) to restrict access.

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙌 Acknowledgments

- Inspired by tutorials on IBM Watson Tone Analyzer integration.
- Example projects like those on GitHub for Flask-based AI apps.
