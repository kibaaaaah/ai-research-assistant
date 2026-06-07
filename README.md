# 🔍 AI Research Assistant

A lightweight AI-powered research tool that searches the web in real-time and generates structured, sourced research reports instantly — built with the Anthropic Claude API.

**[Live Demo →](https://yourusername.github.io/ai-research-assistant/)**

---

## ✨ Features

- 🌐 **Real-time web search** — not just AI training data, actual live results
- 📋 **Structured reports** — summary, key points, pros/cons, verdict, and sources
- ⚡ **Instant results** — clean JSON synthesis rendered on the fly
- 💡 **Quick topic chips** — one-click example searches to get started
- 🎨 **Clean UI** — minimal, responsive design that works on any device

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-----------|
| Frontend | HTML, CSS, Vanilla JavaScript |
| AI Model | Claude Sonnet (Anthropic API) |
| Search | Anthropic Web Search Tool (`web_search_20250305`) |
| Hosting | GitHub Pages |

---

## 🚀 How It Works

1. User enters a research topic
2. A request is sent to the **Anthropic `/v1/messages` API** with the **web search tool** enabled
3. Claude searches the web across multiple sources in real-time
4. Results are synthesized into a **structured JSON report**
5. The UI parses and renders the report cleanly

```javascript
// Core API call with web search tool
const response = await fetch('https://api.anthropic.com/v1/messages', {
  method: 'POST',
  headers: { 'Content-Type': 'application/json' },
  body: JSON.stringify({
    model: 'claude-sonnet-4-20250514',
    max_tokens: 1000,
    tools: [{ type: 'web_search_20250305', name: 'web_search' }],
    messages: [{ role: 'user', content: `Research this topic: ${query}` }]
  })
});
```

---

## 📦 Setup & Run Locally

No install needed. Just open the file:

```bash
git clone https://github.com/yourusername/ai-research-assistant.git
cd ai-research-assistant
open index.html
```

> **Note:** The app uses Anthropic's API via Claude.ai's infrastructure. To run it independently, you'll need an [Anthropic API key](https://console.anthropic.com).

---

## 📁 Project Structure

```
ai-research-assistant/
└── index.html      # entire app — HTML + CSS + JS in one file
└── README.md       # this file
```

---

## 🧠 What I Learned

- How to use the **Anthropic Claude API** with tool use
- How **web search tool** works as an API-level capability
- Structuring AI output as **JSON for dynamic UI rendering**
- Deploying a frontend project with **GitHub Pages**

---

## 🔮 Possible Improvements

- [ ] Save past research reports (localStorage)
- [ ] Export report as PDF
- [ ] Choose research depth (quick vs deep)
- [ ] Add citation links to sources
- [ ] Dark/light mode toggle

---

## 👤 Author

**Hiba Sherin**
- GitHub: [@kibaaaaah](https://github.com/kibaaaaah)
- LinkedIn:(www.linkedin.com/in/hiba-sherin-733330336)

---

## 📄 License

MIT License — free to use, modify, and share.
