# Quick Start Guide

Get up and running with Meegle MCP skill in 5 minutes!

## Prerequisites Checklist

- [ ] OpenClaw installed
- [ ] Node.js 16+ installed
- [ ] Meegle account with API access
- [ ] Meegle User Key available

## Installation Steps

### 1. Install the Skill

**Option A: Via ClawHub (Recommended)**
```bash
clawhub install meegle-mcp
```

**Option B: From GitHub**
```bash
git clone <your-repo-url> meegle-mcp
cd meegle-mcp
```

### 2. Run Setup

```bash
./scripts/setup.sh
```

Follow the prompts:
- Enter your Meegle User Key
- Choose credential storage method (environment variable recommended)

### 3. Restart OpenClaw

```bash
openclaw restart
```

### 4. Test Installation

```bash
# Check skill is loaded
openclaw skills list | grep meegle

# Try a simple command
openclaw ask "List my Meegle projects"
```

## Your First Commands

### View Projects
```bash
openclaw ask "Show all my Meegle projects"
```

### Create a Task
```bash
openclaw ask "Create a task in Meegle: Update API documentation, due next Friday"
```

### Check Task Status
```bash
openclaw ask "What tasks are assigned to me in Meegle?"
```

### Update Workflow
```bash
openclaw ask "Move the task 'Homepage redesign' to In Progress stage in Meegle"
```

## Troubleshooting

### Can't find user key?
1. Log in to Meegle
2. Go to Settings → API Access
3. Copy your User Key

### Authentication errors?
```bash
# Check if key is set
echo $MEEGLE_USER_KEY

# View logs
openclaw logs --filter=meegle
```

### Skill not loading?
```bash
# Check installed skills
openclaw skills list

# View skill details
openclaw skills info meegle-mcp

# Check OpenClaw logs
openclaw logs --filter=meegle
```

## Next Steps

- Read [SKILL.md](SKILL.md) for all available features
- See [README.md](README.md) for advanced configuration
- Check [CHANGELOG.md](CHANGELOG.md) for updates

## Need Help?

- 📖 [Full Documentation](README.md)
- 🐛 [Report Issues](https://github.com/YOUR_USERNAME/meegle-mcp-skill/issues)
- 💬 [ClawHub Discussion](https://clawhub.ai/)

---

**Happy managing with Meegle + OpenClaw! 🦞📊**
