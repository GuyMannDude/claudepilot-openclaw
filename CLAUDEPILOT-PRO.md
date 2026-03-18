# ClaudePilot Pro: The Power Setup

**Let Claude Code build your entire setup. $100/month Claude Max subscription. One month is all you need.**

---

## Free vs Pro

| | ClaudePilot (Free) | ClaudePilot Pro ($100/mo) |
|---|---|---|
| Claude guides you through setup | Yes | — |
| Claude Code builds it for you | — | Yes |
| You run the commands | You | Claude Code |
| You debug the errors | You (with help) | Claude Code |
| Time to working bot | A few hours | One afternoon |
| Cost | Free | $100 for one month |

**Free ClaudePilot** walks you through it. **ClaudePilot Pro** has Claude Code do it for you. Both end at the same place — a fully configured OpenClaw agent with memory and smart routing.

The difference is who types the commands.

---

## Phase 1 — Subscribe and Install Claude Code

### Get Claude Max

1. Go to [claude.ai](https://claude.ai)
2. Sign up or log in
3. Subscribe to **Claude Max** ($100/month)
4. You can cancel anytime — one month is enough to get everything built

### Install Claude Code

Open your terminal and run:

```
curl -fsSL https://claude.ai/install.sh | bash
```

Close and reopen your terminal, then type:

```
claude
```

That's it. You now have the most powerful AI coding agent on your machine. It can read files, write files, run commands, install software, configure services — everything a developer would do, but it does it for you.

"If free Claude is a consultant who tells you what to do, Claude Code is the contractor who shows up and does the work."

---

## Phase 2 — Tell Claude Code What You Want

Paste this into your Claude Code session:

```
I want to set up a complete OpenClaw AI agent stack. Here's what I need:

- [describe your bot: personal assistant / business tool / research helper / etc.]
- Channels: [Telegram / Discord / WhatsApp / web chat]
- Budget for AI models: [free only / up to $20/month / up to $50/month]
- This machine runs: [Mac / Ubuntu / Windows with WSL]
- I want: [one bot / two bots with different purposes]

Please install and configure everything:
1. OpenClaw (agent framework)
2. My bot(s) with channels connected
3. Mnemo Cortex v2 (memory system)
4. Sparks Router (cost optimization)
5. Systemd services for uptime
6. Backup scripts

Build it all. Test each piece. Tell me when it's done.
```

Claude Code will ask a few clarifying questions, then get to work. You watch.

---

## Phase 3 — CC Installs OpenClaw

Claude Code handles everything:

- Checks your Node.js version, installs or upgrades if needed
- Installs OpenClaw globally
- Runs the onboarding wizard with your preferences
- Configures the gateway daemon
- Verifies `openclaw status` shows everything green

**What you do:** Answer any questions CC asks. Otherwise, sit back.

**Checkpoint:** CC will confirm the gateway is running and show you the status output. If something went wrong, CC already fixed it.

---

## Phase 4 — CC Sets Up Your Bot

Claude Code configures your first agent:

- **Model selection** — CC recommends the best option for your budget:
  - Free: `nvidia/nemotron-3-super-120b-a12b:free` via OpenRouter
  - Budget: Gemini or OpenRouter with a small deposit
  - Quality: Claude API or comparable
- **Channel connection** — CC walks through the bot token setup for your chosen platform (Telegram, Discord, etc.) and wires it into OpenClaw
- **System prompt** — CC writes a solid starter personality based on what you told it in Phase 2
- **Skills** — CC installs relevant skill packs for your use case
- **Testing** — CC sends a test message and confirms the bot responds

**Checkpoint:** Your bot is live on your chosen channel. Send it a message from your phone. It answers. Done.

"Your agent is running. That took about 15 minutes. A developer would've spent a few hours on this."

---

## Phase 5 — CC Installs Mnemo Cortex v2

This is where your bot gets a brain that persists across conversations.

Claude Code:

- Clones the [Mnemo Cortex v2](https://github.com/GuyMannDude/mnemo-cortex-v2) repo
- Installs dependencies
- Configures the SQLite database (nothing extra to install — it's just a file)
- Sets up the **watcher daemon** — monitors for new conversations and processes them into memories
- Sets up the **refresher daemon** — periodically consolidates and summarizes stored memories
- Creates **systemd services** for both daemons so they start automatically on boot
- Patches the OpenClaw **bootstrap hook** so your bot loads its memory context at the start of every conversation
- Ingests any existing sessions so nothing is lost
- Tests recall: starts a new conversation, asks the bot about something from a previous chat

### Don't Fear the /new!

"Here's the thing people get wrong: they think starting a new conversation means the bot forgets everything. It doesn't. Mnemo Cortex lives outside the chat window. Every time a new conversation starts, the bot's memories get loaded in. Start fresh conversations freely. The context carries over. That's the whole point."

**Checkpoint:** CC confirms the watcher and refresher are running, shows you the systemd status, and demonstrates memory recall across a `/new` conversation boundary.

---

## Phase 6 — CC Installs Sparks Router

This is how you stop overpaying for AI.

Claude Code:

- Clones the [Sparks Router](https://github.com/GuyMannDude/sparks-router) repo
- Installs and configures it
- Sets up **model tiers** based on your budget:
  - **Tier 1 (free/cheap):** Handles simple messages — greetings, time zones, basic questions
  - **Tier 2 (mid):** Handles normal conversations, summaries, everyday tasks
  - **Tier 3 (premium):** Handles complex reasoning, planning, creative work
- Configures **budget caps** — daily and monthly limits so a runaway conversation can't drain your wallet
- Wires OpenClaw to route all messages through Sparks Router instead of directly to a provider
- Tests classification — sends test messages at different complexity levels and shows you which tier handled each one

### Stop Burning Tokens on Heartbeats

"Without routing, every message — even 'hey' — hits your most expensive model. That's like taking a taxi to your mailbox. Sparks Router sends 'hey' to the free model and saves the premium model for when it actually matters."

**Checkpoint:** CC shows you the router logs. Simple messages go to Tier 1. Complex ones go to Tier 3. Your budget cap is set. Money saved from day one.

---

## Phase 7 — CC Hardens Everything

Claude Code locks it all down for production:

### Auto-start on boot
- Creates systemd services for: OpenClaw gateway, Mnemo Cortex watcher, Mnemo Cortex refresher, Sparks Router
- Enables all services so everything comes back after a reboot
- Tests with a simulated reboot sequence

### Backup scripts
- Creates a backup script that snapshots:
  - `~/.openclaw/workspace/` (bot configs and personality)
  - Mnemo Cortex SQLite database (all memories)
  - Sparks Router config (tier definitions and budget caps)
- Sets up a daily cron job to run the backup
- Stores backups locally with a 30-day rotation
- "If you have an external drive or cloud storage, tell CC and it'll send backups there too."

### Monitoring
- Sets up a simple health check script that verifies all services are running
- Configures alerts if something goes down (email, Discord webhook, or Telegram — your choice)
- "You'll know something is broken before your bot's users do."

### Budget alerts
- Configures Sparks Router to send you a notification when you hit 80% of your monthly budget
- Hard stop at 100% — bot switches to free-tier-only mode instead of going over budget
- "Set it and forget it. Your wallet is safe."

**Checkpoint:** CC reboots the services, confirms everything comes back up, shows you the backup cron schedule, and triggers a test alert. Everything is production-ready.

---

## Phase 8 — The Decision

Everything is built and running:

- Your OpenClaw agent is live on your chosen channels
- Mnemo Cortex gives it persistent memory across conversations
- Sparks Router keeps your costs optimized
- Systemd services keep everything running 24/7
- Backups run daily
- Monitoring alerts you if anything breaks

**Now you choose:**

### Option A: Cancel Claude Max
- Everything you built keeps running — it doesn't depend on Claude Max
- Your bot, memory system, and router are all self-contained
- You save $100/month going forward
- If you need CC again later, resubscribe for a month

### Option B: Keep Claude Max
- Use Claude Code for ongoing maintenance, upgrades, and new features
- Add more bots, new channels, custom skills
- CC can troubleshoot issues as they come up
- "It's like having a developer on retainer"

### Option C: Downgrade to Claude Pro ($20/month)
- You lose Claude Code but keep regular Claude access
- Use the free ClaudePilot guide for any future manual changes
- Good middle ground

**There's no wrong answer.** Everything CC built is yours. It runs on your machine, with your API keys, on your terms. The subscription was for the builder, not the building.

"You built a complete AI agent stack in one afternoon. The $100 was the best investment you'll make this year."

---

## Quick Reference

After setup, here are the commands you'll actually use:

```bash
# Check if everything is running
openclaw status

# View bot logs
openclaw logs

# Restart everything after a problem
sudo systemctl restart openclaw-gateway
sudo systemctl restart mnemo-watcher
sudo systemctl restart mnemo-refresher
sudo systemctl restart sparks-router

# Manual backup
~/scripts/openclaw-backup.sh

# Check Sparks Router spend
sparks-router stats
```

## Need Help Later?

- Paste the free [ClaudePilot guide](CLAUDEPILOT-OPENCLAW.md) into Claude for guided troubleshooting
- Resubscribe to Claude Max for a month and let CC fix things directly
- Check the repos for updates:
  - [OpenClaw](https://github.com/GuyMannDude/openclaw)
  - [Mnemo Cortex v2](https://github.com/GuyMannDude/mnemo-cortex-v2)
  - [Sparks Router](https://github.com/GuyMannDude/sparks-router)

---

*"Most people talk about building AI agents. You actually did it."*
