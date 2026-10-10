# ContentFlow AI 🚀

> **AI-Powered Smart Social Media Planner** — generate a full 7-day content calendar with platform-tailored copy, hashtags, and optimal posting times in seconds.

![ContentFlow AI](https://img.shields.io/badge/ContentFlow-AI%20Powered-6c63ff?style=for-the-badge)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)

---

## ✨ Features

| Feature | Description |
|---|---|
| 🤖 AI Content Generation | Brand-aware, tone-aware copy for every platform |
| 📅 7-Day Visual Calendar | Full week grid with day/date headers |
| 📱 4 Platforms | Instagram, X (Twitter), LinkedIn, Facebook |
| 🎨 4 Tone Modes | Motivational, Professional, Casual & Fun, Educational |
| ⏰ Optimal Timing | Research-backed best posting times per platform |
| #️⃣ Smart Hashtags | Platform-specific hashtag sets auto-generated |
| ✏️ Edit Posts | In-modal post editor for copy, hashtags, time |
| ↺ Regenerate | Per-post or full calendar regeneration |
| ✓ Mark Done | Track published posts with done state |
| 📋 Export | Copy full calendar as formatted text |
| 🔍 Platform Filter | Filter view by platform tab |

---

## 🗂️ Project Structure

```
contentflow-ai/
│
├── index.html              # App shell — structure only
│
├── styles/
│   ├── variables.css       # CSS custom properties (design tokens)
│   ├── base.css            # Reset, body, global forms, shared buttons
│   ├── header.css          # Sticky top navigation bar
│   ├── sidebar.css         # Left config panel
│   ├── calendar.css        # Week grid, stats bar, platform tabs
│   ├── post-card.css       # Individual post card component
│   ├── modals.css          # Edit & export modals
│   ├── loading.css         # Full-screen AI generation overlay
│   ├── toast.css           # Bottom-right notification
│   └── responsive.css      # Breakpoint overrides
│
├── js/
│   ├── config.js           # Platform metadata, times, hashtags
│   ├── templates.js        # AI content templates (tone × platform)
│   ├── state.js            # Central application state
│   ├── generator.js        # AI content generation engine
│   ├── renderer.js         # DOM rendering functions
│   ├── actions.js          # User action handlers
│   ├── ui.js               # UI controls (modals, toast, loading)
│   └── app.js              # Entry point & DOMContentLoaded init
│
└── README.md
```

---

## 🚀 Getting Started

### Run locally

No build step needed — it's pure HTML/CSS/JS.

```bash
# Clone
git clone https://github.com/Awaniii24/content-flow-ai-.git
cd content-flow-ai-

# Open in browser
open index.html        # macOS
start index.html       # Windows
xdg-open index.html    # Linux
```

Or use the [Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer) VS Code extension.

---

## 🎮 How to Use

1. **Enter your Brand Name** and a short description in the sidebar
2. **Select Platforms** — toggle Instagram, X/Twitter, LinkedIn, Facebook
3. **Choose a Tone** — Motivational, Professional, Casual & Fun, or Educational
4. **Set Posts Per Day** (1–4)
5. **Pick a Content Focus** from the dropdown
6. Click **✦ Generate 7-Day Calendar**
7. Browse your week grid — use filter tabs to view by platform
8. **Edit** any post with the ✏️ button, **Regenerate** with ↺, **Copy** with 📋
9. **Mark Done** posts with ✓ as you publish them
10. **Export** the full calendar as text with the ↓ Export button

---

## 🏗️ Architecture

```
index.html
    │
    ├── styles/*.css          (10 modular stylesheets)
    │
    └── js/ (load order matters — scripts are plain globals)
         ├── config.js        → PLATFORMS, DAYS, OPTIMAL_TIMES, HASHTAG_SETS
         ├── templates.js     → CONTENT_TEMPLATES
         ├── state.js         → state {}
         ├── generator.js     → generatePostForPlatform(), generateFullCalendar()
         ├── renderer.js      → renderCalendar(), renderPostCard(), escHtml()
         ├── actions.js       → generateCalendar(), regenPost(), editPost() …
         ├── ui.js            → togglePlatform(), showToast(), openModal() …
         └── app.js           → DOMContentLoaded bootstrap
```

---

## 🎨 Design System

| Token | Value | Usage |
|---|---|---|
| `--bg` | `#0f1117` | Page background |
| `--surface` | `#1a1d27` | Cards, sidebar |
| `--surface2` | `#22263a` | Inputs, secondary surfaces |
| `--accent` | `#6c63ff` | Primary brand colour |
| `--accent2` | `#ff6584` | Highlights |
| `--accent3` | `#43e97b` | Success / done states |
| `--ig` | `#e1306c` | Instagram |
| `--tw` | `#1da1f2` | X/Twitter |
| `--li` | `#0a66c2` | LinkedIn |
| `--fb` | `#1877f2` | Facebook |

---

## 📜 License

MIT — free to use, fork, and build upon.

---

*Built for the AI Content Creation Challenge — ContentFlow AI eliminates the repetitive friction of weekly social media planning.*
