# Loopy plugins

Loopy finds what your customers really want and turns it into ads. It researches a brand's customers, surfaces angles to test, writes hooks, and builds Meta ad briefs. All analysis runs on Loopy's servers.

This repo holds the Claude and ChatGPT/Codex plugins: the Loopy MCP server (`https://app.tryloopy.io/api/mcp`) plus a short skill that tells the assistant how to use it. You need a Loopy account; the free plan includes your first brief.


## Install

### Claude (Claude Code, claude.ai, Cowork)

- App: Customize > Plugins > Add > Add marketplace, then paste this repo's URL.
- Claude Code:

```
claude plugin marketplace add lucentwooo/loopy-plugins
claude plugin install loopy@loopy
```

### Codex

```
codex plugin marketplace add lucentwooo/loopy-plugins
```

### Or connect the server directly (no plugin, no skill)

- Claude (pre-filled link): https://claude.ai/customize/connectors?modal=add-custom-connector&connectorName=Loopy&connectorUrl=https%3A%2F%2Fapp.tryloopy.io%2Fapi%2Fmcp
- Claude Code: `claude mcp add --transport http loopy https://app.tryloopy.io/api/mcp`
- Codex:

```
codex mcp add loopy --url https://app.tryloopy.io/api/mcp
codex mcp login loopy
```

## Links

- Privacy: https://tryloopy.io/privacy
- Terms: https://tryloopy.io/terms
- Support: info@tryloopy.io
