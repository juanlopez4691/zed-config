# Zed Config

My personal configuration files for Zed.

## 🚀 Quick Start

1. Clone this repo to your Zed config directory:
   ```bash
   git clone https://github.com/juanlopez4691/zed-config ~/.config/zed
   ```
2. Restart Zed or reload config (`cmd-shift-p` → `zed: reload config`).

## 🤖 AI Setup

This config expects the following environment variables to be available to Zed:

- `CONTEXT7_API_KEY` — used by the Context7 MCP server
- `ZED_GITHUB_MCP_TOKEN` — used by the GitHub Copilot MCP server
- `BRAVE_SEARCH_API_KEY` — used by the Brave Search MCP server

If you use `direnv` or shell-based environment loading, make sure Zed is launched in a context where these variables are available.

This config also includes a custom `opencode` agent server. Make sure the `opencode` binary is installed and available on the `PATH` that Zed sees, especially when launching Zed as a GUI app.

The configured Copilot models in `settings.json` must also be available in your current Zed build and GitHub Copilot plan. If a model is unavailable, select an available one in Zed and update the config accordingly.

Current-file test tasks in `tasks.json` use `${ZED_FILE}`. If those tasks do not work as expected in your setup, verify how Zed expands that path and adjust the task command if needed.

## 🧩 Intelephense

This config uses a local Intelephense license file path in `settings.json`.

If Intelephense licensing does not work when Zed is launched as a GUI app, replace `~/intelephense/licence.txt` with an absolute path, since `~` expansion may not always work as expected in that environment.

## 📁 What's Included

- `settings.json` — Editor settings, themes, UI tweaks
- `keymap.json` — Custom keybindings (Vim-inspired + custom)
- `tasks.json` — Laravel Sail, Pest/PHPUnit, Bun, Pint, Composer, and Sail helper tasks
- `.gitignore` — Excludes Zed state files (.mdb prompts, cache, etc.)

## 📄 License

MIT - Feel free to use and adapt!
