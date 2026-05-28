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

## Infrastructure

(Database, caching, external services, deployment target)
