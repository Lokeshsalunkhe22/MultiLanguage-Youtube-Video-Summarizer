# MultiLanguage-Youtube-Video-Summarizer

## 📝 Overview

This web application enables users to generate concise summaries of YouTube video transcripts. Users can input a video URL, specify the minimum summary length, and choose a preferred language for the summary. The application utilizes advanced natural language processing techniques to retrieve, translate, and summarize transcripts.

## ✨ Features

- 🔗 **Input YouTube Video URL**: Easily input the URL of the YouTube video you wish to summarize.
- ✂️ **Customizable Summary Length**: Specify the desired minimum length of the summary.
- 🌐 **Language Selection**: Choose the language for the output summary.
- 🎥 **Multilingual Transcript Retrieval and Translation**: Utilize the YouTube Transcript API and Google Translator liabrary for multilingual support.
- 🧠 **Advanced Summarization**: Generate summaries using fine-tuned BART models.
- 📷 **Visual Output**: Display the summarized text along with the video thumbnail.

## 🛠️ Technology Stack

- **Frontend**: HTML, CSS, JavaScript
- **Backend**: Flask
- **APIs**: YouTube Transcript API
- **NLP Models**: Hugging Face Transformers (BART models including "facebook/bart-large-cnn" and a fine-tuned model on the SAMSum dataset)

## 📚 Methodology

### 🌟 User Interface (HTML/CSS/JS)
The interface allows users to input the YouTube video URL, specify the summary length, and select the language. It provides a smooth user experience with real-time feedback and input validation.

### 🔧 Flask Application
Flask manages routing, data processing, and API integrations, coordinating the entire flow from user input to the final output presentation.

### 📥 Data Retrieval
Fetches transcripts in multiple languages using the YouTube Transcript API, providing a rich dataset for analysis.

### 🌐 Translation
Translates transcripts into the user's preferred language via the Google Translate API if they are not originally in English.

### 🛠️ Text Processing and Chunk Creation
Preprocesses the transcript text and segments it into manageable chunks for effective summarization.

### 🧩 Summarization Models
- **Fine-Tuned BART Model**: Specifically Pre-trained on the SAMSum dataset for domain-specific summaries.
- **"facebook/bart-large-cnn" Model**: Generates high-quality, coherent summaries across various topics.

### 📊 Output Presentation
Displays the summarized text and video thumbnail, providing users with a clear and concise representation of the video's content.

## 🚀 How to Run

1. Clone the repository:
2. Train the Model Using Google Colab:
3. Set Up Local Environment:
     `python -m venv venv
      source venv/bin/activate`
5. Install dependencies:
     `pip install -r requirements.txt`
7. Run the Flask application:
     `flask run -p 5001`
9. Open your browser and go to
     `http://127.0.0.1:5000/`

### 🌍 Deployment on AWS

This application is deployed on AWS using an EC2 instance for scalability and reliability. Here’s the process:

**EC2 Instance Setup:**
- Launched an EC2 instance with the necessary configuration and Amazon Machine Image (AMI) for Flask.
- Configured security groups to allow HTTP/HTTPS traffic.

**Environment Setup:**
- Connected to the EC2 instance using PuTTY for SSH access.
- Installed Python, Flask, and all required dependencies using `requirements.txt`.

**Application Deployment:**
- Uploaded the project files to the EC2 instance using WinSCP.
- Set up the Flask application to run on a specific port.

![Screenshot 2024-04-28 200147](https://github.com/user-attachments/assets/776301be-d1d5-4efa-8c1e-13fc6dd04080)


