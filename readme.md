# Cynthia Ugwu — Portfolio Clone 🎨

> A pixel-faithful clone of [Cynthia Ugwu's](https://cynthiaugwu.com/) award-winning product designer portfolio, rebuilt to study advanced CSS/JS animation techniques.

![HTML](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white)
![CSS](https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)
![GSAP](https://img.shields.io/badge/GSAP-88CE02?style=flat&logo=greensock&logoColor=black)

---

## ✨ Features

- 🖱️ **Velocity-aware cursor** — Custom blob cursor that squishes/stretches based on real-time mouse speed
- 🖼️ **Hover image reveal** — Project cards reveal a tilting image that rotates proportional to horizontal mouse speed
- 🚂 **Locomotive Scroll** — Inertia-based buttery-smooth scrolling across the entire page
- 🎬 **GSAP Timelines** — Coordinated multi-step entrance animations with staggered `Expo.easeInOut` easing
- 🌑 **Dark minimal design** — High-contrast black theme inspired by the original portfolio

---

## 🗂️ Project Structure

```
├── index.html        # Page structure
├── style.css         # Core styles & dark theme
├── loco.css          # Locomotive Scroll overrides
├── script.js         # GSAP animations & interactions
├── plug.png          # Project — The Plug
├── ixperience.png    # Project — Ixperience
└── hudu.png          # Project — Hudu
```

---

## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| HTML5 + CSS3 | Structure & dark theme styling |
| Vanilla JavaScript | DOM manipulation & event handling |
| [GSAP 3](https://greensock.com/gsap/) | Cursor physics & animation timelines |
| [Locomotive Scroll](https://locomotivemtl.github.io/locomotive-scroll/) | Smooth inertia-based scrolling |
| [Remix Icons](https://remixicon.com/) | Icon library |

---

## 🎬 Key Animations Explained

### 🖱️ Cursor Squish Physics
```js
xscale = gsap.utils.clamp(0.8, 1.2, dets.clientX - xprev);
yscale = gsap.utils.clamp(0.8, 1.2, dets.clientY - yprev);
```
Mouse velocity is clamped to a 0.8–1.2 scale range — the faster you move, the more the cursor stretches.

### 🖼️ Hover Image Rotation
```js
rotate: gsap.utils.clamp(-20, 20, diffrot * 0.5)
```
Rotation angle is mapped directly to horizontal mouse delta — fast swipes = sharp tilt.

### 🎬 Entrance Timeline
```js
tl.from("#nav", { y: -10, opacity: 0, duration: 1.5, ease: Expo.easeInOut })
  .to(".boundingelem", { y: 0, duration: 2, stagger: 0.2 })
  .from("#herofooter", { opacity: 0, duration: 1.5 });
```

---

## 🚀 Running Locally

**Option 1 — Direct open**
```
Open index.html in any browser
```

**Option 2 — Local server (recommended for full animation support)**
```bash
npx live-server
```
Then visit `http://localhost:8080`

---

## 🎨 Original Design Credit

This is a **clone built for learning purposes only.**
All design credit goes to **[Cynthia Ugwu](https://cynthiaugwu.com/)** — a Toronto-based product designer.

---

<div align="center">Built to learn · Not for commercial use</div>
