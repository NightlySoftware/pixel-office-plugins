---
name: connect
description: Connect this computer's coding agents to the user's Pixel Office (pixel-office.app), so each session shows up as a robot in the team's office. Use when the user asks to connect, pair or set up Pixel Office.
argument-hint: "[office-slug]"
allowed-tools: Bash(npx -y @pixel-office/connect@latest*)
---

# Connect to Pixel Office

Pixel Office shows each coding agent session as a small robot next to its owner in the team's office. The agent's hook sends only the agent type, a hashed session id, its state (working, waiting, ended), a fixed label such as "Editing files", and the repository name. Prompts, code, file names, commands and paths never leave the computer.

1. Tell the user, in one or two sentences, what will happen: a browser tab opens to approve this computer, then a small hook is added to the coding agents installed here (Claude Code, Codex, Cursor and others). Nothing keeps running in the background.

2. Run this with the Bash tool and a timeout of 600000 ms, because it waits until the user approves in the browser. If the user named an office, add `--office <slug>`; `$ARGUMENTS` holds it when given.

   ```
   npx -y @pixel-office/connect@latest connect
   ```

3. While it waits, repeat the pairing code and link it printed, so the user can approve from any browser where they are signed in to Pixel Office.

4. When it finishes, report which agents it connected, from its output. Say that the robots appear the next time each agent starts working, and that new Claude Code sessions pick up the hook (this session may not).

If the command fails because Node.js is missing or older than 20, tell the user to install Node.js 20 or later and try again. If it says there is no office, send them to https://pixel-office.app to create one; the Free plan holds up to 3 people.
