# Project Instructions

## Overview

This is an AI-assisted development template. It provides a shared configuration for multiple AI coding tools (Claude Code, Aider, Gemini) so that project context and instructions are defined once in this file and consumed everywhere.

## Repository Structure

```
.
├── AGENTS.md              # Shared project instructions (this file)
├── CLAUDE.md              # Claude Code entry point (references AGENTS.md)
├── .aider.conf.yml        # Aider configuration (reads AGENTS.md)
├── .gemini/
│   └── settings.json      # Gemini configuration (reads AGENTS.md)
├── README.md              # Project readme
└── LICENSE                # GPL v3
```

## How It Works

- **Claude Code** reads `CLAUDE.md`, which includes this file via `@AGENTS.md`.
- **Aider** reads this file directly via the `read: AGENTS.md` setting in `.aider.conf.yml`.
- **Gemini** reads this file via the `contextFileName` setting in `.gemini/settings.json`.

This means any instructions added here are automatically available to all three tools.

## Getting Started

To use this template for your own project:

1. Clone or fork this repository.
2. Add your source code, dependencies, and tooling.
3. Update this file with project-specific instructions (tech stack, conventions, commands, etc.).

## Customization Guide

Replace the sections below with details relevant to your project.

### Tech Stack

- Always check the web for the latest version of each dependency before installing or upgrading.
- **Python**: 3.14 or later
- **React / Next.js**: Use the latest available version
- **.NET Aspire**: 13 or later
- **.NET**: 10 or later, prefer the latest version regardless of whether it is STS or LTS

### Development Commands

<!-- Document how to build, test, lint, and run the project. Example:
```
npm install          # Install dependencies
npm run build        # Build the project
npm test             # Run tests
npm run lint         # Lint the code
```
-->

### Code Conventions

<!-- Describe naming conventions, file organization patterns, or style guidelines. -->

### Testing

<!-- Describe the test framework, how to run tests, and expectations for test coverage. -->

### Architecture

<!-- Provide a high-level overview of the system architecture, key modules, and data flow. -->
