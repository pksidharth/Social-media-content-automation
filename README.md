# AI-Powered Social Media Content Automation

An automated social media content generation workflow built using **n8n, Google Gemini, Google Sheets, and LinkedIn**.

## Project Overview

This project automates the process of converting news article links into AI-generated social media content.

It retrieves article URLs from Google Sheets, generates article summaries using Google Gemini, creates professional LinkedIn posts, and publishes the generated content through LinkedIn.

## Features

- Retrieves article URLs from Google Sheets.
- Generates article summaries using Google Gemini.
- Identifies key insights and actionable takeaways.
- Generates professional LinkedIn post content.
- Publishes generated posts to LinkedIn.
- Connects multiple services through an n8n workflow.

## Technology Stack

| Technology | Purpose |
|---|---|
| n8n | Workflow automation |
| Google Sheets | Article URL input |
| Google Gemini | AI summarization and content generation |
| LinkedIn | Social media publishing |
| OAuth 2.0 | Account authentication |

## Workflow Architecture

```text
Google Sheets Trigger
        |
        v
Basic LLM Chain
        |
        v
Google Gemini
        |
        v
Article Summary
        |
        v
Basic LLM Chain
        |
        v
LinkedIn Post Generation
        |
        v
LinkedIn Create Post
        |
        v
Published LinkedIn Post
```

## How It Works

1. Google Sheets Trigger retrieves an article URL.
2. The first Basic LLM Chain sends the prompt and article URL to Gemini.
3. Gemini generates a summary containing key insights, actionable advice, and implications.
4. The second Basic LLM Chain uses the summary to generate a professional LinkedIn post.
5. The LinkedIn node publishes the generated post.

## Setup Instructions

1. Import the workflow JSON into your n8n instance.
2. Configure your Google Sheets credentials.
3. Configure Google Gemini credentials.
4. Connect your LinkedIn account.
5. Select your Google Sheets document and configure the required fields.
6. Test the workflow and verify the generated content before publishing.

## Requirements

- An n8n account
- Google account with Google Sheets access
- Google Gemini API access
- LinkedIn account with the required permissions

## Security

- Credentials and access tokens should never be committed to GitHub.
- Configure your own credentials after importing the workflow.
- Review workflow exports before making repositories public.

## Project Status

Implemented and tested:

- Google Sheets integration
- AI-powered article summarization
- LinkedIn post generation
- LinkedIn publishing

## Author

**Sidharth**

GitHub: [pksidharth](https://github.com/pksidharth)
