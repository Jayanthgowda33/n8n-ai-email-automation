# AI Email Classification & Automation using n8n

An AI-powered email automation workflow built using **n8n** and **Groq LLM**. The workflow analyzes incoming emails, classifies them into predefined categories, determines their priority, and decides whether a response should be sent.

## 🚀 Features

* Automatically processes incoming emails
* Uses an LLM to classify emails
* Categorizes emails as:

  * Urgent
  * Spam
  * Meeting
  * Support
  * Personal
* Assigns priority:

  * High
  * Medium
  * Low
* Automatically determines whether a reply should be sent
* Uses JavaScript logic inside n8n
* Returns structured JSON output
* Can be extended to automatically send email responses

## 🛠️ Technologies Used

* n8n
* Groq API
* LLM
* JavaScript
* REST API
* JSON
* Email automation

## 🔄 Workflow

```text
Incoming Email
      ↓
Extract Subject & Body
      ↓
HTTP Request
      ↓
Groq LLM
      ↓
Email Classification
      ↓
JavaScript Logic
      ↓
Reply = true / false
      ↓
Send Reply / Skip
```

## 🧠 Classification Logic

The AI classifies emails into five categories:

| Category | Description                                    |
| -------- | ---------------------------------------------- |
| Urgent   | Important emails requiring immediate attention |
| Spam     | Unwanted or suspicious emails                  |
| Meeting  | Meeting invitations or scheduling emails       |
| Support  | Customer or technical support requests         |
| Personal | Personal/non-business communication            |

## 📊 Example Output

```json
{
  "category": "support",
  "priority": "High",
  "reply": true
}
```

For spam:

```json
{
  "category": "spam",
  "priority": "Low",
  "reply": false
}
```

## ⚙️ Setup

1. Install or create an n8n instance.
2. Import the workflow JSON from the `workflow` folder.
3. Configure your email credentials.
4. Add your Groq API credentials.
5. Update the required environment/configuration values.
6. Activate the workflow.

## 🔐 Security

API keys, credentials, passwords, and other sensitive information are **not included** in this repository.

Create your own API credentials and configure them inside n8n.

## 📸 Screenshots

Screenshots of the n8n workflow and execution results are available in the `screenshots` folder.

## 🎯 Future Improvements

* Add automatic email reply generation
* Add Gmail/Outlook integration
* Store classified emails in PostgreSQL
* Add an email dashboard
* Add confidence scoring
* Add logging and error handling
* Add Slack/WhatsApp notifications

## 👨‍💻 Author

Jayanth Gowda

MCA Graduate | Python | Full Stack | AI/GenAI | Automation
