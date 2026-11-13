---
name: status
description: Show which Pixel Office this computer reports to and which coding agents are connected. Use when the user asks whether Pixel Office is connected or working.
allowed-tools: Bash(npx -y @pixel-office/connect@latest status*)
---

# Pixel Office status

Run `npx -y @pixel-office/connect@latest status` with the Bash tool and summarize its output in a few lines: the office, and each agent with whether it reports to it. If nothing is paired, offer `/pixel-office:connect`.
