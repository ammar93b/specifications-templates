# Spec: <AI feature name>

Use the following specification as your single source of truth.
Do not make assumptions about any requirement not listed here.

## Feature

<!-- A one-sentence name of the feature. -->

## Overview

<!-- A short explanation of what the AI does, who uses it and why. Say what a person would do without it. -->

## Inputs

<!-- Everything the AI is given: the user's message, records from the database, files, documents, web pages. Say which inputs come from people or sources we do not control. -->

| Input | Source | Trusted |
|---|---|---|
|  |  | yes / no |

## Output

<!-- What the AI produces (text answer, filled form, structured data, a decision) and its exact format. For structured output, give an example. -->

```json
{
}
```

## Actions

<!-- What the AI may do besides answering: read data, write data, send messages, call other services. For each action, say whether a person must confirm it first. Write "Answers only" if it takes no actions. -->

| Action | Needs confirmation | Who confirms |
|---|---|---|
|  | yes / no |  |

## Model and instructions

- Model: 
- Instructions (system prompt): <!-- Link to the file in the repository where they live. -->
- Language(s): 
- Tone: 

## Quality

<!-- How we know the AI is good enough. List example inputs with the expected output, and the bar it must reach before release. -->

| Example input | Expected output or behavior |
|---|---|
|  |  |

## When the AI is wrong or unsure

<!-- What happens when the AI does not know, gives a wrong answer, or the model service is down. Say when it must hand over to a person. -->

## Cost and speed

<!-- Expected calls per day, cost per call, monthly budget, and the longest acceptable wait for an answer. -->

## Data and privacy

<!-- Which data is sent to the model provider, whether it contains personal data, and what is stored (conversations, outputs) and for how long. -->

## Acceptance criteria

<!-- A list of testable conditions that define when the feature is complete. -->

- [ ] All examples in the Quality table give the expected output
- [ ] 

## Out of scope

<!-- What the feature doesn't define. -->

- 

## Edge cases

<!-- Unusual or boundary situations the feature must handle. Delete the lines that do not apply. -->

<!-- - Empty, very long or off-topic input -->
<!-- - Input in a different language -->
<!-- - Questions about data the user may not see -->
<!-- - Model service slow, down or over its rate limit -->

## Security impact

<!-- How the feature affects security: data sent outside, actions the AI can take, data the AI can read on behalf of a user. -->

## Threat modeling

<!-- How the feature could be attacked or misused, and how each threat is mitigated. Consider: instructions hidden in inputs (prompt injection), getting the AI to reveal other users' data, getting it to take actions the user may not take, running up cost. -->

| Threat | Mitigation |
|---|---|
|  |  |
