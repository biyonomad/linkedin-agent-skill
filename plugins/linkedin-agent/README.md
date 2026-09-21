# LinkedIn Agent plugin

Portable Agent Plugins package for ChatGPT and Codex.

This package contains eleven skills and no MCP server, credentials, authentication code, browser automation, or automatic LinkedIn publishing.

## Included skills

- li-post
- li-comment
- li-reply
- li-profile
- li-plan
- li-human
- li-carousel
- li-repurpose
- li-dm
- li-inbox
- li-audit

## Local repository marketplace

This repository also includes `.agents/plugins/marketplace.json`.

Add the repository as a marketplace:

```bash
codex plugin marketplace add biyonomad/linkedin-agent-skill --ref main
```

Then restart the ChatGPT desktop app, open Plugins, select the LinkedIn Agent marketplace source, and install **LinkedIn Agent**.

Local marketplace support depends on the ChatGPT/Codex surface and rollout. Web and mobile surfaces may not expose local marketplace sources.

## Behavior

The plugin is skills-only. It does not connect to LinkedIn and does not publish automatically. Approval gates and manual-posting behavior from the original project are preserved.
