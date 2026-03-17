# agent-guides

This directory contains guides and helper files for working with AI agents and project-specific instructions.

## Files

### `CLAUDE.md`

The project's instruction file for Claude Code.

The file defines, among other things:

- autonomous decision rules
- requirements for syntax checking and testing
- git safety rules and forbidden commands
- safeguards for external and destructive operations
- guidelines for code comments

It is used as a control file for how the agent should operate in the project.

### `SKILL.md`

A skill definition for bash scripting.

The file contains guidelines for:

- CLI design
- argument handling
- error messages and exit codes
- robust bash structure with `set -euo pipefail`
- validation and script template examples

It is used when you want an agent to follow a clear standard for writing production-quality bash scripts.

### `claude-md-generator.sh`

An interactive bash script that generates a project-specific `CLAUDE.md`.

The script:

- asks questions about the project's language, framework, and test command
- can run interactively or with default values using `--defaults`
- writes the result to `CLAUDE.md` or to a custom path via `--output`

Examples:

```bash
bash claude-md-generator.sh
bash claude-md-generator.sh --defaults
bash claude-md-generator.sh --output ./CLAUDE.md
```

### `README.md`

This file.

It provides a quick overview of the contents of the directory and what each file is used for.

## Purpose

This directory is intended to serve as a small reference library for:

- agent instructions
- reusable rules for code generation
- tools for creating project-specific instruction files
