# OpenCode Workspace

Welcome to the central repository for your OpenCode environment. It is configured to leverage Gemini Pro high reasoning models and integrated across multiple development platforms

---

## Documentation Hub

Use the links below to navigate through the setup of this environment. This allows for easy maintenance and future expansion

### [Core Installation](./install.md)

- **Windows Terminal:** npm and Scoop one-liners
- **IDEs:** Extension links and IDs for VS Code and Google AntiGravity

### [Gemini Pro & OAuth Setup](./GeminiProOAuth.md)

- **Authentication:** Linking your Google One AI Premium subscription
- **Provider Config:** opencode.json settings for Gemini 3 Pro and Thinking Mode
- **Security:** OAuth session management and encrypted token storage

---

## Common Workflow Commands

Quick reference for your development sessions:

| Action | Command |
| :--- | :--- |
| Deep Reasoning | opencode --think "your prompt" |
| Model Switch | /model gemini-3-pro |
| Check Status | opencode auth status |
| Update CLI | npm i -g opencode-ai |

---

## Usage Tips

- Run OpenCode from the project root to ensure it picks up your local context automatically
- If you install new packages, remember to use the shell restart one-liner found in the Installation Guide
- Use the `opencode-antigravity-auth` plugin when working in the cloud to keep your local and remote sessions synchronized

---

## Re-auth Google Account / Troubleshoot

Install Antigravity update
```powershell
npm install -g opencode-antigravity-auth@latest
```

Clear cache (if necessary)
```powershell
Remove-Item -Recurse -Force "$env:LOCALAPPDATA\opencode" -ErrorAction SilentlyContinue
Remove-Item -Recurse -Force "$HOME\.cache\opencode" -ErrorAction SilentlyContinue
Remove-Item "$env:USERPROFILE\.config\opencode\antigravity-accounts.json" -ErrorAction SilentlyContinue
```

Test
```cmd
opencode run "Is my account working?" --model=google/antigravity-gemini-3-pro
```

---
*Maintainer: Jasen Henry*
