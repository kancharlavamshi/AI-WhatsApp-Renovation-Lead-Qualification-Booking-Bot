# AI-WhatsApp-Renovation-Lead-Qualification-Booking-Bot
An AI-powered WhatsApp assistant built with n8n, Groq LLM, WhatsApp Cloud API, and Google Calendar that automatically qualifies renovation leads and schedules consultation calls.  This automation helps renovation businesses capture leads, understand project requirements, and book meetings automatically without manual coordination.

## Workflow Overview

The bot interacts with customers on WhatsApp, gathers project details, and schedules a consultation call once the required information is collected.

## Workflow Overview

```
WhatsApp Message
        ↓
Lead Qualification AI Agent (Groq)
        ↓
Conversation Memory
        ↓
Action Detection (JavaScript Parser)
        ↓
Decision Logic (Switch Node)
        ↓
Google Calendar Event Creation
        ↓
WhatsApp Confirmation Message
```


---

## Workflow Architecture

Below is the n8n workflow used in this project.

![Workflow Architecture](n8n_1.png)


---

## Features

### AI Lead Qualification

The bot collects key information from potential customers:

- Renovation project type
- Budget range
- Timeline / urgency
- Location

---

### Conversational AI

The bot asks **one question at a time** in a friendly WhatsApp style conversation.

---

### Smart Scheduling

When the user provides:

- email
- preferred date & time

The system automatically:

- converts natural language time
- creates a **30-minute consultation event**
- schedules it in **Google Calendar**

---

### WhatsApp Confirmation

After scheduling, the user receives confirmation directly on WhatsApp.

---

### Conversation Memory

The system remembers information provided across multiple messages.

Example interaction:

User: kitchen renovation
User: under 10k
User: India
User: krishna@email.com
User: 16 March 7pm


The AI combines this data to create the appointment.

---

## Technologies Used

| Tool | Purpose |
|-----|------|
| n8n | Workflow automation |
| Groq LLM | AI conversational agent |
| WhatsApp Cloud API | Messaging interface |
| Google Calendar API | Meeting scheduling |
| JavaScript (n8n Code Node) | Action parsing |
| Conversation Memory | Context management |

---

