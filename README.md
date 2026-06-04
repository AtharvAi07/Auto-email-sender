# AI-Powered Auto Email Sender (n8n Workflow)

An automated, event-driven email response system built using **n8n**. The workflow dynamically detects incoming customer chats, processes the context using an OpenAI Chat Model with conversational memory, and automatically drafts or sends appropriate replies via Gmail.

This repository contains the exported JSON workflow architecture for replication and self-hosting.

## 🚀 Features

- **Instant Event Triggering:** Monitors and triggers immediately when a new chat interaction is detected.
- **Context-Aware AI Processing:** Leverages an **OpenAI Chat Model** combined with **Simple Memory** to maintain conversational context and deliver precise, human-like answers.
- **Automated Email Delivery:** Integrates natively with **Gmail** to execute the email delivery based on the AI's generated response.

## 🛠️ Tech Stack & Tools

- **Workflow Automation:** n8n
- **AI Integration:** OpenAI Node (Chat Model + Simple Memory)
- **Communication Tool:** Gmail API
- **Data Protocol:** JSON & Webhooks

## 📐 How It Works

1. **Trigger:** The workflow activates when a new chat event is detected.
2. **Context & Memory:** The OpenAI node pulls previous interaction data via the Simple Memory sub-node to understand the full user history.
3. **Generation:** The LLM constructs a professional response based on pre-configured system prompts.
4. **Action:** The **Gmail tool** takes the final output and sends/drafts the email directly to the recipient.

## 💻 Setup & Installation

1. Download the `auto-email-sender.json` file from this repository.
2. Open your n8n dashboard, click the top-right menu, and select **Import from File**.
3. Upload the `.json` file to restore the workflow canvas.
4. Configure your credentials for the **OpenAI** and **Gmail** nodes.
5. Click **Activate** to put the pipeline into production.
