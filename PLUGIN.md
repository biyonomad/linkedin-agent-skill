# ChatGPT / Codex plugin package

The installable portable plugin lives in:

```
plugins/linkedin-agent/
```

It follows the Agent Plugins portable package format:

```
plugins/linkedin-agent/
├── plugin.json
└── skills/
    ├── li-post/
    ├── li-human/
    └── ...
```

The repository marketplace is:

```
.agents/plugins/marketplace.json
```

To register the repository marketplace:

```bash
codex plugin marketplace add biyonomad/linkedin-agent-skill --ref main
```

After registration, restart the ChatGPT desktop app and install **LinkedIn Agent** from the marketplace source when local marketplaces are available on your surface.

This package is deliberately separate from the original Claude-compatible `skills/` tree and the repo-local Codex `.agents/skills/` tree so those integrations remain unchanged.
