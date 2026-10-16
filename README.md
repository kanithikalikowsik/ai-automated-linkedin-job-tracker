 <div align="center">

<img src="https://images.unsplash.com/photo-1677442136019-21780ecad995?auto=format&fit=crop&w=1600&q=85" alt="Generative AI technology" width="100%" />

# 🤖 AI Automated LinkedIn Job Tracker

### Discover Opportunities. Automate Intelligence. Track Smarter.

  An AI-powered workflow built with **n8n, Google Gemini, RSS feeds, and Google Sheets** to automate the processing and organization of job-    related information.

<p>
<img src="https://img.shields.io/badge/AI-Google%20Gemini-4285F4?style=for-the-badge&logo=google&logoColor=white" alt="Google Gemini" />
<img src="https://img.shields.io/badge/Automation-n8n-EA4B71?style=for-the-badge&logo=n8n&logoColor=white" alt="n8n" />
<img src="https://img.shields.io/badge/Data-Google%20Sheets-34A853?style=for-the-badge&logo=googlesheets&logoColor=white" alt="Google Sheets" />
<img src="https://img.shields.io/badge/Workflow-AI%20Powered-7C3AED?style=for-the-badge" alt="AI-powered workflow" />
</p>

</div>

---

## ✨ Project Overview

  Finding and organizing job opportunities can involve repetitive searching, reading, and record keeping.

  **AI Automated LinkedIn Job Tracker** explores how AI and workflow automation can simplify this process. The workflow retrieves information   from a configured RSS feed, processes the content through Google Gemini, formats the output using a Structured Output Parser, and stores     the results in Google Sheets.

  The goal is to build a repeatable pipeline that helps organize job-related information with less manual effort.

> **One workflow. Multiple connected services. Smarter information management.**

## 🎯 Key Features

  - ⏰ **Scheduled Execution** — Starts automatically according to the configured schedule.
  - 📰 **RSS Integration** — Retrieves information from a configured RSS feed.
  - 🧠 **AI-Powered Processing** — Uses Google Gemini to analyze and process incoming content.
  - 🧩 **Structured AI Output** — Uses a Structured Output Parser to format generated results.
  - 📊 **Google Sheets Integration** — Appends or updates processed information in a spreadsheet.
  - 🔄 **Workflow Automation** — Connects data collection, AI processing, and storage in one pipeline.
  - 🔐 **Credential Management** — Supports securely configured service credentials through n8n.

## 🛠️ Technology Stack

  | Technology | Purpose |
  |---|---|
  | **n8n** | Connects and automates the workflow steps |
  | **RSS Feed** | Provides job-related information |
  | **Google Gemini** | Processes content using generative AI |
  | **Basic LLM Chain** | Orchestrates AI processing |
  | **Structured Output Parser** | Formats the AI response |
  | **Google Sheets** | Stores and organizes processed results |

## ⚡ Inside the Workflow

### Workflow Architecture

  ```mermaid
  flowchart TD
      A["⏰ Schedule Trigger"] --> B["📰 RSS Read"]
      B --> C["✨ Basic LLM Chain"]
      D["🧠 Google Gemini Model"] -.-> C
      E["🧩 Structured Output Parser"] -.-> C
      C --> F["📊 Append or Update Row in Google Sheets"]
  
      style A fill:#172554,color:#FFFFFF,stroke:#60A5FA
      style B fill:#7C2D12,color:#FFFFFF,stroke:#FB923C
      style C fill:#4C1D95,color:#FFFFFF,stroke:#C4B5FD
      style D fill:#1E3A8A,color:#FFFFFF,stroke:#93C5FD
      style E fill:#164E63,color:#FFFFFF,stroke:#22D3EE
      style F fill:#065F46,color:#FFFFFF,stroke:#6EE7B7
  ```

### 🔍 How It Works

  **01 — Schedule**
  
  The Schedule Trigger starts the workflow at the configured time.
  
  **02 — Collect**
  
  The RSS Read node retrieves content from the configured RSS feed.
  
  **03 — Analyze**
  
  The Basic LLM Chain processes the incoming content using the connected Google Gemini model.
  
  **04 — Structure**
  
  The Structured Output Parser helps format the AI-generated response into the expected structure.
  
  **05 — Store**
  
  The Google Sheets node appends or updates the processed information in the configured spreadsheet.

### 📌 Workflow Outcome

  A connected automation pipeline for collecting, processing, and organizing job-related information using AI.

  *Note: The workflow shown uses RSS-based information retrieval. It does not necessarily connect directly to LinkedIn or scrape LinkedIn job   listings. Results depend on the configured feed, AI prompt, and spreadsheet mapping.*

