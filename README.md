# YouTube Video Summarizer

This is a web application that automatically generates a text summary of any YouTube video. Users can simply paste a YouTube video URL, and the app will extract the video's transcript, process the text, and present a concise summary.

The application is built with a **Flask** backend, uses **NLTK** for natural language processing, and is designed for easy deployment on cloud platforms like Heroku.

## Features

* **YouTube Transcript Extraction:** Automatically pulls the closed captions/transcript from a YouTube video.
* **NLP Text Summarization:** Uses NLTK (Natural Language Toolkit) to process the raw text and generate an extractive summary.
* **Web Interface:** A simple and clean UI built with Flask and HTML/CSS for pasting the URL and viewing the summary.
* **Deployment Ready:** Includes a `Procfile`, `requirements.txt`, and `runtime.txt` for easy deployment.

## Technology Stack

* **Backend:** Python, Flask
* **NLP:** NLTK
* **YouTube API:** `youtube_transcript_api`
* **Frontend:** HTML, CSS, JavaScript (in `static`/`templates`)
* **Deployment:** Gunicorn (as per `Procfile`)

## How to Run This Project Locally

### 1. Clone the Repository

```bash
git clone [https://github.com/robisuresh8/Youtube-Video-Summarizer.git](https://github.com/robisuresh8/Youtube-Video-Summarizer.git)
cd Youtube-Video-Summarizer
```

### 2. Create a Virtual Environment

It's highly recommended to use a virtual environment to manage dependencies.

```bash
# Create a virtual environment
python -m venv venv

# Activate it
# On Windows:
venv\Scripts\activate
# On macOS/Linux:
source venv/bin/activate
```

### 3. Install Dependencies

Install all the required Python packages using the `requirements.txt` file.

```bash
pip install -r requirements.txt
```

The app also requires NLTK data. The `nltk.txt` file indicates it needs `punkt` and `stopwords`. You can download these by running:

```bash
python -m nltk.downloader punkt stopwords
```

### 4. Run the Flask Application

Once the dependencies are installed, you can start the Flask development server.

```bash
python app.py
```

### 5. View in Browser

Open your web browser and navigate to the following address:

`http://127.0.0.1:5000`

You can now paste a YouTube URL and test the summarizer.
