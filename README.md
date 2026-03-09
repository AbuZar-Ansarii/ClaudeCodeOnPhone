# Run Claude Code on a Phone (Free)
### Claude Code + OpenRouter Setup Guide

This guide explains how to run **Claude Code** on a mobile device (such as Android using **Termux**) using **OpenRouter** as the API provider.

![download](https://github.com/user-attachments/assets/f377096d-bba0-47b8-af43-cc9bce847133)

---

# Overview

This setup allows you to:

- Run **Claude Code CLI** on a phone
- Use **OpenRouter** as the backend API
- Access **free coding models** (e.g., Qwen Coder)
- Work entirely from the terminal

---

# Requirements

Before starting, ensure you have:

- Android phone
- **Termux** installed
- Internet connection
- An **OpenRouter API key**

Recommended:

- At least **4GB RAM**
- Updated Termux environment

---

# Installation

## 1. Update Termux and Install Dependencies
Update your system packages and install Node.js and Git.
```
pkg update && pkg upgrade -y
pkg install nodejs-lts git -y
```


## 2. Install Claude Code CLI
Install Claude Code globally using npm.

```
npm install -g @anthropic-ai/claude-code
```
## Replace:
```
YOUR_OPENROUTER_API_KEY
```
with your API key:

Get your free api key - https://openrouter.ai

## 3. Configure OpenRouter API
Add the OpenRouter configuration to your shell profile.
```
cat <<EOF >> ~/.bashrc

export ANTHROPIC_BASE_URL="https://openrouter.ai/api/v1"
export ANTHROPIC_API_KEY="YOUR_OPENROUTER_API_KEY_HERE" 
export CLAUDE_CODE_MODEL="qwen/qwen-2.5-coder-32b:free"
EOF
source ~/.bashrc
```


## Starting Claude Code
Launch the Claude Code CLI: 
```
claude
```
You can now start coding and interacting with the AI directly from your terminal.

## Example Usage

Ask coding questions:
```
write a python script to rename files in a folder
```
Generate code:
```
build a simple express API
```
Debug code:
```
fix this javascript error
```
## Recommended Free Models

You can change the model by editing:
```
CLAUDE_CODE_MODEL
```
## Examples:
```
qwen/qwen-2.5-coder-32b:free
deepseek/deepseek-coder:free
meta-llama/llama-3.1-8b-instruct:free
```
# Conclusion

You now have a fully functional Claude Code environment running on your phone using OpenRouter and free models.

## This setup is useful for:

1. Coding on mobile

2 . AI-assisted development

3 . Terminal-based workflows
