# waitdeadai Claude Code plugins

Self-hosted marketplace for the open-source Claude Code plugins from
[waitdeadai](https://github.com/waitdeadai). Apache-2.0.

## Why a self-hosted marketplace

The Anthropic community marketplace pipeline at
`claude-plugins-community` shows the same plugin as `Published` in the
submissions dashboard but does not list it in the live `marketplace.json`
for many submitters
([anthropics/claude-plugins-official#1272](https://github.com/anthropics/claude-plugins-official/issues/1272),
[#984](https://github.com/anthropics/claude-plugins-official/issues/984),
[#1292](https://github.com/anthropics/claude-plugins-official/issues/1292),
[#1597](https://github.com/anthropics/claude-plugins-official/issues/1597),
[#1887](https://github.com/anthropics/claude-plugins-official/issues/1887)).
Some submissions have been stuck for two months without resolution.

This marketplace bypasses that pipeline. Plugins listed here are installable
today, directly from this repo.

## Install

```bash
claude plugin marketplace add waitdeadai/claude-plugins
claude plugin install llm-dark-patterns@waitdeadai-plugins
```

To update after a new release:

```bash
claude plugin marketplace update waitdeadai-plugins
claude plugin update llm-dark-patterns@waitdeadai-plugins
```

## Plugins listed here

| Name | Description | Source |
|---|---|---|
| `llm-dark-patterns` | 31-hook out-of-band suite that blocks LLM dark-pattern closeouts. Apache-2.0. | https://github.com/waitdeadai/llm-dark-patterns |

## Adding more plugins

Each plugin needs (at minimum) `.claude-plugin/plugin.json` at the plugin
repo root. Add an entry to `.claude-plugin/marketplace.json` here, push,
and users refresh with `claude plugin marketplace update waitdeadai-plugins`.

## License

Apache-2.0. The marketplace catalog (`.claude-plugin/marketplace.json`)
and this README are themselves under Apache-2.0; each listed plugin
carries its own LICENSE.
