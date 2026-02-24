# 🤖 AI-Powered Data Lookup & Automation Agent (n8n)

## 🖼️ Workflow Overview
![Workflow Overview](n8nworkflow-overview.png)

---

## 📘 Overview
Built an AI-powered automation workflow that allows users to query structured contact data using natural language and automatically trigger follow-up actions such as **email delivery** and **calendar scheduling**.

This project demonstrates how conversational AI can be safely integrated into **business workflows** by combining large language models with structured data sources—without exposing or inferring real-world personal information.

---

## 🧠 Business Problem Solved
Manual lookup of contact information and follow-up actions (emails, meetings) is time-consuming and error-prone.

This workflow replaces manual steps with an AI-assisted system that:
- Interprets user requests
- Retrieves the correct contact from a structured dataset
- Automatically executes downstream actions

---

## 🔄 Workflow Architecture (High Level)
**Natural Language → Verified Data → Automated Action**

1. User submits a natural-language request  
2. AI agent extracts intent and target record  
3. Google Sheets is queried as the single source of truth  
4. Validated contact data is returned  
5. Automation triggers:
   - 📧 Email sent to the selected contact  
   - 📅 Calendar event created  

---

## 🧹 Data Source & Handling
**Data Source:**  
Structured Google Sheet containing names, emails, and row identifiers.

**Data Controls Implemented:**
- Enforced strict schema alignment to ensure consistent lookups  
- Used deterministic row matching to prevent incorrect results  
- Restricted AI responses to tool-provided data only  
- Prevented real-world data inference through prompt constraints  

---

## 🤖 AI & Automation Implementation

### Large Language Model Integration
- Integrated Groq Chat Model via API  
- Designed prompts to:
  - Extract user intent  
  - Match structured records accurately  
  - Return controlled, predictable outputs  

### AI Agent Design
- Built a modular AI agent workflow that:
  - Separates reasoning from execution  
  - Uses automation tools (Sheets, Email, Calendar) deterministically  
  - Includes guardrails for error handling and safe responses  

---

## 🔔 Automated Capabilities

### ✅ Contact Lookup
- Matches natural-language requests to structured contact records  
- Returns validated email data only when a match exists  

### 📧 Email Automation
- Automatically sends emails using retrieved contact information  
- Reduces manual follow-up and lookup time  

### 📅 Calendar Scheduling
- Creates calendar events based on AI-interpreted requests  
- Enables scheduling through conversational input  

---

## 📊 Key Outcomes
- Demonstrates safe AI adoption in operational workflows  
- Reduces manual data lookup and follow-up steps  
- Bridges conversational interfaces with structured business data  
- Designed with production-style controls, not experimental shortcuts  

---

## 🛠️ Tools & Technologies
- n8n — Workflow automation and orchestration  
- Groq API — Large language model inference  
- Google Sheets — Structured data source  
- Email API — Automated communication  
- Calendar API — Event scheduling  
- GitHub — Version control and documentation  

---

## 📈 Skills Demonstrated
- AI-assisted workflow automation  
- Prompt engineering for controlled AI behavior  
- API integration and orchestration  
- Data validation and safety controls  
- Event-driven system design  
- Technical documentation for business use cases  
