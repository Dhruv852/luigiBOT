# Gemini Chatbot

A modern web-based chatbot powered by Google's Gemini AI API.

## Features

- Clean and responsive user interface
- Real-time chat with Gemini AI
- Support for multi-line messages
- Mobile-friendly design

## Setup

1. Replace the API key in `script.js`:
   - Find the line `const API_KEY = 'YOUR_GEMINI_API_KEY';`
   - Replace `'YOUR_GEMINI_API_KEY'` with your actual Gemini API key

2. Open `index.html` in a web browser to start using the chatbot

## Usage

1. Type your message in the input box
2. Press Enter or click the Send button to send your message
3. Wait for the AI to respond
4. Continue the conversation as needed

## Security Note

For security reasons, in a production environment, you should:
1. Never expose your API key in the frontend code
2. Use environment variables or a backend server to handle API requests
3. Implement proper rate limiting and error handling

## Technologies Used

- HTML5
- CSS3
- JavaScript (ES6+)
- Google Gemini API 