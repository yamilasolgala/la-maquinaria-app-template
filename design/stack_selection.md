# Stack Selection

## Backend

- **Language**: [Selected during planning]
- **Framework**: [Selected during planning]
- **ORM/Query Builder**: [Selected during planning]
- **Rationale**: [Why this stack]

## Frontend

- **Framework**: [Selected during planning]
- **Language**: [Selected during planning]
- **CSS**: [Selected during planning]
- **State Management**: [Selected during planning]
- **Rationale**: [Why this stack]

## Database

- **Engine**: [Selected during planning]
- **Version**: [Selected during planning]
- **Rationale**: [Why this database]

## Additional Tools

(Build tools, linters, formatters, testing frameworks — selected during planning)

## AI / Model Provider (Rule 9 — portability)

- **Abstraction**: [OpenAI-compatible SDK with configurable `base_url`+`model`, or LiteLLM — one adapter for all providers]
- **Default provider / model**: [e.g. Anthropic / claude-* ] · **Fallback / alternates enabled**: [OpenAI, Google, local…]
- **Config shape**: `{ provider, model, apiKey, baseUrl? }` per model use (key = Level 3 credential)
- **Rationale**: no vendor lock-in — provider is a config field; swapping it doesn't touch prompts, skills, memory, or integrations.
