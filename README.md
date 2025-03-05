# ChitChatScoop.com

## ChitChatScoop
ChitChatScoop is a Next.js application that uses ChatGPT (via OpenAI’s API) to transcribe and summarize both Twitch chat messages and live audio from a stream, providing viewers and streamers with a concise, real-time “scoop” on what’s happening.

## Table of Contents
- [Project Overview](#project-overview)
- [Key Features](#key-features)
- [Tech Stack](#tech-stack)
- [Getting Started](#getting-started)
- [Environment Variables & API Keys](#environment-variables--api-keys)
- [Contributing](#contributing)
- [License](#license)

## Project Overview
ChitChatScoop aims to:

- Capture live chat messages from Twitch (or other streaming platforms, eventually).
- Transcribe audio from the streamer’s mic/stream audio and process it with a speech-to-text service (this can be an external API or custom solution).
- Combine chat messages + transcriptions into a unified context.
- Use ChatGPT (OpenAI’s large language model) to generate concise, reader-friendly summaries at regular intervals.
- Provide a simple HTML/JS widget (or an embeddable URL) that streamers can integrate into OBS or any broadcasting software.

Ultimately, we want to make streams more accessible and engaging, so viewers can quickly catch up on the latest conversation or commentary without scrolling endlessly.

## Key Features
### Real-Time Summaries
- Summaries refresh based on a defined interval (e.g., every 1–5 minutes).

### Audio Transcription Integration
- Combine spoken words from the streamer with chat input for richer context.

### Next.js Frontend
- A user-facing web interface to configure and display summaries.
- Seamless server-side rendering and easy deployment.

### Powered by ChatGPT
- Leverages OpenAI’s GPT-3.5 (or latest) API for text summarization and optional advanced NLP features.

### Embeddable Widget
- A small overlay (using iframes or direct HTML/JS) that can be added to OBS or your website.

## Tech Stack
- **Frontend:** Next.js (React framework)
- **Backend:** Node.js (integrated into Next.js serverless routes)
- **AI Summarization:** OpenAI API (ChatGPT)
- **Optional Speech-to-Text:** External API of your choice (e.g., Google Cloud Speech-to-Text, AWS Transcribe, or Whisper API)

## Getting Started
### 1. Clone the Repository
```bash
git clone https://github.com/yourusername/chitchatscoop.git
cd chitchatscoop
```

### 2. Install Dependencies
```bash
npm install
```

### 3. Run the Development Server
```bash
npm run dev
```
By default, the app will be running at [http://localhost:3000](http://localhost:3000).

### 4. Testing (Optional: if you have a testing framework set up)
```bash
npm run test
```

## Environment Variables & API Keys
Each contributor is responsible for managing their own dev environment and API keys. Never commit your private keys or tokens to the repository. Instead, use a local `.env` file (which is listed in `.gitignore` by default) and add environment variables there.

In a typical Next.js app, you might have something like:
```bash
# .env (example)
OPENAI_API_KEY=your_openai_api_key_here
TWITCH_CLIENT_ID=your_twitch_client_id_here
TWITCH_CLIENT_SECRET=your_twitch_client_secret_here
SPEECH_TO_TEXT_API_KEY=optional_speech_api_key_here
```
When deployed, services like Vercel or Netlify have dedicated interfaces for storing these environment variables.

## Contributing
We love contributions! ChitChatScoop is a community project, and all development efforts—whether code, documentation, or design—are welcome.

### How to Contribute
1. Fork this repository.
2. Create a feature or bugfix branch (e.g., `feat/chat-transcription` or `fix/widget-style`).
3. Commit your changes, ensuring good commit messages.
4. Push to your fork and submit a Pull Request (PR) to our main repo.
5. Join our discussions in the Issues or contact us on Discord/Slack if you need guidance.

### Important
- Make sure to keep your local `.env` file private.
- We maintain a project board with open tasks/issues. Feel free to grab any “help wanted” or “good first issue.”

## License
This project is released under the MIT License. You are free to use, modify, and distribute the code under the terms of this license.

---
ChitChatScoop is your one-stop solution to easily keep track of everything happening during a stream—chat messages, voice commentary, and more—summed up in a neat, digestible scoop for everyone to see. We appreciate all your support and contributions.

**Happy coding and summarizing!**
