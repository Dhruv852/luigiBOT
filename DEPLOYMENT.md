# Deployment Guide

This guide explains how to deploy the Gemini Chatbot to various cloud platforms.

## Prerequisites

1. A Google Cloud account with Gemini API access
2. Your Gemini API key
3. Git installed on your system
4. Node.js and npm installed

## General Deployment Steps

1. Clone the repository
2. Install dependencies:
   ```bash
   npm install
   ```
3. Set up environment variables:
   - Create a `.env` file in the root directory
   - Add your Gemini API key:
     ```
     GEMINI_API_KEY=your_api_key_here
     ```

## Deployment Options

### 1. Render

1. Create a new account on [Render](https://render.com)
2. Click "New +" and select "Web Service"
3. Connect your GitHub repository
4. Configure the service:
   - Name: gemini-chatbot
   - Environment: Node
   - Build Command: `npm install`
   - Start Command: `npm start`
5. Add environment variable:
   - Key: `GEMINI_API_KEY`
   - Value: Your Gemini API key
6. Click "Create Web Service"

### 2. Heroku

1. Install [Heroku CLI](https://devcenter.heroku.com/articles/heroku-cli)
2. Login to Heroku:
   ```bash
   heroku login
   ```
3. Create a new Heroku app:
   ```bash
   heroku create your-app-name
   ```
4. Set environment variables:
   ```bash
   heroku config:set GEMINI_API_KEY=your_api_key_here
   ```
5. Deploy the app:
   ```bash
   git push heroku main
   ```

### 3. Railway

1. Create an account on [Railway](https://railway.app)
2. Create a new project and connect your GitHub repository
3. Add environment variable:
   - GEMINI_API_KEY=your_api_key_here
4. Deploy the project

## Important Notes

1. Always keep your API key secure and never commit it to version control
2. Enable CORS only for your specific domain in production
3. Consider implementing rate limiting for production use
4. Monitor your API usage to stay within limits
5. Set up proper error handling and logging

## Troubleshooting

1. If the app fails to start, check:
   - Environment variables are properly set
   - All dependencies are installed
   - Port configuration is correct

2. For CORS issues:
   - Update the CORS configuration in `server.js` to allow your domain
   - Ensure your client-side URL matches the allowed origins

3. For API issues:
   - Verify your Gemini API key is valid
   - Check API usage limits
   - Monitor server logs for error messages