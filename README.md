# Synchestra AI Marketplace

Claude Code marketplace for plugins published by [Synchestra.io](https://synchestra.io).

## Install

Add this marketplace to Claude Code once:

```
/plugin marketplace add https://github.com/synchestra-io/ai-marketplace
```

Then install any plugin from it:

```
/plugin install synchestra-cli@synchestra-io
/plugin install spec-studio@synchestra-io
```

## Plugins

| Plugin | Install | Repository |
|---|---|---|
| `synchestra-cli` | `/plugin install synchestra-cli@synchestra-io` | [ai-plugin-synchestra](https://github.com/synchestra-io/ai-plugin-synchestra) |
| `specscore-cli` | `/plugin install specscore-cli@synchestra-io` | [ai-plugin-specscore](https://github.com/synchestra-io/ai-plugin-specscore) |
| `spec-studio` | `/plugin install spec-studio@synchestra-io` | [spec-studio](https://github.com/synchestra-io/spec-studio) |

### `synchestra-cli`

Wraps the [`synchestra` CLI](https://github.com/synchestra-io/synchestra) as agent skills, slash commands, and hooks. One skill per CLI command; token-efficient; progressively loaded. The natural install path after the CLI binary itself.

### `specscore-cli`

Wraps the [`specscore` CLI](https://github.com/synchestra-io/specscore) as agent skills. Teaches AI agents how to use `specscore` for spec navigation, linting, and lifecycle operations. Pairs with `spec-studio` for the full authoring experience.

### `spec-studio`

AI skills for spec-driven development as a project-level studio — ideate, design, and (on the roadmap) plan, build, verify, recap, review, ship. Gates implementation on lint-clean SpecScore artifacts and user approval. Works standalone with Claude Code; pairs with Synchestra Hub for remote execution.

## Why a meta-marketplace

Each plugin lives in its own repository (`ai-plugin-*`). This marketplace is a thin index that lists them, so a single `marketplace add` gives users all Synchestra-published plugins. Plugins retain independent release cadence, independent CI, and independent ownership. See [ADR-0001](https://github.com/synchestra-io/synchestra/blob/main/spec/decisions/0001-extract-ai-plugin.md) in the synchestra repo for the reasoning behind this structure.

## Contributing a plugin

External plugins are not accepted into this marketplace at this time — it is reserved for Synchestra-published plugins. Third parties are encouraged to publish their own marketplace; Claude Code supports multiple marketplaces per user.

## License

MIT — see [LICENSE](LICENSE).

## Outstanding Questions

- Distribution branding (`marketplace.synchestra.io` CNAME) — deferred pending first external consumer.
- Plugin naming convention across multiple plugins — partially resolved; revisit when a third plugin is added.
