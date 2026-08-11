# 🤖 AI Email Assistant — Multimodal AI Email Automation

An AI-powered email assistant built with **n8n** that allows users to compose and send professional emails using either **text or voice messages**.

The system interprets the user's request, processes voice messages through speech-to-text transcription when necessary, uses an AI Agent to understand the instruction, identifies the intended recipient, drafts the email, sends it through Gmail, and provides confirmation to the user after successful delivery.

---

## 🚀 Project Overview

Traditional email workflows require users to manually open an email application, identify the recipient, compose the message, and send it.

This project automates that process using an **AI Agent and n8n workflow automation**.

Users can simply send a natural-language instruction such as:

> "Send an email to John telling him that our meeting has been moved to Friday."

Or use a voice message:

> 🎤 "Send an email to John and let him know I'll be available for the meeting on Friday afternoon."

The system processes the request and handles the email workflow automatically.

---

# ✨ Key Features

### 📝 Text-Based Email Requests

Users can provide instructions using natural language text.

Example:

```text
Send an email to Sarah telling her that the project meeting has been moved to 10 AM tomorrow.

Workflow Architecture
                         USER
                           │
                ┌──────────┴──────────┐
                │                     │
             TEXT MESSAGE        VOICE MESSAGE
                │                     │
                │                Audio Processing
                │                     │
                │                Transcription
                │                     │
                └──────────┬──────────┘
                           │
                           ▼
                      AI AGENT
                           │
                ┌──────────┴──────────┐
                │                     │
          MyContacts Tool       SendEmail Tool
                │                     │
                ▼                     ▼
        Find Recipient              Gmail
        Email Address            Email Delivery
                                      │
                                      ▼
                              Confirmation Message
                                      │
                                      ▼
                                    USER