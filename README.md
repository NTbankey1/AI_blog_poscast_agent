# Blog-to-Podcast AI

A Streamlit-based AI application that transforms any public blog post into a podcast episode.

Simply provide a blog URL, and the application will scrape the article, generate an engaging summary using OpenAI, and convert the result into natural-sounding speech with ElevenLabs.

## Features

- **Blog Content Extraction**  
  Scrapes the content of public blog posts using the Firecrawl API.

- **AI-Powered Summarization**  
  Uses OpenAI GPT-4 to transform the extracted article into a concise and engaging podcast script of up to 2,000 characters.

- **Text-to-Speech Podcast Generation**  
  Converts the generated script into natural-sounding audio using the ElevenLabs API.

- **Simple Streamlit Interface**  
  Provides an easy-to-use web interface where users can enter a blog URL and generate a podcast with a single click.

- **Secure API Key Input**  
  API keys are entered through the Streamlit sidebar and are not hard-coded into the application.

## How It Works

The application follows a simple pipeline:

```text
Blog URL
   ↓
Firecrawl
   ↓
Extract Article Content
   ↓
OpenAI GPT-4
   ↓
Generate Podcast Script
   ↓
ElevenLabs
   ↓
Generate Audio
   ↓
Listen / Download Podcast
```

## Requirements

Before running the application, make sure you have:

- Python 3.8 or newer
- An OpenAI API key
- An ElevenLabs API key
- A Firecrawl API key

### API Keys

You will need API keys from the following services:

- **OpenAI** — used for generating the podcast script.
- **Firecrawl** — used for extracting content from blog URLs.
- **ElevenLabs** — used for text-to-speech generation.

## Installation

### 1. Clone the Repository

```bash
git clone https://github.com/Shubhamsaboo/awesome-llm-apps.git
cd awesome-llm-apps/starter_ai_agents/ai_blog_to_podcast_agent
```

### 2. Install Dependencies

Create a virtual environment if desired:

```bash
python -m venv .venv
source .venv/bin/activate
```

Then install the required packages:

```bash
pip install -r requirements.txt
```

## Running the Application

Start the Streamlit application:

```bash
streamlit run blog_to_podcast_agent.py
```

Streamlit will provide a local URL that you can open in your browser.

## Usage

1. Open the Streamlit application.
2. Enter your **OpenAI API key** in the sidebar.
3. Enter your **ElevenLabs API key**.
4. Enter your **Firecrawl API key**.
5. Paste the URL of the blog post you want to convert.
6. Click **Generate Podcast**.
7. Wait for the article to be scraped, summarized, and converted into audio.
8. Listen to the generated podcast directly in the application.
9. Download the generated audio if you want to save it locally.

## Example Workflow

```text
https://example.com/blog-post
          │
          ▼
   Extract blog content
          │
          ▼
   Generate AI summary
          │
          ▼
   Create podcast script
          │
          ▼
   Generate AI voice
          │
          ▼
      🎙️ Podcast
```

## Notes

The application requires valid API keys for all three services. API usage may incur costs depending on the pricing and usage limits of OpenAI, Firecrawl, and ElevenLabs.

The application works best with publicly accessible blog posts that contain clearly structured article content.
