# AI Marketing Emailer

[GitHub Repository](https://github.com/aungkaungpyaepaing/ai-marketing-emailer)

---

## Overview

This project is an AI-powered marketing email generator and sender that uses multiple specialized OpenAI agents with distinct personalities to create different versions of a marketing email. The system evaluates these versions, selects the most emotionally engaging one, converts it into a polished HTML email, and sends it out via SendGrid.

The goal is to automate personalized, persuasive, and engaging marketing emails tailored to different brand voices and tones.

---

## Features

- **Multiple AI Agents** with different copywriting styles:
  - Sales-focused copywriter emphasizing benefits and urgency
  - Story-driven brand voice crafting engaging narratives
  - Funny/informal tone using humor and casual language

- **Marketing Manager Agent** that evaluates all generated email versions and selects the best one to send.

- **Email Subject Writer** to craft compelling subject lines.

- **HTML Email Converter** to transform plain text emails into professional HTML format with styling, CTA buttons, and emojis.

- **SendGrid Integration** for reliable email delivery.

- Asynchronous execution with Python's `asyncio`.

---

## Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/aungkaungpyaepaing/ai-marketing-emailer.git
   cd ai-marketing-emailer


2. Create and activate a Python virtual environment:

  ```bash
  python3 -m venv venv
  source venv/bin/activate   # Linux/macOS
  venv\Scripts\activate      # Windows
  ```


3. Install dependencies:
```bash
  pip install -r requirements.txt
```


4. Create a .env file with your environment variables, e.g.:
```bash
SENDGRID_API_KEY=your_sendgrid_api_key_here
OPENAI_API_KEY=your_openai_api_key_here
```

## Usage

Run the main script (e.g., main.py) to generate and send a marketing email about the MovieJoys subscription (a movie website) to new users.

The system will:

- Generate multiple email drafts using different agent personalities.

- Select the most emotionally engaging draft.

- Write a compelling subject line.

- Convert the plain text email to a polished HTML email.

- Send the email via SendGrid.

## Example Output

<img width="1384" alt="image" src="https://github.com/user-attachments/assets/246f1182-ac22-4e93-9238-b21c80cb78ae" />

## Code Structure Highlights


Agent: Defines specialized AI agents with specific instructions.

Runner: Runs agents asynchronously and manages outputs.

function_tool: Decorator to wrap email sending functions as callable tools.

SendGrid integration for sending emails securely.

Multi-agent workflow for generating, selecting, converting, and sending emails.

## Author

Aung Kaung Pyae Paing
