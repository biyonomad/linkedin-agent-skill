# OpenAI / Codex compatibility layer

This directory adds OpenAI-compatible Agent Skills without modifying the original Claude implementation in `skills/` or `.claude-plugin/`.

## Layout

- `.agents/skills/li-*/SKILL.md`: OpenAI/Codex-compatible copies of the eleven LinkedIn skills.
- Supporting files such as `hooks.json`, `rubric.json`, `slop.json`, `humanize.py`, and `detect.py` stay beside the skill that uses them.

## State

When a writable project filesystem is available, OpenAI-compatible skills use `.linkedin-agent/` for runtime state such as `voice.md`, `plan.md`, and `log.md`.

If persistent filesystem access is unavailable, use the current conversation/project files as state and never claim that a file was written when it was not.

## Compatibility contract

The original Claude files remain untouched. The OpenAI copies preserve the original behavior, approval gates, safety rules, hook data, humanizer scripts, and profile rubric. Claude-style `/li-*` references are expressed as sibling skill references and Claude-specific state paths are made platform-neutral.

## Usage

In Codex, open the repository and invoke the relevant skill by name, for example `li-post`, `li-plan`, or `li-human`.

For ChatGPT environments that support Skills, package or upload an individual folder under `.agents/skills/li-*` with its bundled resources.
