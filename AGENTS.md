# Project Instructions

## Overview

This is an AI-assisted development template. It provides a shared configuration for multiple AI coding tools (Claude Code, Aider, Gemini) so that project context and instructions are defined once in this file and consumed everywhere.

## Getting Started

To use this template for your own project:

1. Clone or fork this repository.
2. Add your source code, dependencies, and tooling.
3. Update this file with project-specific instructions (tech stack, conventions, commands, etc.).

## Customization Guide

Replace the sections below with details relevant to your project.

### Tech Stack

Always check the web for the latest version of each dependency before installing or upgrading.
#### Here are some of the common languages I prefer
- **Python**: 3.14 or later
- **React**: Use the latest available version
- **NextJS**: Use the latest available version
- **ReactRouter**: Use the latest available version
- **ShadCN**: Use the latest available version
- **.NET Aspire**: 13 or later
- **.NET**: 10 or later, prefer the latest version regardless of whether it is STS or LTS

### Workflow

Always pause after presenting a plan and ask clarifying questions before proceeding to build. Do not assume intent or make guesses about requirements — if anything is unclear or ambiguous, ask the user for clarification instead of just trying things. It is better to ask one extra question than to build the wrong thing and have to redo it.

### Development Methodology

Use Behavior-Driven Development (BDD) when creating solutions. When building a new feature, write the spec tests first — before writing any implementation code. The specs define the expected behavior and serve as the acceptance criteria. Only after the specs are in place should the implementation begin.

### Git

Always rebase on `origin/main` before anything else is done.

Use the git CLI for all git-related commands. 
When running github specific commands, use the official github cli (found at
https://cli.github.com/)

### Development Commands

When aspire exist use aspire run command from the aspire cli (found at https://aspire.dev/get-started/install-cli/)

Otherwise use what's default for the specific language. Use web to find the correct syntax.

### Code Conventions
Follow the official guidelines of the specific language used, use the web to find the relevant for the solution

### Testing

See the chapter for [Workflow](#workflow)

### Architecture
- Use the SOLID principle when designing and coding the solutions.
- Make it right the first time
- YAGNI
- KISS
And when in doubt ask.
