# ⚙️ Setup Guide

Get your environment ready before the workshop starts. This should take **10–15 minutes** max.

---

## 1. Install Git

### macOS
```bash
# Check if Git is already installed
git --version

# If not, install via Homebrew
brew install git

# Or download the installer:
# https://git-scm.com/download/mac
```

### Windows
Download and run the installer from: https://git-scm.com/download/win  
Use all default settings — make sure **Git Bash** is included.

### Linux (Ubuntu/Debian)
```bash
sudo apt update && sudo apt install git -y
```

---

## 2. Configure Git (everyone does this once)

```bash
git config --global user.name "Your Name"
git config --global user.email "your@email.com"

# Set VS Code as your default editor (optional but recommended)
git config --global core.editor "code --wait"
```

Verify it worked:
```bash
git config --list
```

---

## 3. Authenticate with GitHub

You have two options. **Pick one.**

### Option A — GitHub CLI (recommended for this workshop)

**Install:**
```bash
# macOS
brew install gh

# Windows — download from: https://cli.github.com

# Linux
sudo apt install gh -y
```

**Authenticate:**
```bash
gh auth login
# → Choose: GitHub.com
# → Choose: HTTPS
# → Authenticate with browser: Yes
```

**Verify:**
```bash
gh auth status
```

### Option B — SSH Key

```bash
# Generate a key
ssh-keygen -t ed25519 -C "your@email.com"
# Press Enter through all prompts to accept defaults

# Copy the public key
cat ~/.ssh/id_ed25519.pub
```

Then go to: **GitHub → Settings → SSH and GPG keys → New SSH key**  
Paste the key and save.

**Test it:**
```bash
ssh -T git@github.com
# Should say: Hi <username>! You've successfully authenticated.
```

---

## 4. Install GitHub Desktop (optional — for the GUI portion)

Download from: https://desktop.github.com  
Sign in with your GitHub account when prompted.

---

## 5. Install VS Code (if you don't have a code editor)

Download from: https://code.visualstudio.com  

Recommended extensions for this workshop:
- **GitLens** — supercharges the Git view in VS Code
- **Git Graph** — visualizes branch history

---

## ✅ Pre-workshop Checklist

Run these commands and make sure they all return without errors:

```bash
git --version          # should be 2.x or higher
gh auth status         # should show your GitHub username
```

If anything is broken, flag it before the workshop starts — we'll sort it out.
