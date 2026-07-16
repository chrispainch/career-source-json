# career-source-json

This repository publishes a machine-readable career profile as JSON for direct download, inspection, and ingestion into LLM workflows.

The canonical file is [`career-source.json`](./career-source.json).

## Purpose

This repo is intended to make career data easy to use in tools such as Codex, Claude Code, and other LLM-assisted workflows. Typical usage includes:

- downloading the raw JSON file
- cloning the repository and reading the file locally
- supplying the file as structured context for agents, prompts, or retrieval pipelines

## File Format

The top-level structure of `career-source.json` currently includes:

- `version`
- `profile`
- `organizations`
- `cross_cutting`
- `derived`

At a high level:

- `profile` contains core identity and summary information
- `organizations` contains organization- and role-level career history
- `cross_cutting` contains skills, tools, themes, and domain information that span multiple roles
- `derived` contains synthesized artifacts such as resume variants and career highlights

Consumers should expect additive changes over time. Field names and structure may evolve as the dataset expands, but the goal is to keep the overall format stable and practical for machine consumption.

## Intended Use

This dataset is designed for:

- LLM context ingestion
- career profile analysis
- resume and narrative generation workflows
- downstream transformation into other structured formats

If you are building against this file programmatically, prefer tolerant parsing and avoid assuming that only the current fields will exist.

## Update Cadence

This repository is updated as the source career data evolves. Updates are published incrementally rather than on a fixed release schedule.

## Consumption

Recommended consumption pattern:

1. Fetch `career-source.json`.
2. Parse it as UTF-8 JSON.
3. Treat the current repository version as the latest published artifact unless a separate versioning scheme is introduced.

## Stability Notes

- The canonical filename is `career-source.json`.
- Additive changes are more likely than breaking renames, but both remain possible as the schema matures.
- Consumers should not assume strict backwards compatibility across all historical revisions.

## License

No license has been added yet. Reuse rights should be considered undefined until a `LICENSE` file is included in this repository.
