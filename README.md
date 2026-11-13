# 😊 MoodMap: Customer Sentiment Journey

An interactive dashboard that treats customer sentiment as a **journey**, not a single score.
The customer describes a problem, a sentiment agent scores **every message** and shows a smiley,
the chatbot changes its reply to fit the situation, and the final outcome is mapped to
**🥳 SOLVED** or **😞 NOT SOLVED**.

## ✨ Features
| Feature | What it does |
|---|---|
| 💬 Support chat | The customer types a problem, and the bot replies based on mood, topic and mood trend |
| 😡→😍 Per-message smiley | 7-level mood scale on every customer message, with a score from −1 to +1 |
| 📈 Live mood panel | Large smiley, red-to-green meter, and the words the agent picked up |
| 🛤️ Emotion journey | Smiley trail (😡 → 😠 → 🙂 → 😊) and a mood-trend chart |
| ✅ Resolution mapping | Final 🥳 / 😞 outcome, set automatically from the chat or manually |
| 📂 Bulk review analysis | Upload a CSV and get a mood mix, sentiment by star rating, a filterable table and a CSV export |

## 🎭 Mood scale
| Smiley | Mood | Score range |
|---|---|---|
| 😡 | Angry | −1.00 to −0.60 |
| 😠 | Frustrated | −0.60 to −0.30 |
| 😟 | Worried / Upset | −0.30 to −0.08 |
| 😐 | Neutral | −0.08 to +0.12 |
| 🙂 | Hopeful | +0.12 to +0.35 |
| 😊 | Happy | +0.35 to +0.60 |
| 😍 | Delighted | +0.60 to +1.00 |

## 🚀 Run it
No build step and no server needed.
1. Clone the repo, or download it.
2. Double-click `index.html` to open it in a browser. The page needs an internet connection to load the chart library.
3. Click the sample message buttons in order to see a customer go from angry to solved.
4. Under **Bulk review analysis**, choose `sample_reviews.csv` or click **Load sample reviews**.

**GitHub Pages:** go to Settings → Pages → Deploy from branch `main` / root. The dashboard will then be live at `https://<username>.github.io/moodmap-sentiment-journey/`.

## 🤖 AI agent version
The dashboard scores moods with a built-in word list, so it runs instantly in any browser.
There is also an LLM-powered **MoodMap Support Agent**, built in Amazon Quick. It understands context and sarcasm,
replies in the customer's language, tries two fixes before escalating, and closes a case only after the customer confirms.
See [`agent/agent_instructions.md`](agent/agent_instructions.md).

## 🧠 How it works
See [`docs/architecture.md`](docs/architecture.md).

## 📁 Structure
```
├── index.html               # The dashboard (one self-contained file)
├── sample_reviews.csv       # Sample data for the review analysis
├── agent/agent_instructions.md
├── docs/architecture.md
├── LICENSE
└── README.md
```

## 🛣️ Roadmap
- Plug an LLM API into the dashboard in place of the word list
- Save customer journeys across visits
- Add Tamil and Hindi words to the word list

## 📸 Screenshots
_Add screenshots of the chat journey and the review analysis here._

## 📄 License
MIT
