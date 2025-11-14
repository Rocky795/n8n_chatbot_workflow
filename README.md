# Hotel Food Ordering & FAQ Chatbot Automation (n8n Workflow)

## Overview
This project is an AI-driven hotel assistant built using n8n. It allows users to:
- Place food orders
- Check item availability based on live inventory
- Get answers to hotel FAQs
- Automatically record customer orders

The workflow integrates AI reasoning, Google Sheets as a backend database, and conversational memory to create an automated hotel support system.

## Features
- **AI Agent (Gemini-based):** Handles all user messages and applies rules such as only ordering items available in the inventory list.
- **Inventory Lookup:** Reads live data from the “Inventory” sheet and ensures orders are validated before processing.
- **FAQ Tool:** Retrieves pre-defined hotel FAQs from a Google Sheet.
- **Order Logging:** Automatically appends confirmed orders to the “Order” sheet with customer name, item, quantity, timestamp, and status.
- **Conversational Memory:** Maintains short-term context for smooth user interaction.
- **Webhook Chat Trigger:** Begins workflow whenever a new message is received.

## Tech Used
- **n8n Workflow Automation**
- **Google Gemini AI Model**
- **Google Sheets (Inventory, FAQ, Orders)**
- **n8n LangChain nodes**
- **Webhook-based chat trigger**

## Workflow Structure
1. User sends a message (Webhook trigger)
2. AI agent interprets message and uses tools:
   - Inventory lookup
   - FAQ lookup
   - Order logging
3. AI responds with:
   - Food availability status
   - FAQ answer
   - Order confirmation or rejection
4. Order details are appended to Google Sheets

## Requirements
- n8n installed locally or hosted
- Google Sheets API credentials
- Gemini API key (free tier supported)
- Google Sheets with:
  - Inventory sheet
  - FAQ sheet
  - Order sheet

## How to Use
1. Import the workflow JSON into n8n  
2. Set credentials:
   - Google Sheets OAuth2
   - Gemini API key  
3. Replace the Google Sheet IDs with your own  
4. Activate workflow
5. Send messages to the webhook URL to interact with the chatbot

## License
This project is open-source. Modify and use freely.
