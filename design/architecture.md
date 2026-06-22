# System Architecture

## Overview

(System architecture diagram and description — populated during planning)

## Module Structure

(Backend and frontend module organization)

## Technology Choices

See stack_selection.md for detailed rationale.

## Credential Level Mapping

- **Level 1 (.env)**: [Infrastructure secrets — DB URL, JWT secret, encryption key]
- **Level 2 (deployment)**: [Service URLs, feature flags, environment config]
- **Level 3 (admin panel)**: [Third-party API keys, integration tokens — encrypted at rest]

## Model Provider Layer (Rule 9 — portability)

The LLM provider is a swappable plug, isolated behind one adapter so the system survives changing providers.

- **Adapter**: [single module all AI calls go through — e.g. `ai/provider.ts`. No direct SDK calls outside it.]
- **Config-driven**: each model use is `{ provider, model, apiKey, baseUrl? }` in config — never hardcoded. API key = Level 3 credential.
- **Supported providers**: [Anthropic / OpenAI / Google / local-Ollama / OpenRouter — list what this project enables]
- **What a provider swap touches**: only the config. NOT system prompts, skills, memory, data, or integrations.
- **What the adapter isolates** (the honest caveats): tool/function-call format differences, response shape, token/context limits, feature support (vision, tool use). These live inside the adapter, not in agent logic.
- **Swap test (verification)**: switch the config to a second provider and re-run the standard test prompts. System works (light prompt re-tuning allowed; no architectural change).

## Infrastructure

(Database, caching, external services, deployment target)
