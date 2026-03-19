# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Kilox.nvim — a personal Neovim + tmux dotfiles repo based on Kickstart.nvim. Uses `folke/lazy.nvim` for plugin management, bootstrapped in `nvim/init.lua`.

## Setup

```bash
chmod +x install.sh
./install.sh
```

This symlinks `nvim/` to `~/.config/nvim` and `tmux/tmux.conf` to `~/.config/tmux/tmux.conf` (backs up existing configs automatically).

## Formatting

Lua files use StyLua. Config is in `nvim/.stylua.toml`: 160 column width, 2-space indent, single quotes.

```bash
stylua nvim/
```

## Architecture

- `nvim/init.lua` — Entry point. Loads `kilox.options` and `kilox.keymaps`, sets up yank highlight autocommand, bootstraps lazy.nvim, and defines plugin specs (mix of inline specs and external modules from `lua/kilox/plugins/`).
- `nvim/lua/kilox/options.lua` — Core Neovim settings. Leader is Space. Relative line numbers, 2-space indentation, system clipboard.
- `nvim/lua/kilox/keymaps.lua` — Global keymaps (`jk` to escape, `;` for command mode, `tn`/`tj`/`tk` for tab navigation).
- `nvim/lua/kilox/health.lua` — `:checkhealth kilox` module. Validates Neovim >= 0.10 and external tools (git, make, unzip, rg).
- `nvim/lua/kilox/plugins/` — Each file returns a lazy.nvim plugin spec table:
  - `lsp.lua` — LSP via Mason + nvim-lspconfig + blink.cmp. Servers: gopls, ts_ls, eslint, ruff, pyright, lua_ls. Formatters: stylua, goimports, gofumpt, prettier, prettierd.
  - `ai.lua` — claudecode.nvim integration (with snacks.nvim terminal).
  - `telescope.lua` — Fuzzy finder with fzf-native. Custom nav: C-j/C-k, C-t for tab open.
  - `neo-tree.lua` — File explorer with grug-far search integration (press `z` to search in directory).
  - `debug.lua` — DAP setup for Go (Delve) via mason-nvim-dap.
  - `greeter.lua` — Custom startup screen with ASCII art.
  - `lint.lua`, `gitsigns.lua`, `autopairs.lua`, `indent_line.lua` — Standard plugin configs.
- `tmux/tmux.conf` — Tmux config. Prefix is C-a, vim-style copy mode, vim-tmux-navigator for C-h/j/k/l pane switching.

## Conventions

- All Lua config lives under `nvim/lua/kilox/`. Plugin specs go in `nvim/lua/kilox/plugins/`.
- Plugin specs can be inline in `init.lua` (simple ones) or in separate files under `plugins/` (complex ones).
- Formatting uses conform.nvim (configured in `init.lua`): stylua for Lua, goimports/goimports-reviser/gofumpt for Go, prettierd/prettier for web languages.
- Linting uses nvim-lint (`lint.lua`): markdownlint for markdown, eslint for JS/TS.
