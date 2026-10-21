# Spec: <API name>

Use the following specification as your single source of truth.
Do not make assumptions about any requirement not listed here.

## Feature

<!-- A one-sentence name of the feature. -->

## Overview

<!-- A short explanation of what the API does, who calls it (our frontend, the mobile app, another service, a scheduled job, an outside partner) and why it is needed. -->

## Related specs

<!-- Links to the backend, frontend and database specs that use or build this API. Write "None" if there are none. -->

- Backend spec: 
- Frontend spec: 
- Database spec: 

## Endpoints

<!-- One row per endpoint. Use nouns in the path (/goats, /goats/{id}/weights), not verbs. -->

| Method | Path | Purpose | Who may call it |
|---|---|---|---|
|  |  |  |  |

## Endpoint details

<!-- Copy this block once for each endpoint in the table above. -->

### `<METHOD> <path>`

#### Request

<!-- Path and query parameters, required headers, and the request body. Delete the parts that do not apply. -->

| Field | Where | Type | Required | Rules |
|---|---|---|---|---|
|  | path / query / header / body |  | yes / no | e.g. max 100 characters, must be in the future, one of A, B, C |

```json
{
}
```

#### Response

<!-- The success status code (200, 201, 204) and an example body. Say which fields can be null or missing. -->

Status: 

```json
{
}
```

#### Errors

<!-- Every error this endpoint can return. Use the error format in "Conventions" below. -->

| Status | Error code | When |
|---|---|---|
| 400 | `validation_failed` | A field breaks a rule in the Request table |
| 401 | `unauthenticated` | No valid session or token |
| 403 | `forbidden` | Caller does not have the access right |
| 404 | `not_found` | The resource does not exist or the caller may not see it |
|  |  |  |

## Conventions

<!-- Delete this section if the project already defines these in a shared document, and link that document instead. -->

- Field names: camelCase in JSON
- Dates and times: ISO 8601 in UTC, for example `2026-10-21T14:30:00Z`
- Money: integer in the smallest unit (cents) plus a currency code, never a floating point number
- Error body:

```json
{
  "error": {
    "code": "validation_failed",
    "message": "A short sentence a person can read.",
    "details": [{ "field": "name", "issue": "required" }]
  }
}
```

## Authentication and permissions

<!-- How the caller proves who they are (session cookie, bearer token, API key, webhook signature) and which roles may call each endpoint. Say what the caller sees when they may read only part of the data. -->

| Endpoint | Role or access right | Without the right |
|---|---|---|
|  |  | 403 / 404 / filtered result |

## Paging, sorting and filters

<!-- For endpoints that return lists: page size (default and maximum), how to ask for the next page, which fields can be sorted and filtered, and the default order. Write "None" if no endpoint returns a list. -->

## Side effects

<!-- What else happens when the API is called: database rows written, emails or notifications sent, files stored, other services called, jobs started. -->

## Repeated and simultaneous requests

<!-- What happens if the same request arrives twice (double click, network retry), or two callers change the same record at the same time. Say if an idempotency key or a version number is needed. -->

## Limits

<!-- Rate limits, maximum request body size, maximum upload size, timeouts. Say what the caller gets when a limit is reached (for example 429 with a Retry-After header). -->

## Versioning and breaking changes

<!-- Is this a new API or a change to an existing one? List any change that would break an existing caller (renamed or removed field, new required field, changed meaning) and how existing callers are moved over. -->

## Logging

<!-- What is logged for each call, and what must never be logged (passwords, tokens, personal data, payment details). -->

## Acceptance criteria

<!-- A list of testable conditions that define when the feature is complete. Include at least one success case and one error case per endpoint. -->

- [ ] 

## Out of scope

<!-- What the feature doesn't define. -->

- 

## Edge cases

<!-- Unusual or boundary situations the API must handle. Delete the lines that do not apply. -->

<!-- - Empty body, unknown fields, wrong types, very long strings, unexpected characters -->
<!-- - Resource deleted between two calls -->
<!-- - Empty list, last page, page beyond the end -->
<!-- - Time zones, daylight saving changes, dates far in the past or future -->
<!-- - A service this API depends on is slow or down -->

## Security impact

<!-- How the API affects security: new data exposed, new ways in, changes to authentication or permissions, data that leaves our system. -->

## Threat modeling

<!-- How the API could be attacked or misused, and how each threat is mitigated. Consider: reading another user's data by changing an id, sending too many requests, sending crafted input, replaying an old request. -->

| Threat | Mitigation |
|---|---|
|  |  |
