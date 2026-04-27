# Project Configuration

## Skills (113 active — extras in `.claude/skills-archive/`)

### Engineering Quality Skills (4) — code-level quality, snapshotted from upstream
Self-contained, no plugin/network dependency — travel with the repo.
- **emil-design-eng** — Emil Kowalski's animation & UI polish philosophy: animation decision framework (when *not* to animate), motion taste, required Before/After/Why review table format
- **vercel-web-design-guidelines** — terse `file:line` review for Vercel WIG (a11y, focus, forms, animation, typography, performance, hydration, dark mode, i18n, anti-patterns)
- **vercel-react-best-practices** — 70 React/Next.js perf rules across 8 categories (waterfalls, bundle, server perf, re-render, rendering, JS perf, advanced)
- **vercel-react-native-skills** — 36 React Native/Expo rules (FlashList virtualization, Reanimated GPU patterns, Pressable, Expo image, safe areas, monorepo native deps); only triggers on RN/Expo work

### Designer Skills (72) — design, build, deliver
- **Design Research (10)** — personas, empathy maps, journey maps, interviews, usability testing
- **Design Systems (8)** — tokens, components, accessibility, theming, documentation
- **UX Strategy (8)** — competitive analysis, design principles, experience mapping, alignment
- **UI Design (9)** — color systems, typography, layout grids, responsive, dark mode
- **Interaction Design (7)** — micro-interactions, animations, state machines, gestures, error handling
- **Prototyping & Testing (8)** — wireframes, heuristic evaluation, A/B testing, user flows
- **Design Ops (7)** — critique, handoff specs, sprint planning, QA checklists, workflows
- **Designer Toolkit (6)** — rationale, presentations, case studies, UX writing, adoption
- **Figma (7)** — `figma-use` (mandatory prereq), generate-design, implement-design, generate-library, code-connect, create-design-system-rules, create-new-file
- **Frontend Design (1)** — distinctive, production-grade UI code (Anthropic official)
- **shadcn/ui (1)** — Radix UI + Tailwind CSS component patterns

> **Optional visual-style packs** (not bundled): `high-end-visual-design`, `minimalist-ui`, `industrial-brutalist-ui`, `stitch-design-taste`, `design-taste-frontend`, `redesign-existing-projects`. Add to `.claude/skills/` per project if a specific aesthetic direction is needed.

### Inclusive Design Skills (37) — accessibility, inclusion, cognitive a11y
Moderate selection optimized for agency frontend delivery. Niche/specialty skills archived to `.claude/skills-archive/` — restorable via `git mv` when needed.
- **Cognitive Accessibility (7)** — cognitive load, plain language, wayfinding, memory, error recovery, simplify, review
- **Inclusive Interaction (8)** — keyboard nav, gestures, touch targets, motion sensitivity, multi-modal, feedback, design-flow, audit
- **Accessible Content (7)** — alt text, headings, forms, links, structure, readable content, review
- **Inclusive Personas (4)** — generate, disability-inclusive personas, inclusive user stories, scenario map
- **Adaptive Interfaces (6)** — color independence, flexible typography, information density, responsive accessibility, user preferences, specify
- **Accessibility Decisions (5)** — compliance mapping, decision documentation, tradeoff analysis, handoff, review

## Agents (5 — auto-activate)
Just talk naturally. Claude picks the right agent based on your task. **New designers should start by saying hello to Unicorn.**
- **unicorn** — studio lead & project director; greets newcomers, reads PRD/WBS, tracks project stage, routes to the right specialist. Ask it to be **instructor** (explains every step) or **operator** (just runs the workflow).
- **designer-copilot** — senior design partner; hands-on design thinking, reviews, prototype iteration
- **ui-designer** — visual & interaction design specialist
- **design-system-architect** — components, tokens, theming
- **design-reviewer** — QA, heuristics, accessibility checks

Additional specialist agents (ux-strategist, design-researcher, interaction-designer, design-ops-lead) live in `.claude/agents-archive/` if a project needs deeper specialist routing.

### Project layout (used by Unicorn)
- `./project/brief/` — drop the PRD, WBS, and any reference materials here
- `./project/STATE.md` — current project stage, decisions, next step (Unicorn reads & updates)

## Default Skill Routing

When skills overlap, follow these defaults unless the user explicitly asks for a different one:

- **Animation, motion, UI polish, transitions, micro-interactions (implementation/review)** → default to `emil-design-eng`. It has a decision framework (when *not* to animate), specific opinionated values with reasoning, and a required `Before | After | Why` review table format. Other skills (`interaction-design--animation-principles`, `interaction-design--micro-interaction-spec`) are only used when the user explicitly names them or asks for a generic principles primer / formal spec document.
- **Motion accessibility (vestibular safety, prefers-reduced-motion, photosensitivity)** → `inclusive-interaction--motion-sensitivity` always runs alongside Emil for any motion work — it's harm prevention, not taste, and is non-negotiable.
- **Code-level UI review (a11y, forms, hydration, dark mode, anti-patterns)** → `vercel-web-design-guidelines` for the file-by-file checklist pass.
- **React/Next.js performance** → `vercel-react-best-practices`. **React Native/Expo perf** → `vercel-react-native-skills`.
- **Bold aesthetic direction / building a new screen from scratch** → `frontend-design`.

## How Skills Layer Together
Designer skills build the system. Inclusive skills extend it for accessibility. Use together:
1. Design gestures → then design gesture alternatives
2. Build color system → then audit for color independence
3. Create personas → then expand with disability dimensions
4. Define animations → Emil for the motion taste, motion-sensitivity for the safety pass
5. Write component spec → then verify keyboard navigation
6. Create typography scale → then ensure flexible typography
7. Design layouts → then audit responsive accessibility

## How to Use
- Skills load automatically from `.claude/skills/`
- Commands available as slash commands from `.claude/commands/`
- Agents auto-activate from `.claude/agents/`
- MCP servers (Puppeteer, Chrome DevTools) configured in `.mcp.json`
- Run `./setup.sh` on a new machine to install marketplace plugins

## Project Conventions
- Adapt all design outputs to the project's existing stack and conventions
- Prioritize accessibility (WCAG AA minimum) in all design decisions
- Use design tokens over raw values whenever possible
- Design for keyboard, screen reader, and reduced motion from the start
- Include disability as a natural dimension in all personas and user stories
