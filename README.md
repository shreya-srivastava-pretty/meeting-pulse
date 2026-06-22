# ⚡ MeetingPulse

> **Turn meeting transcripts into action items in 10 seconds.**
> Free forever. Runs locally. No API keys. No cloud. No subscriptions.

---

## 🎯 What it does

Paste any meeting transcript — Zoom, Teams, voice notes, raw text — and instantly get:

- **Action Items** — with owner, priority (high/medium/low) and deadline
- **Decisions Made** — key decisions captured from the discussion
- **Smart Summary** — 2-3 sentence overview of the meeting
- **Export** — download as Markdown, JSON, or plain text

---

## 🚀 Quick Start

### 1. Install Ollama
| OS | Command |
|---|---|
| macOS | `brew install ollama` |
| Linux | `curl -fsSL https://ollama.com/install.sh \| sh` |
| Windows | Download from [ollama.com](https://ollama.com) |

### 2. Pull the AI model
```bash
ollama pull llama3
```
*(~4GB download, one time only)*

### 3. Start Ollama with CORS enabled
```bash
# macOS / Linux
OLLAMA_ORIGINS=* ollama serve

# Windows (Command Prompt)
set OLLAMA_ORIGINS=* && ollama serve

# Windows (PowerShell)
$env:OLLAMA_ORIGINS="*"; ollama serve
```

### 4. Open the app
Double-click `index.html` in your browser. Done.

---

## 🏗 Tech Stack

| Layer | Tech | Cost |
|---|---|---|
| AI Model | Llama 3 via Ollama | **Free** |
| Frontend | Vanilla HTML/CSS/JS | **Free** |
| Hosting | Netlify / GitHub Pages | **Free** |
| Backend | None needed | — |

**Total cost: $0. Forever.**

---

## 🌐 Deploy (Free)

### Netlify (easiest — drag & drop)
1. Go to [netlify.com](https://netlify.com) and sign up
2. Drag the `meetingpulse` folder onto the dashboard
3. Get a live URL instantly — e.g. `meetingpulse.netlify.app`

### GitHub Pages
```bash
git init && git add . && git commit -m "init"
git remote add origin https://github.com/YOUR_USERNAME/meetingpulse.git
git push -u origin main
# Enable Pages in repo Settings → Pages → main branch
```

> **Note:** Visitors need Ollama running locally. For a shared deployment, point the fetch URL to a hosted Ollama server.

---

## 🔧 Configuration

Edit these in `index.html`:

```javascript
// Change AI model
model: 'llama3'      // default — good balance
model: 'mistral'     // faster, lighter
model: 'llama3:70b'  // most accurate, needs 32GB+ RAM

// Change Ollama endpoint
'http://localhost:11434/api/generate'   // local (default)
'http://your-server:11434/api/generate' // shared server
```

---

## 🏆 Hackathon Pitch

> *"Every team wastes 20-30 minutes after every meeting figuring out who does what.
> MeetingPulse fixes that in 10 seconds — with zero cloud dependency,
> zero cost, and zero privacy risk since everything runs on your machine."*

**Theme:** AI for Productivity · Privacy-first AI · Local/Edge AI

**Tags:** `productivity` `AI` `llama3` `ollama` `local-ai` `meeting` `NLP` `privacy` `open-source`

---

## 📁 Project Structure

```
meetingpulse/
└── index.html    # Entire app — single file, no dependencies
```

---

## 📄 License

MIT — free to use, modify, and distribute.
