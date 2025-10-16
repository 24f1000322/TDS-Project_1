# TDS-Project_1
# GitHub Pages Deployer API

A FastAPI-based service that automatically creates GitHub repositories, generates web applications using Google's Gemini AI, and deploys them to GitHub Pages.

## Features

- 🤖 **AI-Powered Code Generation**: Uses Google Gemini to generate complete web applications based on task briefs
- 🚀 **Automated Deployment**: Automatically creates GitHub repos and enables GitHub Pages
- 🔄 **Two-Round System**: Supports initial deployment (Round 1) and updates (Round 2)
- 📝 **Smart File Management**: Generates both application code and documentation
- 🔐 **Secure**: Protected with secret-based authentication

## Prerequisites

- Python 3.11+
- GitHub Account with Personal Access Token
- Google Gemini API Key
- Render Account (for deployment)

## Environment Variables

Create a `.env` file in the project root with the following variables:

```env
GITHUB_TOKEN=your_github_personal_access_token
GITHUB_USERNAME=your_github_username
GOOGLE_API_KEY=your_google_gemini_api_key
SECRET=your_secret_key_for_authentication
```

### Getting Your API Keys

1. **GitHub Token**: 
   - Go to GitHub Settings → Developer settings → Personal access tokens → Tokens (classic)
   - Generate new token with `repo` scope
   - Copy and save the token

2. **Google Gemini API Key**:
   - Visit [Google AI Studio](https://makersuite.google.com/app/apikey)
   - Create or select a project
   - Generate API key

3. **Secret Key**: 
   - Create a strong random string for authentication
   - Example: `openssl rand -hex 32`

## Local Installation

1. **Clone the repository**
```bash
git clone <your-repo-url>
cd <your-repo-name>
```

2. **Install dependencies**
```bash
pip install -r requirements.txt
```

3. **Set up environment variables**
```bash
cp .env.example .env
# Edit .env with your actual credentials
```

4. **Run the application**
```bash
python main.py
```

The API will be available at `http://localhost:8000`


