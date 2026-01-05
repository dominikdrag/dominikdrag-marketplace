# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

This is a Claude Code plugin marketplace that hosts plugin metadata for distribution. Plugins are referenced from external GitHub repositories, not stored locally.

## Architecture

- `.claude-plugin/marketplace.json` - Main manifest file listing all available plugins with their metadata, versions, and GitHub source locations
- `plugins/` - Reserved directory for plugin root (currently empty as plugins are hosted externally)
- Plugins listed here point to external repos (e.g., `dominikdrag/bug-fix`, `dominikdrag/devflow`)

## Adding a New Plugin

1. Add plugin entry to `.claude-plugin/marketplace.json` in the `plugins` array
2. Update `README.md` table with plugin name, description, and version
3. Ensure the source repo is public and contains a valid Claude Code plugin

## Updating Plugin Versions

When bumping a plugin version:
1. Update the `version` field in `.claude-plugin/marketplace.json`
2. Update the version in `README.md` table to match

## Commit Convention

Use [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/):

```
<type>[optional scope]: <description>
```

Types: `feat`, `fix`, `docs`, `chore`, `refactor`

Examples:
- `feat: add new-plugin to marketplace`
- `fix(bug-fix): update version to 1.0.3`
- `docs: update README with installation instructions`
