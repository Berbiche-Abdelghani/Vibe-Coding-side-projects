# LOGICA · 3D Portfolio

**Wanna know us?** Click the name and find out.

An immersive, scroll-driven 3D portfolio for **LOGICA**, a scientific club themed around cybersecurity and computer science. The club name breaks into six physical 3D letters, and as you scroll down through them, each one reveals a value we stand for.

![HTML5](https://img.shields.io/badge/HTML5-single%20file-e34f26?logo=html5&logoColor=white)
![three.js](https://img.shields.io/badge/three.js-r128-000000?logo=threedotjs&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-vanilla-f7df1e?logo=javascript&logoColor=black)
![Build](https://img.shields.io/badge/build%20step-none-6d28d9)
![Made with](https://img.shields.io/badge/vibe%20coded%20with-Claude-06b6d4)

## Try it

Download this repository (**Code → Download ZIP**) or clone it, then open `index.html` in a modern browser. No installation and no build step.

Prefer a local server?

```bash
python -m http.server 8000
# then visit http://localhost:8000
```

An internet connection is needed for three.js and the fonts, which load from CDNs. Because the site is a single static file, you can host it anywhere, such as GitHub Pages, Netlify or Vercel.

## What LOGICA stands for

| Letter | Stands for | Our line |
|:------:|------------|----------|
| **L** | Logic | We train our minds to think like a machine, logically. |
| **O** | Optimization | Faster, leaner, cleaner. We optimize our code and our minds. |
| **G** | Growth | Today's mistakes are tomorrow's lessons. We grow together. |
| **I** | Innovation | We turn curiosity into creativity. We innovate. |
| **C** | Cyber security | The art of protecting systems. We secure the future. |
| **A** | Artificial intelligence | Machines that learn, minds that lead. |

## The experience

1. **Intro.** A glossy white studio room with the club name and a blinking "wanna know us ?" prompt.
2. **Click the name.** Electric waves, sparks and lightning charge up, then the name breaks into six extruded, bevelled letters.
3. **Physics.** The letters are kicked, tumble under gravity and bounce, denting metal platforms and sending out shock rings.
4. **Scroll.** The camera descends through the letters. Each one reveals a panel with its meaning, and the scene turns from the white room into a dark void as you go deeper.
5. **Find us.** The final section links to our channels. Click one and the page plays an exit animation with a circular wipe before the link opens.

## Features

- Real-time 3D scene with soft shadows, studio-style reflections and ACES tone mapping
- Scroll-driven camera, progress bar and automatic light/dark theme based on depth
- Letter physics with damped bounces and platform dents
- 2D lightning and spark effects layered over the WebGL canvas
- Animated link transition with a fallback if pop-ups are blocked
- A **Plain version** button, and an automatic plain layout when WebGL is unavailable or reduced motion is requested
- Responsive layout with safe-area support for phones
- One HTML file, no framework, no bundler

## Hidden easter eggs 🥚

There are **eleven** easter eggs hiding in the page. Some are for keyboards, some for clicks, one is for the curious who open the console, and one waits in the source code. Stuck? Press the **Hints** button in the top-left corner: it gives a riddle for each egg and keeps count of the ones you have found.

No spoilers here. Happy hunting!

## Tech stack

| Layer | Choice |
|-------|--------|
| 3D | [three.js](https://threejs.org) r128 (loaded from cdnjs) |
| Language | Vanilla JavaScript, HTML5, CSS3 |
| Fonts | Space Grotesk and JetBrains Mono (Google Fonts) |
| Effects | Canvas 2D overlay for lightning, sparks and code rain |

## Make it your own

Fork it and swap in your own club, team or school.

| What | Where |
|------|-------|
| Letter titles and sentences | The `L` array at the top of the main script |
| Social links | The `#lrow` block near the end of the `<body>` |
| Colors | CSS variables such as `--primary` and `--accent` in `:root` |
| Easter egg hints | The `H` array in the easter egg script at the end of the file |

## Project structure

```text
.
├── index.html   # the whole site: markup, styles, 3D scene, interactions
├── PROMPT.md    # the prompts used to vibe-code the project
└── README.md
```

## Accessibility and compatibility

- The intro is a real `button` with a descriptive label, and a screen-reader heading describes the club.
- Panels announce changes through an `aria-live` region.
- If you prefer reduced motion, you automatically get the plain version.
- Works in current versions of Chrome, Edge, Firefox and Safari on desktop and mobile. WebGL is required for the 3D experience.

## Built by vibe coding

This site was built by talking to an AI assistant instead of writing every line by hand. Curious how? The full master prompt and every follow-up round are in [PROMPT.md](PROMPT.md), so you can reproduce it, remix it or build something better.

## Feedback

Found a bug or have an idea? Open an issue or a pull request. All contributions are welcome.

## Join LOGICA

- Telegram community: <https://t.me/+BBQlQgQssy84OTJk>
- Telegram channel: <https://t.me/+XAwKO-6PTfxmYzU8>
- Instagram: <https://www.instagram.com/logica.cx>
- Facebook: <https://www.facebook.com/LOGICAcx>
- Email: <logica.cx.club@gmail.com>

## Author

Built by **Abdelghani Berbiche** · [GitHub](https://github.com/Berbiche-Abdelghani)

## License

Released under the MIT License.
