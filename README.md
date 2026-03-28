# Claude Project Starter Pack

A template repository with **63 designer skills** and **27 commands** pre-configured for Claude Code.

## What's Inside

```
.claude/
  settings.json        # All 8 plugins enabled
  skills/              # 63 skills (bundled, works on any machine)
  commands/            # 27 slash commands
CLAUDE.md              # Project instructions for Claude
setup.sh               # One-time machine setup (installs plugins)
```

## Quick Start

### Option A: Use as GitHub Template
1. Click **"Use this template"** on GitHub
2. Clone your new repo
3. Start Claude Code in the project directory

### Option B: Clone directly
```bash
git clone https://github.com/YOUR_USERNAME/claude-project-starter.git my-new-project
cd my-new-project
rm -rf .git && git init  # Fresh git history
```

### Optional: Install Marketplace Plugins
```bash
./setup.sh
```
> Skills work without this step (they're bundled in `.claude/skills/`). The setup script adds marketplace plugin support for updates.

## Included Plugins

| Plugin | Skills | Commands |
|--------|--------|----------|
| design-research | 10 | 4 |
| design-systems | 8 | 3 |
| ux-strategy | 8 | 3 |
| ui-design | 9 | 4 |
| interaction-design | 7 | 3 |
| prototyping-testing | 8 | 4 |
| design-ops | 7 | 3 |
| designer-toolkit | 6 | 3 |

## Keeping Updated

Pull the latest skills from this template:
```bash
git remote add template https://github.com/YOUR_USERNAME/claude-project-starter.git
git fetch template
git merge template/main --allow-unrelated-histories
```

## Credits
Designer skills by [MC Dean](https://marieclairedean.substack.com/) via [Owl-Listener/designer-skills](https://github.com/Owl-Listener/designer-skills).
