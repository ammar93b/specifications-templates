# Spec: <data change name>

Use the following specification as your single source of truth.
Do not make assumptions about any requirement not listed here.

## Feature

<!-- A one-sentence name of the feature. -->

## Overview

<!-- A short explanation of what data is added or changed, which feature needs it and why. -->

## Related specs

<!-- Links to the backend, API and frontend specs that use this data. Write "None" if there are none. -->

- 

## Tables

<!-- Copy this block once for each new or changed table. For a changed table, list only the columns that change and mark each one new / changed / removed. -->

### `<table name>`

<!-- One sentence: what one row in this table represents. -->

| Column | Type | Null allowed | Default | Notes |
|---|---|---|---|---|
| id | uuid | no | generated | Primary key |
| created_at | timestamptz | no | now() |  |
| updated_at | timestamptz | no | now() |  |
|  |  |  |  |  |

## Relationships

<!-- Foreign keys between tables, and what happens to child rows when the parent row is deleted (delete them too, block the delete, or set to null). -->

| From | To | On delete |
|---|---|---|
|  |  | cascade / restrict / set null |

## Rules and constraints

<!-- Rules the database itself must enforce: unique values, allowed values, value ranges, required combinations. -->

- 

## Indexes

<!-- Indexes needed for the searches, filters and sorting the features do. Say which query each index is for. -->

| Columns | Unique | For which query |
|---|---|---|
|  | yes / no |  |

## Access rules

<!-- Who may read and change rows in each table. If the database supports row level security (for example Supabase), describe each policy here. Say "only own rows" or "only rows of their farm/organisation" where that applies. -->

| Table | Role | Read | Create | Update | Delete |
|---|---|---|---|---|---|
|  |  | all / own / none | yes / no | all / own / none | yes / no |

## Migration

<!-- How to go from today's database to the new one without losing data. -->

- Steps: 
- Existing rows: <!-- How existing rows get values for new required columns. -->
- Downtime: <!-- None, or how long and why. -->
- Rollback: <!-- How to undo the migration if something goes wrong, and what data would be lost. -->

## Personal data and retention

<!-- Which columns hold personal data, how long rows are kept, and how they are deleted or anonymised when a person asks or the retention time ends. Write "No personal data" if none. -->

| Column | Personal data | Kept for | Then |
|---|---|---|---|
|  | yes / no |  | deleted / anonymised |

## Acceptance criteria

<!-- A list of testable conditions that define when the feature is complete. -->

- [ ] Migration runs on a copy of production data without errors
- [ ] Rollback runs without errors
- [ ] 

## Out of scope

<!-- What the feature doesn't define. -->

- 

## Edge cases

<!-- Unusual or boundary situations the data must handle. Delete the lines that do not apply. -->

<!-- - Duplicate rows, rows created at the same moment by two users -->
<!-- - Existing rows with missing or bad values -->
<!-- - Very large tables (migration time, locks) -->
<!-- - Deleting a parent row that still has child rows -->

## Security impact

<!-- How the change affects security: new sensitive data stored, changes to who can read or change data, data copied to backups or other systems. -->

## Threat modeling

<!-- How the data could be read, changed or deleted by someone who should not, and how each threat is mitigated. -->

| Threat | Mitigation |
|---|---|
|  |  |
