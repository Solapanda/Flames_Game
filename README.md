# 🔥 FLAMES — The Love Game

A beautifully designed, step-by-step FLAMES love calculator with personalized readings, shareable cards, sound effects, and theme customization. Built entirely with HTML, CSS, and vanilla JavaScript — no frameworks, no dependencies, no backend.

**[▶ Play it live](#)** · *Replace with your deployed URL*

---

## ✨ What is this?

FLAMES is a classic pen-and-paper love game that's been played by kids and teenagers for decades. Enter two names, and the game eliminates letters step by step to reveal your relationship destiny:

- **F** — Friends
- **L** — Lovers
- **A** — Affection
- **M** — Marriage
- **E** — Tension *(reframed from "Enemy" to keep it positive)*
- **S** — BFFs *(reframed from "Sibling" to avoid awkwardness)*

This version turns the simple algorithm into a **visual experience** — animated step-by-step reveals, personalized readings that reference your actual names and game data, unique shareable cards per result, and multiple color themes.

---

## 🎮 Features

**The Game**
- Step-by-step animated reveal showing exactly how the algorithm works
- Playful, randomized narration (8+ variations per step — no two plays feel the same)
- "Skip to result" option for returning players
- Sound effects with toggle (Web Audio API — no external files)
- Confetti celebration scaled to result type (big for Marriage/Lovers, subtle for Tension/BFFs)
- Edge case handling: identical names, zero remaining letters, special characters, XSS protection

**Personalized Readings**
- 384+ unique reading combinations (4 openers × 4 middles × 4 closers × 6 results)
- Readings reference actual names, magic number, round count, and name lengths
- Adapts language for short names vs long names, quick games vs long games
- Meta-aware: after 5+ plays, occasionally acknowledges repeat players

**Shareable Card Customizer**
- Each FLAMES result has a unique background:
  - Friends → Constellation web (interconnected nodes)
  - Lovers → Particle pairs + heat shimmer + echo typography
  - Affection → Soft bokeh orbs (fairy light effect)
  - Marriage → Sacred geometry (flower of life) + Art Deco frame
  - Tension → Fractal lightning veins + spark stars + echo typography
  - BFFs → Confetti scatter (hearts, stars, diamonds, triangles)
- 7 color presets per result (4 universal + 3 result-specific)
- Full custom color picker (background, accent, text)
- Text glow system for readability on any color combination
- Download as PNG or JPG
- Copy text result with site URL for organic sharing

**Customization**
- 4 color themes: Noir & Gold (default), Rose Garden, Peach Dream, Midnight
- 4 font combos: Playful (default), Modern, Elegant, Retro
- Preferences saved in localStorage across sessions
- Lazy font loading (only default fonts load initially, others on demand)

**Technical**
- Single HTML file — zero dependencies, zero build step
- XSS-safe input sanitization
- Clipboard API with `execCommand` fallback for HTTP contexts
- SEO optimized: meta tags, Open Graph, Twitter Cards, Schema.org, static FAQ content
- Accessible: ARIA labels, focus management, keyboard navigation, `aria-live` regions
- Mobile responsive with proper `100dvh` viewport handling
- Confetti canvas created lazily and destroyed after animation

---

## 🚀 Deploy for Free

This is a single HTML file. You can host it anywhere that serves static files:

**Cloudflare Pages** (recommended — unlimited bandwidth, free forever):
1. Push this repo to GitHub
2. Go to [Cloudflare Pages](https://pages.cloudflare.com/)
3. Connect your GitHub repo
4. Build settings: leave everything blank (no build command needed)
5. Deploy

**GitHub Pages:**
1. Go to repo Settings → Pages
2. Set source to `main` branch, `/ (root)` folder
3. Save — your site will be at `https://yourusername.github.io/flames-game`

**Vercel / Netlify:**
1. Import the repo
2. No build settings needed
3. Deploy

---

## 📝 Before You Deploy

1. **Replace the site URL** — Search for `yoursite.pages.dev` in `index.html` and replace all 6 instances with your actual domain
2. **Create an OG image** — Screenshot a result card from the card customizer, resize to 1200×630px, save as `flames-og.png` in the root folder. This is what appears when someone shares your URL on WhatsApp/Instagram/Twitter
3. **Optional: Add analytics** — A single line of [Cloudflare Web Analytics](https://www.cloudflare.com/web-analytics/) (free, no cookies) will tell you how many people play

---

## 🛠 How It Was Built

This project was created through **vibe coding** — an iterative conversation between a human and AI, building feature by feature based on user experience instincts, relationship psychology insights, and developer best practices.

The development went through 6 major iterations:
1. Basic FLAMES calculator with step-by-step reveal
2. Added theme switching, font options, and playful narration
3. Personalized readings with 384+ combinations
4. Reframed Enemy → Tension and Sibling → BFFs based on relationship expert perspective
5. Security hardening, SEO, accessibility, and performance optimization
6. Shareable card customizer with unique backgrounds per result

No frameworks. No build tools. No npm install. Just one HTML file and a lot of iteration.

---

## 📄 License

MIT — do whatever you want with it. If you build something cool on top of this, I'd love to hear about it.

---

*Built with ♥ and a lot of vibe coding*
