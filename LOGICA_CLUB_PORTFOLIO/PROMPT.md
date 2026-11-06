# PROMPT.md · How LOGICA 3D Portfolio was vibe coded

The LOGICA 3D Portfolio was built by describing the experience in plain language to an AI assistant (Claude) and refining it over several rounds. Here are the exact ideas and prompts behind it, so you can reproduce it, remix it or learn from the process.

> The prompts below are cleaned up and condensed for readability. They capture the intent of the original conversation, not every word.

## How to use this file

1. Copy the **Master prompt** into a new chat with a capable AI assistant.
2. Swap in your own content: club or team name, letters and links.
3. Apply the **Follow-up prompts** one at a time, checking the result after each.

## Master prompt

```text
ROLE
You are a senior creative front-end developer who specializes in WebGL and polished motion design.

GOAL
Build a scroll-driven 3D portfolio page for LOGICA, a university scientific club themed around
cybersecurity and computer science. The goal is a memorable first impression for new students.

TECHNICAL CONSTRAINTS
- One self-contained index.html. No framework, no bundler, no build step.
- Vanilla JavaScript and CSS.
- three.js r128 from cdnjs. Fonts: Space Grotesk (headings) and JetBrains Mono (labels),
  both from Google Fonts, with system fallbacks.
- Responsive from 360px phones to large desktops. Respect safe-area insets.
- Light and dark theme driven by CSS variables.

CONCEPT
Each letter of LOGICA stands for a value of the club.
The visitor clicks the name, the name breaks into six physical 3D letters, and the visitor
scrolls down through them to read what each letter means.

EXPERIENCE FLOW
1. Intro: a bright, glossy white studio room. The club name sits in the center with a blinking
   hint: "wanna know us ?". The name is a real button.
2. Click: electric waves ripple behind the name, a 2D canvas overlay draws lightning, and
   sparks fly. Then the name breaks into six separate letters.
3. Physics: the letters are real extruded, bevelled 3D geometry with studio-style reflections
   and soft shadows. They are kicked, tumble under gravity and bounce with damping. Each lands
   on a metal platform with a glowing edge, dents it with a spring effect and emits a shock ring.
4. Scroll: after the letters settle, a 600vh scroll space drives a camera that descends past
   each letter. A thin progress bar runs along the left edge. As the camera goes deeper, the
   scene and the page theme cross-fade from the white room to a dark void with drifting dust.
5. Panels: for each letter, a panel shows a small tag ("L · 01"), a title and one sentence.
6. Finale: a "Find us" section with link pills. Clicking a link plays an exit animation
   (other elements blur out, the clicked pill glows, a circular wipe expands from the click
   point with "Opening ..."), then opens the link in a new tab and restores the page.

CONTENT (the six letters)
L · Logic - We train our minds to think like a machine, logically.
O · Optimization - Faster, leaner, cleaner. We optimize our code and our minds.
G · Growth - Today's mistakes are tomorrow's lessons. We grow together.
I · Innovation - We turn curiosity into creativity. We innovate.
C · Cyber security - The art of protecting systems. We secure the future.
A · Artificial intelligence - Machines that learn, minds that lead.
Keep this content in one array at the top of the script so it is easy to edit.

LINKS (the "Find us" pills)
Telegram community, Instagram, Facebook, Telegram channel, Email (mailto).
Keep them in one HTML block so they are easy to replace.

ACCESSIBILITY AND FALLBACKS
- The intro is a <button> with a descriptive aria-label, plus a visually hidden <h1>.
- Panels use aria-live="polite".
- A visible "Plain version" button switches to a simple readable layout.
- If WebGL is unavailable or the user prefers reduced motion, show the plain version
  automatically and skip all animation.

PERFORMANCE
- Cap the pixel ratio at 2. Reuse geometry and materials. Use additive sprites for particles.

OUTPUT
Return the complete index.html in one code block, with short comments marking each section.
```

## Follow-up prompts

Each round was a short, focused request. The constraint "do not change anything else" kept earlier work intact.

| # | Intent | Prompt (condensed) |
|---|--------|--------------------|
| 1 | Visual polish | "Enhance the design and the animation as much as possible, make it more realistic, keep the same idea." |
| 2 | Links | "Keep only the Telegram, Instagram and Facebook links. Add an exit animation for the links section." |
| 3 | Intro hint | "Add a hint on the intro screen that tells people to click the name." |
| 4 | Easter eggs | "Add some easter eggs to this portfolio. Do not change anything except adding them, and give me notes for each one. Do not change any link or any animation." |
| 5 | Hints and links | "Add hints for each easter egg. Bring back the redirect animation for the links. Only add these links: community, Instagram, Facebook, Telegram, email." |
| 6 | Letter meanings | "Make the letters read L : Logic, O : Optimization, G : Growth, I : Innovation, C : Cyber security, A : Artificial intelligence. Do not touch anything else." |
| 7 | Copywriting | "Give me phrases for each letter" (twice, then picked favorites for the final text). |

<details>
<summary>⚠️ Spoilers: the easter egg prompt details</summary>

The easter egg round asked for small discoverable surprises that need no changes to the 3D scene. In the final project these are:

- A Konami code that triggers a code rain overlay
- Seven fast clicks anywhere as a touch-friendly alternative
- Typed words: `logica`, `sudo`, `hack` and `ctf`
- A console message with a function that reveals a flag
- A second flag hidden in a base64 comment in the page source
- Three clicks on the "Find us" title, which reveals binary text
- Scrolling past the end of the page triggers a "404" message
- The tab title reacts when the visitor leaves or goes idle

A **Hints** button (top left) lists a riddle for each egg and counts the ones the visitor has found, saving progress in `localStorage`.

</details>

## Tips for remixing

- **Rewrite the letters.** Change the acronym, the six titles and the sentences, then keep the physics and camera as they are.
- **Tune the mood.** Ask for a different palette by naming new `--primary` and `--accent` colors, or for a different set of letters, such as a school or team name.
- **Iterate in small steps.** Ask for one change at a time and end with "do not change anything else" to protect work you like.
- **Test the fallbacks.** After every round, check the plain version, a phone-sized window and reduced-motion mode.
- **Make it yours.** Use your own links and texts when you publish your version.
