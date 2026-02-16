# OpenCode + Gemini Pro OAuth Integration

This repository contains the configuration and documentation for using a **Google Gemini Pro (AI Premium)** subscription within the **OpenCode** CLI/IDE. This setup leverages your existing monthly subscription quota, bypassing the need for per-token API billing via Google Cloud.

---

## Overview

By using the `opencode-gemini-auth` plugin, you can authenticate OpenCode directly with your Google account
* **Gemini 3 Pro:** High-reasoning model for complex architecture and refactoring
* **Gemini 3 Flash:** Fast, low-latency model for quick scripts and documentation
* **Thinking Mode:** Native support for long-context chain of thought processing

---

## Prerequisites

* **OpenCode CLI** (v2.4.0 or higher)
* An active **Google One AI Premium** subscription (Gemini Advanced)
* A terminal with browser access for the initial handshake

---

## Installation & Setup

### Install the Auth Plugin
```bash
opencode plugin add opencode-gemini-auth@latest
```

# Perform the OAuth Handshake

Run the authentication command:

```Bash
opencode auth login --provider google
```
- Select the Google account tied to your Pro subscription

- Grant permissions and return to the terminal once the browser confirms success

# Global Configuration

Update your opencode.json (typically in ~/.config/opencode/):

```JSON
{
  "plugins": ["opencode-gemini-auth"],
  "telemetry": false,
  "models": {
    "default": "gemini-3-pro",
    "thinking": "gemini-3-pro-thinking",
    "fast": "gemini-3-flash"
  },
  "auth": {
    "google": {
      "method": "oauth",
      "persist_session": true
    }
  }
}
```

## Usage
Switch Models: /model gemini-3-pro or /model gemini-3-flash

Thinking Mode: Add the --think flag to any prompt for deep reasoning

Status: Run opencode auth status to verify your subscription link

## Privacy & Security
No API Keys: No sensitive keys are stored in plaintext

Session Storage: Tokens are stored encrypted in your OS keychain
