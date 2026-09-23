# Cynthia Ugwu — Portfolio Website 🎨

A clean, minimal, and interactive **product designer portfolio** built with vanilla HTML, CSS, and JavaScript. Features smooth scroll animations, a custom mouse follower, and hover-triggered image reveals on project cards.

---

## ✨ Features

- 🖱️ **Custom Mouse Follower** — A morphing mini-circle that follows cursor movement with dynamic squish/stretch scaling
- 🖼️ **Hover Image Reveal** — Project cards reveal tilting images on mouse hover with GSAP-powered rotation
- 🚂 **Locomotive Scroll** — Buttery smooth scrolling experience throughout the page
- 📐 **Minimalist Dark Design** — Black background with high-contrast typography for a premium, modern aesthetic
- 📱 **Responsive Layout** — Adapts cleanly across different screen sizes

---

## 🗂️ Project Structure

```
cynthiaugwu-main/
├── index.html       # Main HTML structure
├── style.css        # Core styles & layout
├── loco.css         # Locomotive Scroll override styles
├── script.js        # GSAP animations & interaction logic
├── plug.png         # Project image — The Plug
├── ixperience.png   # Project image — Ixperience
├── hudu.png         # Project image — Hudu
└── README.md        # You are here!
```

---

## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| HTML5 | Page structure & semantics |
| CSS3 | Styling, layout, dark theme |
| JavaScript (Vanilla) | Interactivity & DOM manipulation |
| [GSAP 3](https://greensock.com/gsap/) | Smooth animations & mouse effects |
| [Locomotive Scroll](https://locomotivemtl.github.io/locomotive-scroll/) | Smooth scroll & scroll-based triggers |
| [Remix Icons](https://remixicon.com/) | Icon library |

---

## 🚀 Getting Started

### Option 1 — Direct Open (Quick)
Simply open `index.html` in your browser.

> ⚠️ **Note:** Some scroll-based animations may not trigger correctly over `file://` protocol. Use Option 2 for the full experience.

### Option 2 — Local Server (Recommended)
```bash
# Using live-server (Node.js required)
npx live-server

# Or using Python
python -m http.server 3000
```
Then visit `http://localhost:3000` (or the port shown in your terminal).

---

## 🎬 How the Animations Work

### 🖱️ Mouse Follower (`circleChaptaKaro`)
Tracks mouse position and applies a dynamic `scaleX`/`scaleY` based on movement speed — making the cursor blob stretch as it moves fast and snap back to a circle when idle.

```js
xscale = gsap.utils.clamp(0.8, 1.2, dets.clientX - xprev);
yscale = gsap.utils.clamp(0.8, 1.2, dets.clientY - yprev);
```

### 🖼️ Project Card Hover Reveal
Each `.elem` project card listens for `mousemove` to:
1. Show a hidden project image at the cursor's position
2. Rotate it based on horizontal mouse speed — faster = more tilt

```js
rotate: gsap.utils.clamp(-20, 20, diffrot * 0.5)
```

---

## 📄 Sections

| Section | Description |
|---|---|
| **Hero** | Name, title, location (Toronto), freelance availability |
| **Featured Work** | The Plug, Ixperience, Hudu — 2022 projects |
| **About Me** | Short bio with a "Let's talk" CTA |
| **Subscribe** | YouTube channel plug |
| **Footer** | Social links (Dribbble, Instagram, LinkedIn, Twitter) |

---

## 🎨 Design Inspiration

This portfolio is inspired by **[Cynthia Ugwu](https://cynthiaugwu.com/)** — a Toronto-based product designer known for her visually bold and playful design style.

---

## 📝 License

This project is a **clone/study project** built for learning purposes. All design credits go to the original designer, Cynthia Ugwu.

---

<div align="center">Made with ❤️ for learning web animations</div>