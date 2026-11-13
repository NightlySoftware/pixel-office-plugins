# Pixel Office plugins

[Pixel Office](https://pixel-office.app) is a live office where a team meets, talks and ships, and where each coding agent session shows up as a small robot next to its owner. This repository is its Claude Code plugin marketplace.

## Install

In Claude Code:

```
/plugin marketplace add NightlySoftware/pixel-office-plugins
/plugin install pixel-office@pixel-office-app
```

Then run `/pixel-office:connect`. It opens your browser to approve this computer and adds a small hook to the coding agents it finds. Nothing keeps running in the background.

Without the plugin, the same thing is one command in any terminal:

```
npx @pixel-office/connect
```

## Commands

| Command | What it does |
| --- | --- |
| `/pixel-office:connect [office]` | Pair this computer with your office and connect your coding agents |
| `/pixel-office:status` | Show the paired office and which agents report to it |
| `/pixel-office:disconnect` | Remove the Pixel Office hooks |

## What is shared

The agent type, a hashed session id, its state (working, waiting for you, ended), a fixed label such as "Editing files", and the repository name. Prompts, code, file names, commands and paths never leave your computer. See the [privacy policy](https://pixel-office.app/privacy).

## Plans

Free for up to 3 people. Team is USD 10 a month for each person who used the office that month. See [pixel-office.app](https://pixel-office.app/#pricing).

The plugin calls the [`@pixel-office/connect`](https://www.npmjs.com/package/@pixel-office/connect) package from npm. Questions: hi@pixel-office.app.
