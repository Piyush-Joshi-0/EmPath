# 🧠 EmPath – AI Mental Health Therapist

Your compassionate AI companion for emotional support, built with care and real-world tools.
EmPath listens, understands, and responds with empathy — and knows when to escalate to emergency help.

Equipped with an AI agent architecture, specialist healthcare models (MedGemma), and life-saving tools like emergency calling & Telegram alerts, EmPath is designed to support mental well-being — safely and responsibly.

📸 Project Snapshots

## 🤖 Chatting with the AI Therapist

<img width="1920" height="1080" alt="Screenshot 2025-08-12 131330" src="https://github.com/user-attachments/assets/ce6d3c72-99ca-43f9-98dc-aa296480c161" />

<img width="1920" height="1080" alt="Screenshot 2025-08-12 132742" src="https://github.com/user-attachments/assets/43cc961a-e33d-48dc-86f5-7b8f9543645c" />

## 🧑‍⚕️ Therapist recommendations (with contact details)

<img width="1920" height="1080" alt="Screenshot 2025-08-12 133031" src="https://github.com/user-attachments/assets/aacd8303-4211-4a61-b66e-5dc4653cce68" />


## ⚠️ Suicidal thought detection & emergency response

<img width="1920" height="1080" alt="Screenshot 2025-08-12 133359" src="https://github.com/user-attachments/assets/02fec821-0238-4026-8918-76eac702b34d" />


## 📲 Telegram emergency alert sent to a contact

![WhatsApp Image 2025-09-01 at 21 06 44_44e49a0c](https://github.com/user-attachments/assets/3de1c4af-39fc-45d3-9b2f-fd1b4515f4b0)


🔄 System Flowchart of EmPath


## 🚀 Features  

- ✅ Empathetic conversations powered by **MedGemma (LLM)** via **Ollama**  
- ✅ Crisis detection → triggers **Telegram Emergency Alerts** (Twilio optional)  
- ✅ Nearby therapist recommendations (location-based)  
- ✅ Full-stack system with **Streamlit frontend + FastAPI backend**  
- ✅ Modular AI Agent built with **LangChain + LangGraph**  

---

## ⚙️ Tech Stack  

- **Frontend:** Streamlit (`frontend.py`)  
- **Backend:** FastAPI (`main.py`)  
- **AI Agent:** LangGraph + LangChain (`ai_agent.py`)  
- **LLM:** Google MedGemma (via Ollama)  
- **Tools:**  
  - Telegram bot alerts  
  - Therapist lookup  
  - (Optional) Twilio calls for emergencies  
- **Config:** API keys & secrets stored in `config.py`  


## 🏗️ Project Structure  

```bash
backend/
│── ai_agent.py      # AI agent with tools (chat, therapists, emergency)
│── config.py        # API keys & emergency contacts
│── main.py          # FastAPI backend
│── tools.py         # MedGemma queries + alert tools
frontend.py          # Streamlit frontend UI
pyproject.toml       # Dependencies
README.md            # Project documentation
AI Therapist.pdf     # Architecture overview
```
## 🔧 Setup & Installation  

### 1️⃣ Clone the repo  
```bash
git clone https://github.com/YOUR_USERNAME/empath-ai-therapist.git
cd empath-ai-therapist
```
### 2️⃣ Setup environment (using uv)
```bash
uv sync
```
This will:  
- ✔️ Create virtual environment  
- ✔️ Install dependencies from `pyproject.toml`  

---

### 3️⃣ Configure API Keys  

Edit `backend/config.py` and add your:  
- **GROQ_API_KEY** (or OpenAI if you switch models)  
- **Telegram Bot Token & Chat ID**  
- *(Optional)* Twilio credentials  

---

### 4️⃣ Run the Backend  
```bash
uv run backend/main.py
```
### 5️⃣ Run the Frontend
```bash
uv run streamlit run frontend.py
```
## 📡 How It Works  

1. User sends a message in the **Streamlit chat UI**  
2. Message goes to **FastAPI backend** (`/ask`)  
3. AI Agent decides:  
   - 💬 Use **MedGemma** for normal responses  
   - 🧑‍⚕️ Recommend **therapists** if requested  
   - 🚨 Trigger **emergency alert** if suicidal/self-harm intent detected  
4. Response + tool used are displayed in the UI  

---

## 🔐 Safety Note  

This project is **not a replacement for professional help**.  
If you are struggling with mental health issues, please reach out to a qualified therapist or helpline immediately.  

