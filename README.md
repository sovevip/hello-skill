# hello-skill

A minimal example skill for the Local-Auto-Agent skill system.

## Install

```
install_skill("sovevip/hello-skill")
```

## What it adds

| Tool | Description |
|------|-------------|
| `say_hello` | Say hello to someone |

## Skill structure (L1 → L2 → L3)

```
hello-skill/
├── skill.json   # L1: metadata, always loaded (~100 tokens)
├── guide.md     # L2: usage guide, loaded when triggered
└── tools.py     # L3: tool code, loaded on demand
```

## Create your own skill

1. Copy this repo as template
2. Edit `skill.json` — name, tools, description
3. Edit `guide.md` — usage scenarios and examples
4. Edit `tools.py` — your tool functions
5. Push to GitHub → users run `install_skill("your-name/your-skill")`
