# OpenBotX Starter

This is a starter template for [OpenBotX](https://github.com/openbotx/openbotx) — an open-source platform for orchestrating AI agents.

## Quick Start

```bash
# Install OpenBotX
uv tool install openbotx

# Create your project
mkdir my-assistant && cd my-assistant
openbotx init

# Configure
cp .env.example .env
nano .env  # add your API key (ANTHROPIC_API_KEY, OPENAI_API_KEY, etc.)

# Start
openbotx start
```

Your browser opens at `http://localhost:8000`. Default login: `admin` / `admin`.

## Project Structure

```
.
├── config.yml                  # Main configuration
├── .env                        # API keys and secrets (not committed)
├── .env.example                # Template for .env
├── SOUL.md                     # Bot personality and tone
├── USER.md                     # User preferences
├── TOOLS.md                    # Tools reference for the agent
├── AGENTS.md                   # Agent and subagent capabilities
└── workspace/
    ├── HEARTBEAT.md            # Periodic tasks (when heartbeat is enabled)
    ├── memory/
    │   ├── MEMORY.md           # Long-term facts (always loaded)
    │   └── HISTORY.md          # Conversation history (auto-generated)
    └── skills/
        └── meme-creator/       # Example skill
            └── SKILL.md
```

## Configuration

Edit `config.yml` to customize your agent. Key sections:

- **`bot`** — Name and description
- **`credentials`** — API keys, tokens, and secrets (Anthropic, OpenAI, Telegram, AWS, etc.)
- **`providers`** — LLM provider configurations referencing credentials
- **`agents`** — Agent definitions with model, tools, and parameters
- **`image`** — Image generation provider and model
- **`tools`** — Tool-specific settings (web search, exec timeout, workspace restrictions)
- **`channels`** — Telegram integration
- **`storage`** — Local filesystem or AWS S3

All settings can also be edited from the web panel under **Settings**.

## Skills

Skills are Markdown files that teach the agent new capabilities. Place them in `workspace/skills/`:

```
workspace/skills/my-skill/
└── SKILL.md
```

This template includes a **meme-creator** skill as an example. Try it: open the chat and type "create a meme about programming".

See the [Skills documentation](https://github.com/openbotx/openbotx/blob/main/docs/skills.md) for details on creating your own.

## Context Files

These optional files in the project root shape how the agent behaves:

| File | Purpose |
|------|---------|
| `SOUL.md` | Personality, tone, and behavioral guidelines |
| `USER.md` | User preferences and language settings |
| `TOOLS.md` | Tools documentation loaded into agent context |
| `AGENTS.md` | Agent and subagent configuration reference |

Edit them to customize the agent's behavior without touching code.

## Links

- [OpenBotX Repository](https://github.com/openbotx/openbotx)
- [Documentation](https://github.com/openbotx/openbotx/tree/main/docs)
- [PyPI](https://pypi.org/project/openbotx/)

## License

MIT
