

---

# 📄 My Workflow

This repository contains an **n8n workflow** integrating a conversational AI agent with Google Sheets to manage and update inventory records.

---

## ✨ Features

✅ Responds to chat messages in real time
✅ Uses **Google Gemini** (PaLM) for natural language processing
✅ Maintains conversation context with memory buffer
✅ Searches inventory in a Google Sheet
✅ Updates inventory records automatically

---

## 🛠️ Workflow Overview

The workflow includes these main components:

1. **Chat Trigger**
   Listens for incoming chat messages to start the workflow.

2. **AI Agent Node**
   Orchestrates AI actions (language model and tools).

3. **Google Gemini Chat Model**
   Provides conversational responses and understands user queries.

4. **Simple Memory Buffer**
   Keeps context over the last 10 messages.

5. **Google Sheets Tool – Search Inventory**
   Searches the connected Google Sheet to find inventory data.

6. **Google Sheets Tool – Update Inventory**
   Appends or updates inventory entries based on AI instructions.

---

## 🧩 Connections

| From                     | To       | Purpose                                  |
| ------------------------ | -------- | ---------------------------------------- |
| Chat Trigger             | AI Agent | Starts processing when a message arrives |
| Google Gemini Chat Model | AI Agent | Supplies language understanding          |
| Simple Memory            | AI Agent | Retains chat context                     |
| Search Inventory         | AI Agent | Enables searching inventory records      |
| Update Inventory         | AI Agent | Updates records as needed                |

---

## ⚙️ Configuration

To use this workflow:

1. **Google Sheets Credentials**

   * Make sure you set up OAuth credentials for Google Sheets.
   * The workflow references a specific spreadsheet:

     * **Document ID:**
       `1Oqh96aWsTW83OQHJzPvntXr0pSRU0Av602HS3JkN43Q`
     * **Sheet Name:**
       `Sheet1`

2. **Google Gemini API Credentials**

   * Configure your Google Gemini (PaLM) API credentials.

3. **Webhook URL**

   * The chat trigger uses a webhook ID. You may need to register this endpoint with your chat provider.

---

## 🔍 Example Use Case

A user sends a chat message like:

> "What is the quantity of item *Widget A*?"

The workflow:

* Processes the message via Gemini,
* Searches the Google Sheet for *Widget A*,
* Replies with the current stock.

If the user says:

> "Update Widget A quantity to 50."

The workflow updates the row in Google Sheets automatically.

---

## 🚀 How to Deploy

1. Import `My workflow.json` into your n8n instance.
2. Configure all necessary credentials.
3. Activate the workflow.
4. Start interacting via the chat trigger.

---

## 📂 File Structure

```
My workflow.json         # The workflow definition
README.md                # This documentation
```

---

## 📝 License

This project is provided for educational and internal use. Make sure you comply with the terms of your chat and Google APIs.

---

