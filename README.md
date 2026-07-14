# AI Lead Generation & Business Research Automation

> An AI-powered lead generation workflow built with **n8n** that discovers businesses from Google Maps, researches each company using AI, identifies automation opportunities and pain points, and automatically stores qualified leads in Google Sheets.

---

## 📖 Overview

Finding high-quality leads manually is time-consuming. A typical workflow involves:

- Searching businesses on Google Maps
- Opening each website individually
- Researching what the company does
- Identifying potential business problems
- Determining whether AI automation can help
- Copying all the information into a spreadsheet

This workflow automates the entire process.

Users simply enter:

- Industry
- Country
- Number of Leads

The workflow then searches for businesses, researches each company using AI, analyzes automation opportunities, and saves structured results into Google Sheets.

---

# ✨ Features

- Dynamic lead search by industry and country
- Interactive Form Trigger
- Google Maps business discovery
- AI-powered company research
- Business pain point identification
- AI automation opportunity detection
- Website quality assessment
- Company size estimation
- Structured JSON output
- Automatic Google Sheets integration
- Fully automated no-code workflow

---

# 🏗 Workflow Architecture

```
                Form Trigger
                     │
                     ▼
              Edit User Inputs
                     │
                     ▼
           Create Search Query
                     │
                     ▼
      Google Maps Search (SerpAPI)
                     │
                     ▼
            Split Companies List
                     │
                     ▼
       Research Each Company (Tavily)
                     │
                     ▼
      AI Business Analysis (OpenRouter)
                     │
                     ▼
             Parse JSON Response
                     │
                     ▼
         Store Results in Google Sheets
```

---

# ⚙️ How It Works

### Step 1

The user submits:

- Industry
- Country
- Number of Leads

through an n8n Form Trigger.

---

### Step 2

The workflow generates a dynamic search query such as:

```
Marketing Agencies in United States
```

or

```
Real Estate Companies in Australia
```

---

### Step 3

SerpAPI searches Google Maps and returns businesses matching the search criteria.

---

### Step 4

Each business is processed individually.

For every company, the workflow:

- Visits the website
- Searches additional information using Tavily AI
- Collects business information

---

### Step 5

The collected data is sent to an LLM through OpenRouter.

The AI analyzes:

- Company size
- Website quality
- Business overview
- AI automation opportunities
- Operational pain points
- AI automation fit score

---

### Step 6

The response is converted into structured JSON.

---

### Step 7

Each qualified lead is automatically saved into Google Sheets.

---

# 📊 Output

Each generated lead contains:

| Field |
|--------|
| Company Name |
| Industry |
| Website |
| Email |
| LinkedIn |
| Company Size |
| Website Quality |
| AI Automation Fit |
| Automation Opportunities |
| Business Pain Points |
| Research Summary |
| Date Added |

---

# 🛠 Tech Stack

| Technology | Purpose |
|------------|---------|
| n8n | Workflow Automation |
| SerpAPI | Google Maps Business Search |
| Tavily AI | Web Research |
| OpenRouter | LLM Access |
| JavaScript | JSON Parsing |
| Google Sheets API | Data Storage |

---

# 📁 Repository Structure

```
AI-Lead-Generation-Automation/

│
├── README.md
├── LICENSE
├── .gitignore
│
├── workflow/
│   └── ai-lead-generation-workflow.json
│
└── assets/
    ├── workflow.png
    ├── demo.mp4
    └── ai-lead-database.xlxs
```

---

# 🚀 Getting Started

## 1. Clone the repository

```bash
git clone https://github.com/nida-fatima247/ai-lead-generation-automation.git
```

---

## 2. Import the workflow

Open n8n and import:

```
workflow/ai-lead-generation-workflow.json
```

---

## 3. Configure Credentials

Add your own credentials for:

- SerpAPI
- Tavily AI
- OpenRouter
- Google Sheets

---

## 4. Execute the Workflow

Fill out the generated form with:

- Industry
- Country
- Number of Leads

Submit the form and let the workflow run.

---

# 🔒 Security

This repository does **not** include:

- API Keys
- OAuth Credentials
- Google Credentials
- Personal Data

Replace the placeholders with your own credentials before running the workflow.

---

# 💡 Future Improvements

- Frontend Dashboard
- CRM Integration
- Automated Email Outreach
- LinkedIn Enrichment
- AI Lead Scoring
- Duplicate Detection
- Multi-language Support
- Export to CSV
- Supabase Database Integration

---

# 🎯 Learning Outcomes

This project strengthened my understanding of:

- AI Workflow Automation
- API Integration
- JSON Parsing
- Prompt Engineering
- LLM Integration
- Business Process Automation
- Lead Qualification Pipelines
- End-to-End n8n Development

---

# 🤝 Contributing

Contributions, feature suggestions, and improvements are welcome.

Feel free to fork the repository and submit a pull request.

---

# 📄 License

This project is licensed under the MIT License.

---

## 👩‍💻 Author

**Nida Fatima**

Frontend Developer • AI Automation Developer

If you found this project helpful, consider giving it a ⭐ on GitHub!
