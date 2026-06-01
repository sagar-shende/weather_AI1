# 🌦️ Weather AI Agent — IBM watsonx.ai

![IBM Watson](https://img.shields.io/badge/IBM-watsonx.ai-blue?logo=ibm)
![LangChain](https://img.shields.io/badge/LangChain-Agent-green)
![Model](https://img.shields.io/badge/Model-Llama_3.2_90B-orange)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)
[![Open in nbviewer](https://img.shields.io/badge/Open-nbviewer-orange)](https://nbviewer.org/github/sagar-shende/weather_AI1/blob/main/weather-ai-agent-ibm-watsonx)

> 🤖 An AI-powered weather agent built on IBM watsonx.ai platform
> using LangGraph ReAct agent with real-time GoogleSearch tool.

---

## 🎯 What It Does
- Fetches **real-time weather** for any city globally
- Uses **GoogleSearch tool** for live data
- Provides temperature, humidity, rain probability & expert suggestions
- Powered by **Meta Llama 3.2 90B** vision model

---

## 🛠 Tech Stack
| Tool | Purpose |
|---|---|
| IBM watsonx.ai | AI Platform |
| LangGraph | ReAct Agent Framework |
| LangChain IBM | Watson Chat Model |
| Meta Llama 3.2 90B | Foundation Model |
| GoogleSearch Tool | Real-time weather data |
| Python 3.11 | Core programming |

---

## 📊 Sample Output

```
🌤 Weather Report — Nagpur, Maharashtra (7th August 2025)

🌡 Temperature  : 31°C  |  Feels Like: 34°C
💧 Humidity     : 66%   |  Wind: 14 km/h (West)
🌧 Rain Chance  : 60%   |  Evening 6 PM – 8 PM

📈 Today's Range: High 33°C — Low 25°C
🌅 Sunrise: 5:54 AM  |  🌇 Sunset: 6:48 PM

💡 Expert Suggestion:
   ☂ Carry umbrella in evening
   💧 Stay hydrated — humidity is high
```

---

## ⚙️ How It Works

```
User Question
     ↓
ReAct Agent (LangGraph)
     ↓
GoogleSearch Tool → Real-time Weather Data
     ↓
Llama 3.2 90B → Structured Weather Report
     ↓
User Gets Answer
```

---

## 🚀 How to Run

```bash
# Step 1 — Install dependencies
pip install langchain-ibm ibm-watsonx-ai langgraph

# Step 2 — Set IBM API Key
Enter your IBM Cloud API key when prompted

# Step 3 — Run notebook
jupyter notebook weather_AI.ipynb
```

---

## 👤 Author
**Sagar Kishor Shende**
[![GitHub](https://img.shields.io/badge/GitHub-sagar--shende-black?logo=github)](https://github.com/sagar-shende)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-blue?logo=linkedin)](https://www.linkedin.com/in/sagarshende-ai)
