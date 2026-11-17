# Product handover checklist

Use a role or account owner in the review record; never put passwords or tokens in the checklist.

| Area | Owner to name | Evidence to review | Unresolved decision |
|---|---|---|---|
| Repository and release access | | | |
| Domain and hosting accounts | | | |
| Service/integration accounts | | | |
| Who may grant or remove access | | | |
| Deployment and rollback procedure | | | |
| Authoritative data and export | | | |
| Backup and restoration responsibility | | | |
| Retention and deletion decisions | | | |
| Failed-exchange investigation | | | |
| Agreed support and escalation boundary | | | |

## Demonstrate before sign-off
- [ ] A permitted operator can follow the documented release process.
- [ ] The rollback decision and owner are identified.
- [ ] A person can locate the record of unresolved work.
- [ ] Account ownership and recovery are agreed.
- [ ] Manual operating steps and deferred work are recorded.
- [ ] The actual support scope is stated without an assumed24/7 commitment.

Acceptance reviewer, date and remaining decisions:

This is a planning checklist, not a claim that a system has passed security, recovery or compliance testing.

NG Labs is a brand of North Growth Lab LLC.

## Record a bounded recovery exercise

Agree the environment, permitted sample data and reviewer before the exercise. Use an isolated review environment; this template is not an instruction to experiment on live customer work.

Illustrative example: a supplier approval record has one related attachment. The receiving operator needs to understand which backup contains both, how the sample is restored and what remains outside the exercise. This is not a client implementation or test result.

| Review field | Agreed or observed value |
|---|---|
| Environment and authorisation | |
| Permitted sample record and related file | |
| Backup identifier and capture date | |
| Application/source version | |
| Included records, attachments and dependencies | |
| Documented restoration steps followed | |
| What the receiving operator actually observed | |
| Excluded or untested data | |
| Undocumented assistance or missing dependency | |
| Unresolved action and responsible owner | |

Before the demonstration, write what the reviewer should be able to inspect afterwards. After it, record observations rather than ticking “backups work”. Keep the sample, restore date and application version connected so the next operator knows what the evidence covers.

A backup file being present is not restoration evidence. A successful sample restore also does not prove that every record, region, attachment or future incident is covered. Recovery objectives, retention, access and incident response require their own agreed scope. Leave unknowns visible and assign the next decision to an owner.

Keep secret values, customer records and private infrastructure locations out of this public template. Record configuration names and the authorised transfer method in an appropriately controlled company record.

For the buyer-facing five-area review and plain-text worksheet, see [web application handover acceptance](https://nglabs.cc/web-app-development/?utm_source=github&utm_medium=referral&utm_campaign=20261117_nglabs_handover&utm_content=bounded_recovery#handover-review).

Expanded 17 November 2026 by NG Labs / North Growth Lab LLC.