## 🖼️ Workflow Preview

<div align="center">

<!-- Replace the path below with your uploaded workflow screenshot. -->

<img src="https://res.cloudinary.com/dntdfccdk/image/upload/v1792165257/Screenshot_2026-10-16_210948_eug2pp.png" alt="AI Automated LinkedIn Job Tracker n8n workflow" width="100%" />

<em>Workflow preview showing the n8n automation pipeline.</em>

</div>

## 🚀 Getting Started

### Prerequisites

  Before running the workflow, make sure you have:
  
  - An n8n account or self-hosted n8n instance.
  - Access to an RSS feed that provides relevant content.
  - Google Gemini API access, where required by your configuration.
  - A Google account and destination spreadsheet.
  - The necessary Google Sheets credentials configured in n8n.

### Installation and Setup

  **Step 1 — Export the workflow**
  
  Open the workflow in n8n and export it as a JSON file.
  
  **Step 2 — Import into n8n**
  
  Open your n8n workspace and import the exported JSON workflow.
  
  **Step 3 — Configure the RSS feed**
  
  Set the RSS feed URL to a source that provides the job-related information you want to track.
  
  **Step 4 — Configure Google Gemini**
  
  Set up the required credentials and verify the model connected to the Basic LLM Chain.
  
  **Step 5 — Configure structured output**
  
  Review the Structured Output Parser schema and ensure it matches the output expected by your workflow and spreadsheet.
  
  **Step 6 — Connect Google Sheets**
  
  Authorize your Google account, choose the destination spreadsheet, and map the generated fields to the correct columns.
  
  **Step 7 — Test the workflow**
  
  Execute the workflow manually and check the execution results, AI output, and spreadsheet entries.
  
  **Step 8 — Enable automation**
  
  Once the workflow works correctly, activate or publish it according to your n8n version and configuration.
  
## 📊 Suggested Google Sheets Fields

  You can organize the collected information using columns such as:
  
  | Field | Description |
  |---|---|
  | Job Title | Name of the position |
  | Company | Organization offering the role |
  | Location | Job location, if available |
  | Job Description | Relevant job details |
  | Skills | Required skills, if extracted |
  | Application URL | Original application link, if available |
  | Summary | AI-generated summary |
  | Date Added | Date the record was collected |
  
  *These are suggested fields. Your actual spreadsheet should match the fields produced by your configured workflow.*
  
## 🔮 Future Enhancements

  The project can be extended with additional features:
  
  - [ ] Track job titles, companies, locations, and application links.
  - [ ] Filter opportunities by skills, role, and preferred location.
  - [ ] Detect duplicate job entries.
  - [ ] Add job relevance scoring using AI.
  - [ ] Send email notifications for relevant opportunities.
  - [ ] Track application status, deadlines, and follow-ups.
  - [ ] Integrate additional authorized RSS feeds or job APIs.
  - [ ] Generate daily or weekly job opportunity digests.

## 🔐 Security Best Practices

  - Never commit API keys, OAuth tokens, passwords, or private credentials.
  - Store credentials using n8n's credential management features.
  - Inspect exported workflow JSON files before uploading them to GitHub.
  - Remove sensitive information from screenshots and configuration files.
  - Use trusted news and job sources and respect their terms of use.
  - Verify AI-generated details against the original source before applying.

## 📚 Learning Outcomes

  This project provides practical experience with:
  
  - Building multi-step workflows using n8n.
  - Integrating Google Gemini into an automation pipeline.
  - Collecting content through RSS feeds.
  - Processing AI responses using structured output.
  - Connecting automation workflows with Google Sheets.
  - Testing workflow executions and troubleshooting integrations.
  - Applying security practices to AI-powered automation.

## 🌱 Why This Project?

  This project explores how generative AI can be combined with workflow automation to reduce repetitive information-processing tasks.
  
  It also demonstrates how multiple services can work together in a practical pipeline—from information collection to AI processing and         structured storage.

## 👨‍💻 Author

**Kalikowsik**

  Aspiring Full Stack Developer | AI & Automation Enthusiast

### Connect With Me

  - GitHub: https://github.com/kanithikalikowsik
  - LinkedIn: www.linkedin.com/in/kanithi-kali-kowsik

## 📄 License

  This project is licensed under the **MIT License**. See the [LICENSE](LICENSE) file for details.

---

<div align="center">

### 💡 Automate the process. Focus on the opportunity.

  **Built with n8n · Enhanced by Google Gemini · Organized with Google Sheets**

  If you find this project useful, consider giving the repository a ⭐ on GitHub.

</div>
