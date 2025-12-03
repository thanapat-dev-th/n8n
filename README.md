# 🤖 n8n AI Agent with OpenAI + Memory + Google Sheets

This repository contains an **AI Agent Workflow built with n8n**,
integrating: - **OpenAI Chat Model** for natural language
understanding - **Memory** for conversation context - **Google Sheets**
as a real-world data source

It demonstrates a **production-ready Agentic AI Automation
Architecture** suitable for chatbots, data lookup systems, and
AI-powered business automation.

------------------------------------------------------------------------

## 🧠 System Overview

This workflow allows a user to send a chat message, which is then: 1.
Processed by an AI Agent 2. Understood using OpenAI LLM 3. Enhanced with
conversation Memory 4. Enriched with real-time data from Google Sheets
5. Returned back to the user as a natural-language response

------------------------------------------------------------------------

## 🏗 Architecture Diagram (Logical Flow)

    [User / Chat UI]
            │
            ▼
    [When Chat Message Received]
            │
            ▼
         [AI Agent]
       ┌─────┼──────────┐
       │     │          │
    [OpenAI] [Memory] [Google Sheets]
       │     │          │
       └─────┴──────────┘
            │
            ▼
     [AI Response to User]

------------------------------------------------------------------------

## 🔁 Workflow Execution Flow

1.  User sends a chat message
2.  n8n trigger receives the message
3.  AI Agent processes the input
4.  Agent:
    -   Reads conversation Memory
    -   Sends prompt to OpenAI
    -   Calls Google Sheets Tool if data is required
5.  OpenAI generates a response using:
    -   Current prompt
    -   Historical context
    -   Google Sheet data
6.  Response is sent back to the user
7.  Conversation is stored in Memory for future use

------------------------------------------------------------------------

## 🧩 Main Components

  -----------------------------------------------------------------------
  Component                      Description
  ------------------------------ ----------------------------------------
  **n8n**                        Workflow Orchestrator / Automation
                                 Engine

  **AI Agent Node**              Central controller of reasoning and tool
                                 usage

  **OpenAI Chat Model**          Natural language processing and response
                                 generation

  **Simple Memory**              Stores conversation context

  **Google Sheets Tool**         External real-world data source
  -----------------------------------------------------------------------

------------------------------------------------------------------------

## ✅ Key Features

-   Real-time conversational AI
-   Context-aware responses using Memory
-   External data integration via Google Sheets
-   Modular and scalable agent design
-   Production-ready architecture

------------------------------------------------------------------------

## 📦 Files in This Repository

    /workflow
      └── ai-agent-google-sheet.json
    README.md

------------------------------------------------------------------------

## 🚀 How to Use This Workflow

### 1. Import into n8n

1.  Download the JSON workflow file
2.  Open n8n
3.  Click **Import → Import from file**
4.  Select the JSON file
5.  Configure credentials:
    -   OpenAI API Key
    -   Google Sheets OAuth
6.  Activate the workflow

------------------------------------------------------------------------

### 2. Required Credentials

Make sure the following credentials are configured inside n8n:

-   OpenAI API Key
-   Google Sheets OAuth2

> ⚠️ Credentials are **not included** in this repository for security
> reasons.

------------------------------------------------------------------------

## 🧪 Example Use Cases

-   AI Chatbot with real-time data lookup
-   Customer support bot backed by Google Sheets
-   Internal knowledge assistant
-   Sales automation assistant
-   Data-driven conversational AI

------------------------------------------------------------------------

## 🔒 Security Note

-   Do NOT commit API keys or OAuth tokens to GitHub
-   Always use n8n Credentials Manager for secrets
-   Use environment variables for production deployment

------------------------------------------------------------------------

## 🛠 Recommended Production Enhancements

-   Error handling & fallback logic
-   Logging to database
-   Rate limiting
-   Authentication for webhook endpoints

------------------------------------------------------------------------

## 👨‍💻 Author

Created by **Thana Patanaverakit**\
AI Automation / Data & Network Engineer

------------------------------------------------------------------------

## 📜 License

This project is licensed under the MIT License.
