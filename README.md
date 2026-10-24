# Specifications templates

Markdown specification templates for building software, written to work well with AI coding assistants such as Claude. Every new feature, API, data change or bug fix starts as a filled-in spec. The spec is the single source of truth for building it: if something is not in the spec, it is not built.

Each template ends with acceptance criteria, out of scope, edge cases, security impact and threat modeling, so security is considered before any code is written.

## Which template to use

| Template | Use it for |
|---|---|
| [backend.md](templates/backend.md) | Server-side logic, scheduled jobs, scripts, services without a UI |
| [frontend.md](templates/frontend.md) | Screens, pages, forms and anything else the user sees and clicks |
| [api.md](templates/api.md) | A new or changed API endpoint: requests, responses, errors, permissions |
| [database.md](templates/database.md) | New or changed tables, columns, access rules and migrations |
| [integration.md](templates/integration.md) | Connecting to an outside service: payments, notifications, webhooks, websites we read, devices and sensors |
| [ai-feature.md](templates/ai-feature.md) | Anything that uses an AI model: assistants, chat, summaries, automatic decisions |
| [bugfix.md](templates/bugfix.md) | Fixing something that does not work as specified |

A bigger feature usually needs more than one spec. For example, "record a goat's weight from the phone" could be:

- `database.md` for the weights table and who may write to it
- `api.md` for the endpoint that saves a weight
- `frontend.md` for the form on the phone

Link the specs to each other in their "Related specs" or "Backend dependency" sections. Do not repeat the same details in two specs.

## Get the templates

- Download the latest release from the [Releases](../../releases) page, or
- Copy a single file from [templates/](templates/) into your project.

## How to write a spec

1. Copy the template into the project's `specs/` folder and name it with the next number and a short name, for example `specs/07-goat-weights-api.md`.
2. Replace `<...>` placeholders and fill each section. The `<!-- ... -->` comments explain what goes there; delete them when the section is filled.
3. Write "None" in a section that does not apply. Do not delete required sections, so it is clear they were considered.
4. Write acceptance criteria that a person or a test can check with a clear yes or no.
5. Put everything you do not want built under "Out of scope".
6. Have one other person read the spec before building starts.

## How to build from a spec

Give the spec file to Claude (or a developer) with a request like:

> Build the feature in `specs/07-goat-weights-api.md`. Follow the spec exactly and ask before doing anything it does not cover.

When the spec and the code disagree later, fix the spec first, then the code.

## Shared rules for every spec

- Security impact and threat modeling are required for every new feature, even when the answer is short.
- Never put passwords, keys, tokens or real personal data in a spec.
- Dates and times are in ISO 8601 (`2026-10-21T14:30:00Z`). Money is stored as an integer in the smallest unit (cents) together with a currency code.
- Plain language: write for a reader who was not in the meeting.

## Changing the templates

Change a template here, not in a project's copy, so every project gets the improvement. Changes are listed in [CHANGELOG.md](CHANGELOG.md).

Suggestions and improvements are welcome. Open an issue or a pull request.

## License

[MIT](LICENSE). Use, copy and adapt the templates freely, including in commercial work.
