# ClaudePilot for OpenClaw

**The AI-guided way to get started with OpenClaw.**

ClaudePilot gets you from zero to a fully configured AI agent with memory and smart model routing. No developer required. Pick your path:

## Two Paths, Same Destination

| | ClaudePilot (Free) | ClaudePilot Pro ($100/mo) |
|---|---|---|
| **Guide** | [CLAUDEPILOT-OPENCLAW.md](CLAUDEPILOT-OPENCLAW.md) | [CLAUDEPILOT-PRO.md](CLAUDEPILOT-PRO.md) |
| **How it works** | Paste prompt into free Claude | Use Claude Code from terminal |
| **Who does the work** | You, with Claude guiding you | Claude Code does it for you |
| **Who runs the commands** | You | Claude Code |
| **Who debugs errors** | You (with help) | Claude Code |
| **Time to working bot** | A few hours | One afternoon |
| **Best for** | Learners who want to understand every step | People who want results fast |
| **Cost** | Free | $100 for one month (cancel anytime) |

Both paths end at the same place: a fully configured OpenClaw agent with persistent memory (Mnemo Cortex) and smart model routing (Sparks Router).

## Free Path — ClaudePilot

1. Open [claude.ai](https://claude.ai) (free account works)
2. Start a new conversation
3. Copy the entire contents of [CLAUDEPILOT-OPENCLAW.md](CLAUDEPILOT-OPENCLAW.md)
4. Paste it into Claude
5. Follow the conversation — Claude guides you through everything

You'll learn how every piece works because you're building it yourself, with Claude as your mentor.

## Pro Path — ClaudePilot Pro

1. Subscribe to [Claude Max](https://claude.ai) ($100/month)
2. Install Claude Code: `curl -fsSL https://claude.ai/install.sh | bash`
3. Open terminal, type `claude`
4. Follow the instructions in [CLAUDEPILOT-PRO.md](CLAUDEPILOT-PRO.md)

Claude Code installs, configures, and tests everything. You tell it what you want, it builds it. One month is all you need — everything it builds keeps running after you cancel.

## What Gets Built (Both Paths)

- **OpenClaw** — the agent framework running your bot(s)
- **Channel connections** — Telegram, Discord, WhatsApp, or web chat
- **Mnemo Cortex v2** — persistent memory so your bot remembers across conversations
- **Sparks Router** — smart model routing that cuts costs without cutting quality
- **Systemd services** — everything starts on boot, runs 24/7
- **Backups and monitoring** — daily snapshots, alerts if something breaks

## Who This Is For

- You've heard about OpenClaw and want to try it
- You want a personal AI assistant but don't know where to start
- You have an old laptop gathering dust and want to put it to work
- You're not a developer and that's totally fine

---

## Level Up Your Setup

Now that you have Claude Code running, here are two open-source tools we built to make your agent setup even better. Both are optional. Both are free. Both were built because we needed them.

### Mnemo Cortex — Memory for Your Agent

Your AI agent forgets everything between sessions. Every conversation starts from scratch. Mnemo Cortex fixes that.

Persistent memory with DAG-based summary lineage. SQLite-backed. Works with any LLM. Your agent remembers what it learned, what it decided, and why.

- 3,000+ messages tested across two live agents
- 429 summaries with 80% active compaction
- Six weeks of continuous recall

**→ [github.com/GuyMannDude/mnemo-cortex](https://github.com/GuyMannDude/mnemo-cortex)**

### Sparks Router — Stop Burning Tokens

Not every task needs an expensive model. A heartbeat check doesn't need Opus. A quick lookup doesn't need Gemini Pro.

Sparks Router automatically routes tasks to the right model tier. Heavy reasoning goes to Smart models. Code gen goes to Utility. Background work goes to Free. Your budget stays controlled.

Three tiers. Automatic classification. Budget caps. You set the ceiling, the router handles the rest.

**→ [github.com/GuyMannDude/sparks-router](https://github.com/GuyMannDude/sparks-router)**

---

*Both projects are part of [Project Sparks](https://projectsparks.ai) — a creative technology studio building open-source AI infrastructure in Half Moon Bay, CA.*

## Related Projects

| Project | What It Does |
|---------|-------------|
| [OpenClaw](https://github.com/GuyMannDude/openclaw) | The agent framework — runs your bots |
| [Mnemo Cortex](https://github.com/GuyMannDude/mnemo-cortex) | Memory system — your bots remember things |
| [Sparks Router](https://github.com/GuyMannDude/sparks-router) | Model routing — keeps costs down without sacrificing quality |

## About

Built by [Project Sparks](https://projectsparks.ai). Born from the belief that everyone should be able to run their own AI agents — not just developers.

---

*"Most people talk about building AI agents. You actually did it."*
