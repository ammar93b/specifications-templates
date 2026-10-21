# Spec: <integration name>

Use the following specification as your single source of truth.
Do not make assumptions about any requirement not listed here.

## Feature

<!-- A one-sentence name of the feature. -->

## Overview

<!-- A short explanation of which outside service we connect to, what we use it for and why. Examples: payment provider, email or push notifications, a website we read data from, a sensor or device, a partner's API. -->

## Outside service

- Name: 
- Documentation link: 
- Account owner: <!-- Who in the team owns the account and pays for it. -->
- Cost: <!-- Free tier, price per call, monthly fee. -->
- Limits: <!-- Rate limits, quotas, maximum sizes. -->
- Terms of use: <!-- Anything the terms allow or forbid that affects this feature, for example automated reading of a website. -->

## Direction

<!-- Pick one or more and describe each. -->

- [ ] We call their API
- [ ] They call us (webhook / callback)
- [ ] We read their website or files
- [ ] A device sends us data

## Data exchanged

<!-- Every piece of data that goes out or comes in. Say which items are personal or sensitive. -->

| Data | Direction | Format | Personal or sensitive |
|---|---|---|---|
|  | out / in |  | yes / no |

## When it runs

<!-- What triggers the integration: a user action, a schedule (how often, which time zone), an incoming webhook, a device reading. -->

## Credentials

<!-- Which keys, tokens or passwords are needed, where they are stored (never in the code or the repository), who can see them and how they are replaced. -->

| Credential | Stored in | Replaced how / how often |
|---|---|---|
|  | environment variable / secret store |  |

## Incoming messages

<!-- For webhooks and devices only: how we check the message really comes from them (signature, shared secret, allowed addresses), and how we handle the same message arriving twice. Write "None" if nothing comes in. -->

## Failure handling

<!-- What happens when the outside service is slow, down, returns an error, returns data in a new format, or changes its website. -->

- Timeout: 
- Retries: <!-- How many, how long between them, and which errors are retried. -->
- When it keeps failing: <!-- Who is told, and what the user sees meanwhile. -->
- When their data format changes: 

## Monitoring

<!-- How we notice the integration has stopped working, and who gets the alert. -->

## Acceptance criteria

<!-- A list of testable conditions that define when the feature is complete. Include what happens when the outside service is down. -->

- [ ] 

## Out of scope

<!-- What the feature doesn't define. -->

- 

## Edge cases

<!-- Unusual or boundary situations the integration must handle. Delete the lines that do not apply. -->

<!-- - Empty response, partial response, response much larger than usual -->
<!-- - Same item or message received twice -->
<!-- - Credentials expired or revoked -->
<!-- - Time zone or currency different from ours -->
<!-- - Rate limit reached -->

## Security impact

<!-- How the integration affects security: data that leaves our system, new credentials to protect, new ways into our system, trust in data we did not create. -->

## Threat modeling

<!-- How the integration could be attacked or misused, and how each threat is mitigated. Consider: fake webhooks, stolen credentials, harmful content in data we receive, the outside service being compromised. -->

| Threat | Mitigation |
|---|---|
|  |  |
