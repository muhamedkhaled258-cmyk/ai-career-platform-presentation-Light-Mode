<div align="center">

# 🚀 Expert Partner AI — Interactive Pitch Deck

### A cinematic, keyboard-driven presentation experience built with React

*Not your average slideshow. A living, breathing product story.*

[![React](https://img.shields.io/badge/React-18-61DAFB?style=for-the-badge&logo=react&logoColor=black)](https://react.dev)
[![JavaScript](https://img.shields.io/badge/JavaScript-ES6+-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![CSS3](https://img.shields.io/badge/CSS3-Animations-1572B6?style=for-the-badge&logo=css3&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/CSS)
[![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](#-license)
[![PRs Welcome](https://img.shields.io/badge/PRs-Welcome-ff69b4?style=for-the-badge)](#-contributing)

<br/>

**[✨ Live Demo](#)** · **[📖 Documentation](#-table-of-contents)** · **[🐛 Report a Bug](../../issues)** · **[💡 Request a Feature](../../issues)**

</div>

<br/>

## 📌 About The Project

**Expert Partner AI** is a **19-slide interactive deck** rendered entirely in React — no external presentation library, no PowerPoint exports, no PDF embeds. Every slide is a real, live component. That means when this deck showcases a product feature, it doesn't show a *screenshot* of it — it **embeds the actual working UI in a live `iframe`**, right inside the slide.

Built for a real-world pitch: an **AI-powered career platform** that helps developers go from *"stuck job seeker"* to *"job-ready professional"* — covering CV analysis, career path recommendations, job matching, mock interviews, credits system, and more.

> 💬 *"We are not just preparing developers… we are building the bridge between talent and opportunity."*

<br/>

## 🎬 Preview

<div align="center">

| Title Slide | Live Feature Demo | Comparison Table |
|:---:|:---:|:---:|
| 🌌 Gradient hero + team reveal | 🖥️ Embedded live product UI | 📊 Competitive landscape |

*(Drop your own GIF/screenshot here — e.g. `docs/preview.gif`)*

</div>

<br/>

## ✨ Features

<table>
<tr>
<td width="50%">

### 🎮 Navigation & Controls
- ⌨️ **Full keyboard support** — `→` / `Space` / `Enter` to advance, `←` to go back
- 🖱️ **Scroll-to-navigate** with smart debouncing (no accidental double-jumps)
- 🗂️ **Slide-out sidebar** with jump-to-slide navigation
- ⛶ **True fullscreen mode** (toggle with `F`)
- 🔢 Live slide counter (`Slide X / 19`)

</td>
<td width="50%">

### 🎨 Visual Experience
- 🌠 **Animated intro splash** on load
- 🧊 **Glassmorphism** pillar cards
- 🎞️ Staggered **fade/slide-up entrance** animations
- 🌈 Gradient-clipped typography for hero text
- 📱 Fully responsive split & image layouts

</td>
</tr>
<tr>
<td width="50%">

### 🖼️ Dynamic Slide Types
- `title` — Hero intro with animated team reveal
- `split` — Text + live iframe/image side-by-side
- `image` — Full-bleed visual storytelling
- `pillars` — Icon-driven concept grid
- `table` — Competitive comparison matrix
- `vision` — Closing statement slide

</td>
<td width="50%">

### 🔌 Live Product Integration
- 🌐 **Real embedded `iframe` demos** of the actual product (CV Analysis, Career Roadmap, Job Matching, Mock Interview, Dashboard, Admin Panel...)
- ⏳ Lazy-loaded iframes with entrance transitions
- 🚫 Zero static screenshots for feature slides — everything is *live*

</td>
</tr>
</table>

<br/>

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| **UI Library** | [React](https://react.dev) 18 (Hooks — `useState`, `useEffect`, `useRef`) |
| **Styling** | Custom CSS3 (`index.css`) — Glassmorphism, gradients, keyframe animations |
| **State Management** | Local component state (no Redux needed — deck is self-contained) |
| **Interactivity** | Native DOM APIs — `Fullscreen API`, `wheel` & `keydown` event listeners |
| **Content Embeds** | `<iframe>` live demo injection |
| **Build Tooling** | Compatible with [Vite](https://vitejs.dev) or [Create React App](https://create-react-app.dev) |

<br/>

## 🚀 Getting Started

### Prerequisites

```bash
node >= 18.x
npm >= 9.x   (or yarn / pnpm)
```

### Installation

```bash
# 1. Clone the repository
git clone https://github.com/<your-username>/expert-partner-ai-deck.git

# 2. Navigate into the project
cd expert-partner-ai-deck

# 3. Install dependencies
npm install

# 4. Run the dev server
npm run dev        # if using Vite
# or
npm start           # if using Create React App
```

The deck will be live at `http://localhost:5173` (Vite) or `http://localhost:3000` (CRA). 🎉

### Build for Production

```bash
npm run build
```

<br/>

## ⌨️ Controls Cheat Sheet

| Action | Key / Gesture |
|---|:---:|
| Next slide | `→` &nbsp;`Space`&nbsp; `Enter` &nbsp; or &nbsp; scroll down |
| Previous slide | `←` &nbsp; or &nbsp; scroll up |
| Toggle fullscreen | `F` |
| Open slide navigator | Click `☰ Menu` |
| Jump to any slide | Click a slide title in the sidebar |

<br/>

## 📁 Project Structure

```
📦 expert-partner-ai-deck
├── 📂 src
│   ├── App.jsx          # Main deck engine — slide data, navigation logic, renderers
│   ├── index.css         # Animations, glassmorphism, gradients, layout system
│   └── main.jsx          # React entry point
├── 📂 public
├── package.json
└── README.md
```

<br/>

## 🧩 How the Deck Engine Works

The entire presentation is driven by a single **`slidesData`** array — each object describes one slide's `type` (`title`, `split`, `image`, `pillars`, `table`, `vision`) and its content. A single `renderSlideContent()` switch statement maps each type to its layout, meaning **adding a new slide is just adding a new object** — no new components required for standard layouts.

```js
{
  id: 20,
  type: 'split',
  title: 'Your New Feature',
  subtitle: 'A short description of the feature.',
  points: ['Point one', 'Point two', 'Point three'],
  iframe: 'https://your-live-demo-url.com', // or image: '...'
}
```

Bump `TOTAL_SLIDES`, drop it in the array, done. ✅

<br/>

## 🎯 Roadmap

- [ ] Add swipe/touch gesture support for mobile
- [ ] Slide transition variants (fade, cube, zoom)
- [ ] Speaker notes / presenter mode
- [ ] Export deck to PDF
- [ ] Dark / light theme toggle
- [ ] Autoplay mode with configurable timing

See [open issues](../../issues) for the full list of proposed features.

<br/>

## 🤝 Contributing

Contributions make the open-source community amazing. Any contributions are **greatly appreciated**.

1. Fork the project
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

<br/>

## 👥 Team

<div align="center">

| | | | |
|:---:|:---:|:---:|:---:|
| Mohamed Ali | Mohamed Khaled | Ibrahim Mostafa | Mahmoud Mostafa |
| Abdullah Khairy | Amira Nasser | Yomna Hesham | Rania Essam |

</div>

<br/>

## 📄 License

Distributed under the **MIT License**. See `LICENSE` for more information.

<br/>

<div align="center">

### ⭐ If this project inspired you, consider giving it a star!

*Built with ❤️, React, and a lot of `cubic-bezier` easing curves.*

</div>
