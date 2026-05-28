# API Contracts

## Base URL

`/api/v1`

## Authentication

All protected endpoints require `Authorization: Bearer <token>` header.

## Endpoint Format

```
[METHOD] /path
Auth: required | public
Request: { field: type }
Response 200: { field: type }
Response 4xx: { error: string, message: string }
```

## Endpoints

(Populated during planning, organized by resource/module)
