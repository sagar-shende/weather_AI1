<div align="center">

# 🌦️ Weather AI Agent — IBM watsonx.ai

<img src="https://img.shields.io/badge/IBM-watsonx.ai-054ADA?style=for-the-badge&logo=ibm&logoColor=white"/>
<img src="https://img.shields.io/badge/LangGraph-ReAct_Agent-2C8EBB?style=for-the-badge"/>
<img src="https://img.shields.io/badge/Meta_Llama-3.2_90B-F97316?style=for-the-badge&logo=meta&logoColor=white"/>
<img src="https://img.shields.io/badge/Python-3.11-3776AB?style=for-the-badge&logo=python&logoColor=white"/>
<img src="https://img.shields.io/badge/Status-Completed-22C55E?style=for-the-badge"/>

<br/>

[![Open in nbviewer](https://img.shields.io/badge/📓_Open-nbviewer-F37626?style=flat-square)](https://nbviewer.org/github/sagar-shende/weather_AI1/blob/main/weather-ai-agent-ibm-watsonx)
[![GitHub stars](https://img.shields.io/github/stars/sagar-shende/weather_AI1?style=flat-square&color=yellow)](https://github.com/sagar-shende/weather_AI1/stargazers)
[![License](https://img.shields.io/badge/License-MIT-blue?style=flat-square)](LICENSE)
[![Internship](https://img.shields.io/badge/IBM_SkillsBuild-AICTE_Intern-054ADA?style=flat-square&logo=ibm)](https://skillsbuild.org)

<br/>

> 🤖 An **AI-powered conversational weather agent** built on IBM watsonx.ai platform,
> using a **LangGraph ReAct agent** with real-time GoogleSearch tool and **MemorySaver** for multi-turn context.

<br/>

</div>

---

## 📌 Table of Contents

- [Overview](#-overview)
- [Demo Output](#-demo-output)
- [Architecture](#-architecture)
- [Tech Stack](#-tech-stack)
- [Project Structure](#-project-structure)
- [Setup & Installation](#-setup--installation)
- [How It Works](#-how-it-works)
- [Key Features](#-key-features)
- [Internship Context](#-internship-context)
- [Author](#-author)

---

## 🔍 Overview

The **Weather AI Agent** is an intelligent conversational assistant that answers natural language weather queries for any city in the world. Unlike static weather apps, this agent:

- 🧠 **Understands natural language** — Ask *"Is it going to rain in Mumbai tomorrow?"*
- 🔍 **Fetches live data** — Uses GoogleSearch Tool for real-time results
- 💬 **Remembers context** — MemorySaver keeps track of your conversation
- 📊 **Formats rich reports** — Markdown output with expert suggestions

Built as a final project for the **IBM SkillsBuild × AICTE × Edunet Foundation** 4-week internship on AI & Cloud Technologies.

---

## 🖥️ Demo Output

```
User ▶  What is the weather in Nagpur today?

Agent ▶
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
🔎  Weather Report — Nagpur, Maharashtra
     📅  7th August 2025
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

🌤  Current Conditions
    🌡  Temperature   : 31°C  (Feels Like: 34°C)
    💧  Humidity      : 66%
    🌬  Wind          : 14 km/h (West)
    ☁️  Condition     : Partly Cloudy

🌧  Rain Forecast
    ⚡  Probability   : 60%
    🕕  Expected      : Evening 6 PM – 8 PM

📈  Today's Range    : High 33°C — Low 25°C
🌅  Sunrise          : 5:54 AM
🌇  Sunset           : 6:48 PM

💡  Expert Suggestion:
    ☂  Carry an umbrella in the evening
    💧  Stay hydrated — humidity is high
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

---

## 🏗️ Architecture

```
┌─────────────────────────────────────────────────────────────┐
│                      USER INTERFACE                          │
│              Natural Language Weather Query                  │
└──────────────────────────┬──────────────────────────────────┘
                           │
                           ▼
┌─────────────────────────────────────────────────────────────┐
│                  LANGGRAPH ReAct AGENT                       │
│                                                             │
│   ┌─────────────┐    ┌──────────────┐    ┌─────────────┐   │
│   │   Reasoning  │───▶│   Acting     │───▶│ Observation │   │
│   │  (LLaMA 3.2) │    │ (Tool Call)  │    │ (Result)    │   │
│   └─────────────┘    └──────────────┘    └──────┬──────┘   │
│          ▲                                       │          │
│          └───────────────────────────────────────┘          │
│                    MemorySaver (State)                       │
└────────┬──────────────────────────┬────────────────────────┘
         │                          │
         ▼                          ▼
┌─────────────────┐      ┌──────────────────────┐
│  IBM watsonx.ai │      │   GoogleSearch Tool   │
│  Meta LLaMA 3.2 │      │  (Real-time Weather)  │
│     90B Model   │      │                      │
└─────────────────┘      └──────────────────────┘
         │
         ▼
┌─────────────────────────────────────────────────────────────┐
│               STRUCTURED MARKDOWN RESPONSE                   │
│        Weather Report with Expert Suggestions                │
└─────────────────────────────────────────────────────────────┘
```

---

## 🛠 Tech Stack

| Layer | Tool | Purpose |
|---|---|---|
| **AI Platform** | IBM watsonx.ai | Foundation Model hosting & inference |
| **Foundation Model** | Meta Llama 3.2 90B Vision Instruct | NLU + response generation |
| **Agent Framework** | LangGraph | ReAct loop, state management |
| **LLM Interface** | LangChain IBM (`langchain_ibm`) | Watson Chat Model wrapper |
| **Memory** | LangGraph MemorySaver | Multi-turn conversation state |
| **Search** | GoogleSearch Tool | Real-time weather data retrieval |
| **Language** | Python 3.11 | Core development |
| **Environment** | Jupyter Notebook | Interactive development |

---

## 📁 Project Structure

```
weather_AI1/
│
├── 📓 weather-ai-agent-ibm-watsonx.ipynb   # Main notebook — agent setup & demo
├── 📄 Sagar_Shende_IBM_Internship_PPT.pdf  # Internship project presentation
├── 📝 README.md                            # Project documentation
└── 📋 requirements.txt                     # Python dependencies (see below)
```

---

## ⚙️ Setup & Installation

### Prerequisites

- Python 3.11+
- IBM Cloud account with watsonx.ai access
- IBM Cloud API Key & Project ID

### Step 1 — Clone the repository

```bash
git clone https://github.com/sagar-shende/weather_AI1.git
cd weather_AI1
```

### Step 2 — Install dependencies

```bash
pip install langchain-ibm ibm-watsonx-ai langgraph langchain-community
```

Or use the full list:

```bash
pip install -r requirements.txt
```

<details>
<summary>📋 requirements.txt</summary>

```
langchain-ibm>=0.1.0
ibm-watsonx-ai>=0.2.6
langgraph>=0.1.0
langchain-community>=0.2.0
langchain-core>=0.2.0
google-search-results>=2.4.2
jupyter>=1.0.0
```

</details>

### Step 3 — Configure IBM credentials

When prompted in the notebook, enter:

```python
IBM_API_KEY   = "your-ibm-cloud-api-key"
PROJECT_ID    = "your-watsonx-project-id"
```

> 💡 Get your API key from [IBM Cloud IAM](https://cloud.ibm.com/iam/apikeys) and Project ID from [IBM watsonx.ai](https://dataplatform.cloud.ibm.com/)

### Step 4 — Run the notebook

```bash
jupyter notebook weather-ai-agent-ibm-watsonx.ipynb
```

---

## ⚡ How It Works

The agent follows the **ReAct (Reason + Act)** pattern:

```
1. USER sends a natural language weather query

2. AGENT reasons:
   "I need to search for current weather in [city]"

3. AGENT acts:
   → Calls GoogleSearch Tool with weather query

4. AGENT observes:
   → Receives raw search results

5. LLaMA 3.2 90B processes:
   → Formats into structured Markdown weather report
   → Adds contextual expert suggestions

6. MEMORYSAVER stores:
   → Conversation state for multi-turn interactions

7. USER receives:
   → Detailed, formatted weather report
```

---

## ✨ Key Features

| Feature | Description |
|---|---|
| 🌍 **Global Coverage** | Weather for any city worldwide |
| 💬 **Conversational** | Natural language queries, no rigid format needed |
| 🔄 **Multi-Turn Memory** | MemorySaver keeps conversation context across turns |
| ⚡ **Real-Time Data** | GoogleSearch fetches live weather, no stale cache |
| 📊 **Rich Reports** | Temperature, humidity, wind, UV, sunrise/sunset |
| 🧠 **Expert Advice** | AI-generated contextual suggestions (umbrella, hydration, etc.) |
| 📝 **Markdown Output** | Clean, structured, emoji-rich formatting |

---

## 🎓 Internship Context

This project was developed as the **final capstone project** for:

```
🏢  Organization  : Edunet Foundation
🤝  Partners      : IBM SkillsBuild × AICTE
📅  Duration      : 14 July – 6 August 2025 (4 Weeks)
🎯  Domain        : AI & Cloud Technologies
🏆  Certificate   : IBM SkillsBuild + Edunet Foundation
```

**Skills demonstrated:**
- IBM watsonx.ai Foundation Model integration
- LangGraph ReAct agent architecture
- Stateful multi-turn agent design with MemorySaver
- Real-time tool use (GoogleSearch)
- IBM Cloud API configuration & project management

---

## 👤 Author

<div align="center">

**Sagar Kishor Shende**
*AI & Cloud Intern — IBM SkillsBuild × AICTE × Edunet Foundation*

[![GitHub](https://img.shields.io/badge/GitHub-sagar--shende-181717?style=for-the-badge&logo=github)](https://github.com/sagar-shende)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Sagar_Shende-0A66C2?style=for-the-badge&logo=linkedin)](https://www.linkedin.com/in/sagarshende-ai)
[![Email](https://img.shields.io/badge/Email-sagarshende0608@gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:sagarshende0608@gmail.com)

</div>

---

<div align="center">

**⭐ If this project helped you, please star the repo!**

*Built with ❤️ using IBM watsonx.ai · LangGraph · Meta LLaMA 3.2 · GoogleSearch*

</div>
