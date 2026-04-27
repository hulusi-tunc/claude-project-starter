```
 ___________ _
  \/                    __/   .::::.-'-(/-/)
                     _/:  .::::.-' .-'\/\_`*******          __ (_))
        \/          /:  .::::./   -._-.  d\|               (_))_(__))
                     /: (""""/    '.  (__/||           (_))__(_))--(__))
                      \::).-'  -._  \/ \\/\|
              __ _ .-'`)/  '-'. . '. |  (i_O
          .-'      \       -'      '\|
     _ _./      .-'|       '.  (    \\                         % % %
  .-'   :      '_  \         '-'\  /|/      @ @ @             % % % %
 /      )\_      '- )_________.-|_/^\      @ @ @@@           % %\/% %
 (   .-'   )-._-:  /        \(/\'-._ `.     @|@@@@@            ..|........
  (   )  _//_/|:  /          `\()   `\_\     |/_@@             )'-._.-._.-
   ( (   \()^_/)_/             )/      \\    /                /   /
    )  _.-\\.\(_)__._.-'-.-'-.//_.-'-.-.)\-'/._              /
.-.-.-'   _o\ \\\     '::'   (o_ '-.-' |__\'-.-;~ ~ ~ ~ ~ ~~/   /\
          \ /  \\\__          )_\    .:::::::.-'\          '- - -|
     :::''':::::^)__\:::::::::::::::::'''''''-.  \                '- - -
    :::::::  '''''''''''   ''''''''''''':::. -'\  \     C. SWANSIGER
_____':::::_____________________________________\__\______________________
```

<h1 align="center">Unicorn Skills</h1>

<p align="center">
  <em>A Claude Code template that walks in with <strong>112 skills</strong>, <strong>27 commands</strong>, <strong>4 agents</strong>, and <strong>2 MCP servers</strong> already saddled up.</em>
</p>

<p align="center">
  <a href="#quick-start"><img alt="Quick start" src="https://img.shields.io/badge/quick%20start-2%20minutes-FF6B9E?style=flat-square"></a>
  <img alt="Skills" src="https://img.shields.io/badge/skills-112-7AB8FF?style=flat-square">
  <img alt="Commands" src="https://img.shields.io/badge/commands-27-FFB347?style=flat-square">
  <img alt="Agents" src="https://img.shields.io/badge/agents-4-C58BFF?style=flat-square">
</p>

---

A template repository with **112 skills**, **27 commands**, **4 agents**, and **2 MCP servers** pre-configured for Claude Code.

## What's Inside

```
.claude/
  settings.json        # All plugins enabled
  skills/              # 112 skills (bundled, works on any machine)
  commands/            # 27 slash commands
  agents/              # 4 designer agents (auto-activate)
.mcp.json              # Puppeteer + Chrome DevTools MCP servers
CLAUDE.md              # Project instructions for Claude
setup.sh               # One-time machine setup (installs plugins)
```

## Quick Start

### Option A: Use as GitHub Template
1. Click **"Use this template"** on GitHub
2. Clone your new repo
3. Start Claude Code in the project directory
4. Everything works automatically

### Option B: Clone directly
```bash
git clone https://github.com/hulusi-tunc/unicorn-skills.git my-new-project
cd my-new-project
rm -rf .git && git init  # Fresh git history
```

### Optional: Install Marketplace Plugins
```bash
./setup.sh
```
> Skills work without this step (they're bundled in `.claude/skills/`). The setup script adds marketplace plugin support for updates.

### Chrome DevTools MCP (one-time per machine)
```bash
npm install -g chrome-devtools-mcp
```

## Agents (Auto-Activate)

Just talk naturally -- Claude picks the right agent automatically.

| Agent | Role | Skills Loaded |
|-------|------|--------------|
| **designer-copilot** | Main design partner (5 modes: thinking, review, prototype, brainstorm, spec) | 22 |
| **ui-designer** | Colors, typography, grids, responsive, shadcn/ui | 11 |
| **design-system-architect** | Components, tokens, theming, accessibility | 8 |
| **design-reviewer** | Heuristic evaluation, QA, accessibility review | 5 |

> Specialist agents (design-researcher, ux-strategist, interaction-designer, design-ops-lead) live in `.claude/agents-archive/` — restore with `git mv` if you need deeper specialist routing.

## Skills (112)

### Designer Skills (65)

| Plugin | Skills | Commands | Description |
|--------|--------|----------|-------------|
| design-research | 10 | 4 | Personas, empathy maps, journey maps, interviews |
| design-systems | 8 | 3 | Tokens, components, accessibility, theming |
| ux-strategy | 8 | 3 | Competitive analysis, principles, metrics |
| ui-design | 9 | 4 | Colors, typography, grids, responsive, dark mode |
| interaction-design | 7 | 3 | Animations, state machines, gestures, error handling |
| prototyping-testing | 8 | 4 | Wireframes, heuristics, A/B testing, user flows |
| design-ops | 7 | 3 | Handoffs, sprints, critiques, QA, workflows |
| designer-toolkit | 6 | 3 | Rationale, presentations, case studies, UX writing |
| frontend-design | 1 | — | Distinctive, production-grade UI code (Anthropic) |
| shadcn-ui | 1 | — | Radix UI + Tailwind + React Hook Form + Zod |

### Inclusive Design Skills (58)

| Plugin | Skills | Description |
|--------|--------|-------------|
| cognitive-accessibility | 11 | Cognitive load, plain language, wayfinding, memory, focus |
| inclusive-interaction | 10 | Keyboard nav, gestures, voice, touch targets, motion sensitivity |
| accessible-content | 10 | Alt text, headings, forms, links, tables, readable content |
| inclusive-personas | 9 | Disability personas, assistive tech scenarios, ability spectrum |
| adaptive-interfaces | 9 | Color independence, flexible typography, simplified views |
| accessibility-decisions | 9 | Compliance mapping, debt tracking, tradeoff analysis, handoff |

### How Skills Layer Together

Designer skills build the system. Inclusive skills extend it for accessibility:

| Design (build) | → | Inclusive (extend) |
|---------------|---|-------------------|
| gesture-patterns | → | gesture-alternatives |
| color-system | → | colour-independence |
| user-persona | → | disability-inclusive-personas |
| animation-principles | → | motion-sensitivity |
| component-spec | → | keyboard-navigation |
| typography-scale | → | flexible-typography |
| layout-grid | → | responsive-accessibility |
| ux-writing | → | plain-language-design |
| handoff-spec | → | accessibility handoff |
| feedback-patterns | → | multi-sensory feedback |

## MCP Servers

| Server | What it does |
|--------|-------------|
| **Puppeteer** | Navigate, click, type, screenshot, scrape any page |
| **Chrome DevTools** | Inspect DOM, debug CSS, console, network, accessibility |

Plus built-in: **WebSearch** and **WebFetch** (always available).

## How to Update This Template

Edit files locally and push:
```bash
cd unicorn-skills
# Make changes (add skills, update agents, etc.)
git add -A
git commit -m "what you changed"
git push
```

Next time you click "Use this template", it creates from the latest version.

## How to Update Projects Created From This Template

Projects created from the template are independent repos. They don't auto-update. To pull updates:

### First time (one-time setup)
```bash
cd my-existing-project
git remote add template https://github.com/hulusi-tunc/unicorn-skills.git
git fetch template
git merge template/main --allow-unrelated-histories
```

### After that
```bash
git fetch template
git merge template/main
```

### Quick reference

| Action | Command |
|--------|---------|
| **Update template** | Edit, commit, push from `unicorn-skills/` |
| **New project** | "Use this template" on GitHub (gets latest) |
| **Update old project** | `git fetch template && git merge template/main` |

## Credits
- Designer skills by [MC Dean](https://marieclairedean.substack.com/) via [Owl-Listener/designer-skills](https://github.com/Owl-Listener/designer-skills)
- Inclusive design skills by [MC Dean](https://marieclairedean.substack.com/) via [Owl-Listener/inclusive-design-skills](https://github.com/Owl-Listener/inclusive-design-skills)
- Frontend design skill by [Anthropic](https://github.com/anthropics/claude-plugins-official)
- shadcn-ui skill by [Giuseppe Trisciuoglio](https://github.com/giuseppe-trisciuoglio/developer-kit)
