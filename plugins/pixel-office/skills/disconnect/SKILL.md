---
name: disconnect
description: Remove the Pixel Office hooks from this computer's coding agents. Use when the user asks to disconnect, stop or remove Pixel Office.
disable-model-invocation: true
allowed-tools: Bash(npx -y @pixel-office/connect@latest disconnect*)
---

# Disconnect from Pixel Office

Run `npx -y @pixel-office/connect@latest disconnect` with the Bash tool. It removes only the Pixel Office hooks and keeps a backup of each file it changed. If the user also wants the stored credential deleted, add `--forget`.

Then tell the user that the office keeps listing this computer until an admin removes it under Linked computers, and that their robots disappear within 30 minutes.
