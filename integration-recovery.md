# Integration recovery brief

Describe one exchange. Do not assume a third-party API, account or permission is available until its owner confirms it.

- Business purpose:
- Source record, reference, version and authoritative fields:
- Destination record and authoritative fields:
- Trigger:
- Account/access owner for each system:
- Evidence of confirmed completion:
- State shown while no confirmation is available:
- Who investigates and what context they may see:
- Evidence required before a repeat:
- Who may authorise a repeat:
- Rule for late confirmation:
- Rule for changed source version:
- Explicitly manual recovery steps:
- Recovery owner and evidence before closure:
- Agreed support scope/hours and escalation:
- Acceptance reviewer:

| Condition | Decision to agree | Responsible role | Evidence before closure |
|---|---|---|---|
| No confirmation | What is checked before a repeat? | | |
| Person repeats action | Same intended exchange or new version? | | |
| Late confirmation | How is it matched and reconciled? | | |
| Permission changes | Who can approve restored access? | | |
| Source changes | Is a new approval required? | | |

A retry control alone does not answer these questions. This template establishes no monitoring commitment or support agreement.

## Agree the field contract before diagnosing the exchange

Two systems can agree that a message arrived while disagreeing about what a
value means. Review the smallest useful exchange field by field with the people
who own both records. Keep a proposed rule separate from an observed test result.
An API name or a successful connection demonstration does not settle the data
rules or establish that the required account permissions are available.

Use this blank row for each field that affects the business outcome:

| Decision | Record the agreed rule |
|---|---|
| Business meaning | What does this value mean to the people doing the work? |
| Source of truth | Which system and role may originate or change it? |
| Source and destination | Exact field names and permitted direction of travel |
| Representation | Type, allowed values, unit, precision or date/time meaning |
| Missing value | Required or optional; what omission means |
| Empty or null value | Rejected, unchanged, cleared or another explicit outcome |
| Transformation | Any mapping, rounding, timezone or default rule and its owner |
| Invalid or unsupported value | Refusal, visible unresolved state and responsible role |
| Version boundary | Which source version the approval and exchange concern |
| Completion evidence | What is checked in the destination, by whom, before closure |

Do not copy passwords, tokens or private customer records into this table. Use
synthetic values for planning and agree a controlled preview/test environment
before anyone performs a test. The table itself implements no validation,
authorization or retry behaviour.

### Worked example — an approved print request

This is a fictional requirements discussion, not a live integration or client
case. An approved request should create a work item in an operational tool.

| Proposed field rule | Illustrative decision for the owners to review |
|---|---|
| Request reference | Preserve the source reference and approved version so the reviewer can identify the intended request. Agree the destination matching rule. |
| Quantity | Accept a whole number of printed items within an agreed range. State the unit explicitly; do not silently interpret a missing value as one item. |
| Finish code | Map an agreed source code to a supported destination code. A new unmapped finish stays unresolved for the named business owner. |
| Requested date | Decide whether this is a calendar date or a timestamp. If it is a timestamp, record its timezone and display rule; do not infer them from a screenshot. |
| Customer note | Agree whether omission leaves the destination unchanged and whether an explicitly empty value clears it. Do not assume those two inputs mean the same thing. |

The proposal above still needs confirmation from both record owners and an
implementation review. If the destination cannot represent a required value,
record the limitation and choose a bounded manual step or a changed scope. Do
not hide the mismatch in a default that makes the exchange appear complete.

### Three acceptance records to agree

1. **Expected value:** use a synthetic approved request and a supported finish.
   Record the source version, expected destination values, actual observations
   and the person who checked them. Transport acceptance alone is not evidence
   that the right record and business values were created.
2. **Missing versus empty:** compare a note omitted from the proposed exchange
   with an explicitly empty note, using separate authorised test records. Record
   the actual destination outcomes against the two agreed rules.
3. **Changed or unmapped value:** introduce a synthetic finish code not present
   in the agreed mapping. Specify the unresolved message and owner. Record how
   an approved mapping change would be reviewed before a deliberate repeat;
   do not assume that retrying fixes a semantic mismatch.

For each case use: **source reference/version → contract revision → expected
outcome → observed destination evidence → unresolved difference → decision
owner → next action**. Leave observations blank until a check has actually
been performed. A checklist completed from assumptions is not test evidence.

For the wider ownership and recovery discussion, use the
[NG Labs integration failure checklist](https://nglabs.cc/insights/integration-failure-checklist/?utm_source=github&utm_medium=referral&utm_campaign=20261119_nglabs_field_contract).
This reference does not imply that a specific third-party integration, support
window or monitoring service is included.

NG Labs / North Growth Lab LLC. Original planning material.
