# claude-skills-updater

A Claude Code plugin that audits and updates your installed plugins/skills to their latest versions.

## What it does

- Scans all plugins in `~/.claude/plugins/marketplaces/`
- Compares installed versions against latest GitHub releases/tags/commits
- Displays an audit table with status for each plugin
- Interactively proposes updates (with confirmation before each)
- Generates a dated report in `~/.claude/reports/skills-audit/`

## Installation

```bash
claude plugins add dcuenot/claude-skills-updater
```

## Usage

In Claude Code, either:
- Type `/skills-updater`
- Or ask: "check for plugin updates", "update my skills", "audit plugins"

## Example output

```
| Plugin                  | Installed | Latest | Repo                                  | Status           |
|-------------------------|-----------|--------|---------------------------------------|------------------|
| superpowers             | 5.0.2     | 5.0.2  | obra/superpowers                      | Up to date       |
| everything-claude-code  | 1.8.0     | 1.8.0  | affaan-m/everything-claude-code       | Up to date       |
| chrome-devtools-mcp     | 0.20.0    | 0.20.0 | ChromeDevTools/chrome-devtools-mcp    | Up to date       |
| ui-ux-pro-max           | 2.0.1     | 2.5.0  | nextlevelbuilder/ui-ux-pro-max-skill  | Update available  |
| claude-plugins-official | b36fd4b   | b36fd4b| anthropics/claude-plugins-official    | Up to date       |
```

## Prerequisites

- [GitHub CLI](https://cli.github.com/) (`gh`) installed and authenticated
- Plugins installed via git in `~/.claude/plugins/marketplaces/`

## License

MIT
