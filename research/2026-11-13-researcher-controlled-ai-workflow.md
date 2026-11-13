# A Researcher-Controlled AI Workflow Layer
**Author:** Anthony P. — Interstellar Technologies Initiative, LLC (ITI)  
**Date:** November 13, 2026  
**Status:** Architecture proposal v0.1; unimplemented and untested  
**Origin:** Public synthesis of ITI's November 6 Independent AI Workflow Intermediary concept log. AI-assisted drafting. No claim of novelty or affiliation with a named infrastructure provider.

## Abstract
This note proposes a researcher-controlled layer for preparing and routing information to AI services. Its intended function is to make permissions, data selection, destinations and provenance visible before a task proceeds. It separates what the layer can control locally from what depends on an external provider. No integration, protection guarantee, adoption or effectiveness is reported.

## Design question
Can a researcher delegate a bounded AI task while retaining a usable record of what was authorized, what was sent, where it went and which output resulted?

The proposed participants are the human researcher, a local or independently administered workflow service, an external model provider and an optional explicitly authorized collaborator. “Independent” requires a defined administrative and access boundary; running another server does not establish independence by itself.

## Proposed components
| Component | Proposed responsibility | Limit |
|---|---|---|
| Permission record | Capture task, destination, allowed input and expiry | A recorded choice needs an enforcement mechanism |
| Input preparation | Select the minimum approved material | Summaries can still disclose sensitive information |
| Routing gate | Block destinations or payloads outside the approved task | Cannot govern requests made through another channel |
| Provenance record | Link source version, approval, transformation and output | A log records events; it does not verify a claim's truth |
| Export and correction | Let the researcher inspect and amend records | Corrections cannot recall copies already disclosed |

Default to withholding private raw sources. Keep operational metadata minimal too; logs can themselves reveal sensitive research. Authentication, role definitions, credential handling, retention and deletion rules require separate specifications before implementation.

## Worked synthetic scenario
A researcher has a private interview and wants help drafting a public educational outline.

1. The researcher creates a synthetic summary with no real person's information.
2. The interface previews the exact approved payload and the destination.
3. Authorization permits outline generation only, with no collaborator sharing.
4. The gate sends the approved summary and records the source version and task.
5. The result is labeled AI output for human review; it is not automatically published.
6. If sharing is withdrawn before a queued request is sent, the gate rejects that request.

This scenario is a proposed behavior, not a completed test. A later test involving actual private data would need a separate justification and review.

## Acceptance tests to implement
| Test | Proposed pass evidence |
|---|---|
| Payload exceeds approval | Request blocked before external transmission |
| Destination changes | New approval required; original permission not reused |
| Permission withdrawn before send | Queued request remains unsent |
| Restart and reconnect | Previously blocked requests do not silently resume |
| Collaborator requests raw input | Access denied unless separately authorized |
| Source corrected | New version linked; earlier derivative marked for review |
| Export requested | Human-readable provenance and permitted artifacts are produced |

Evaluate observed requests and relevant traffic routes, not just interface indicators. Record failures, bypasses and administrative actions. The local service itself becomes a security dependency.

## External boundaries
A workflow gate cannot prove that an external provider deleted or never retained a received payload. Provider behavior depends on independently checked technical capabilities and applicable terms. Revocation can stop future transfers under the gate's control; it cannot retroactively retrieve information already sent. These are requirements to investigate, not assurances.

## Research path
Define a threat model and intended task; prototype with synthetic records; run the acceptance tests; compare user understanding and task burden with an ordinary workflow; seek independent technical review. Document what the layer cannot control.

This note is a product/design hypothesis, not evidence of misconduct by any company, legal compliance, provider endorsement or an available ITI service.

**Related candidates:** ITI-RP-014, 015, 017, 018, 020, 100, 102, 116, 117. No new candidate IDs.  
Original public text is offered under the repository's [license notice](../LICENSE-NOTICE.md).
