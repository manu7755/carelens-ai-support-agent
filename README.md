# 💬 CareLens AI — Customer Support Agent with Memory

CareLens AI is an intelligent customer support assistant built for **small businesses and SaaS products**.  
It answers customer questions, remembers past context, and responds using your own FAQ / policy documents.

Not just a chatbot — it behaves like a **support agent** with memory.

---

## 🎯 What Problem Does It Solve?

Most small businesses struggle with:

- Repeating answers to the same customer questions
- Slow response time due to manual support
- No unified place for FAQ / policy-based answers
- High support cost for simple, repetitive queries

CareLens AI solves this by:

✅ Handling common questions automatically  
✅ Using your FAQ / docs as a knowledge base  
✅ Remembering previous messages in a conversation  
✅ Logging chats for future review & improvement  

---

## 🚀 Key Features

- 🧠 **Conversation Memory**  
  Remembers previous user messages in the same session for more natural replies.

- 📚 **FAQ / Document-Aware Answers**  
  Can be extended to load product FAQs, policy docs, and help content.

- 🏷️ **Automatic Tagging**  
  Tags each query as: `Sales`, `Support`, or `General`.

- ⚠️ **Priority Flagging**  
  Detects urgent messages (e.g. “refund”, “error”, “not working”) and flags them.

- 📊 **Chat Log Export (Planned)**  
  Chats can be stored for analysis or CRM integration.

---

## 🧠 LLM Flexibility (Free + Premium)

CareLens AI is designed to work with both:

- ✅ **Open-source models** (e.g. Llama-3, Mistral via HuggingFace)
- ✅ **Commercial models** (e.g. GPT-4o, Claude) — *optional for clients who want it*

You can plug in **any LLM** in the `generate_response()` function.

---

## 🛠️ Tech Stack

- **Frontend / UI:** Streamlit
- **Memory:** In-session chat history (can be extended to ChromaDB)
- **Language Models:** Pluggable (Llama-3, GPT-4o, Claude, etc.)
- **Tagging:** Simple rule-based classification (keywords based)

---

## 🏗️ High-Level Architecture

1. User opens CareLens AI web UI  
2. User starts a support conversation  
3. Each user message is:
   - Stored into **chat history** (memory)
   - Checked for keywords to set **category & priority**
4. System generates a reply using:
   - Conversation history
   - (Optional) FAQ / support documentation
5. Reply is displayed + metadata (category, priority) can be logged.

---

## 📂 Project Structure

```bash
carelens-ai-support-agent/
 ├─ app.py
 ├─ requirements.txt
 └─ README.md
