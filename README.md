# Aryan Shekhawat · Terminal Portfolio

An interactive portfolio that behaves like a command prompt. Visitors type commands (or click the highlighted ones) to explore my projects, research, experience and skills.

**Live:** https://aryan07-portfolio.vercel.app

![Portfolio preview](og-image.png)

## Try these commands

| Command | What it shows |
|---|---|
| `about` | Who I am and what I care about |
| `projects` / `projects 1` | Things I've built, with details and links |
| `open <project>` | Opens a project's live demo (e.g. `open codeatlas`) |
| `experience` | DRDO AI/ML internship |
| `research` | Papers and ongoing work |
| `skills` | Languages, frameworks, tools |
| `education`, `achievements`, `certifications` | Grades, hackathons, courses |
| `resume` | Opens my résumé (PDF) |
| `tour` | A guided walkthrough, press Enter for each stop |
| `neofetch`, `contact`, `help`, `clear` | Quick summary, links, command list |
| `milli` | About my little assistant (`milli sleep`, `wake`, `mute`, `unmute`, `hide`, `show`) |
| `intro` | Replays Milli's introduction |

Shortcuts: `Tab` autocompletes, `↑ ↓` recalls history, `Ctrl+L` clears, `Esc` skips Milli's intro. The sun/moon button switches light and dark mode.

## Meet Milli

Milli is a small assistant who lives in the corner of the page.

- She introduces herself when you arrive, over a blurred glass background, then walks to her corner. Click anywhere or press `Esc` to skip.
- Click or tap her to boop her. Tickle her leaf for a different reaction.
- She offers help with clickable `help` and `intro` buttons.
- If you stop exploring, she suggests commands you haven't opened yet.
- If you leave her alone for a minute she falls asleep, and you have to boop her to wake her up.
- She has no LLM and no API. Every line is pre-written, and a small state machine decides when to say it.

## How it's built

- A single static `index.html` with plain HTML, CSS and JavaScript. No framework, no build step, no backend, no API keys.
- Live weather in the status bar comes from the free [Open-Meteo](https://open-meteo.com) API.
- Hosted on Vercel and redeployed automatically on every push to `main`.
- The browser remembers a few things locally (`localStorage`): whether you've visited before, your light/dark choice, and whether you muted or hid Milli. Nothing is sent to a server.

## Project structure

```
aryan-portfolio/
├── index.html     # the whole site
├── og-image.png   # link preview card used when the URL is shared
├── README.md
└── resume.pdf     # served by the `resume` command
```

## Run locally

Open `index.html` in a browser. That's it.

## Customize

Content lives near the top of the script in `index.html`: contact links in `ME`, projects in `PROJ`, and each command's text in `CMDS`.

To update the résumé, replace `resume.pdf` with the new file (keep the exact name) and bump the version in `resumeURL` (for example `resume.pdf?v=2`) so browsers don't show a cached copy.

Milli's lines live in the `Ls` object inside the `Milli` block of the script, and the commands she nudges visitors toward are in the `ORDER` list.

## Contact

[aryanshekhawat1947@gmail.com](mailto:aryanshekhawat1947@gmail.com) · [LinkedIn](https://www.linkedin.com/in/aryanshekhawat07/) · [GitHub](https://github.com/Aryan-1947)
