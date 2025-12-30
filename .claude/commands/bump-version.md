---
name: bump-version
description: Bump a plugin version in the marketplace and update README
arguments:
  - name: plugin
    description: The plugin name to update (e.g., bug-fix, feature-dev, code-explain)
    required: true
  - name: version
    description: The new version number (e.g., 1.0.3)
    required: true
---

Bump the version of plugin "{{plugin}}" to "{{version}}" in this marketplace.

Steps:
1. Update the `version` field for the "{{plugin}}" plugin in `.claude-plugin/marketplace.json`
2. Update the version in the README.md table for the "{{plugin}}" plugin to "{{version}}"
3. Increment the marketplace `metadata.version` in `.claude-plugin/marketplace.json` by 0.0.1

Do NOT commit or push - just make the file changes.
