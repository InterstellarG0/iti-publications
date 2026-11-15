# Offline Assistance and Revocable Handoffs
Date: November 15, 2026
Status: Architecture research question v0.1; no implementation or verified global result.
Origin: Founder logistics analogy and local-assistant requirement; AI-assisted critical synthesis. Private job and payout details are excluded.

## Intended direction
A capable local assistant should support conversation, reasoning and authorized access to a user's own files while cloud services remain optional. A small initial test does not reduce the long-term goal to voice capture alone. Near-parity with any particular cloud assistant is an aspiration, not demonstrated performance.

Source availability, model weights, software licensing, hardware capacity, local installation and ongoing cloud dependencies require separate checks. “Open source” alone does not guarantee offline operation or privacy. The OSI Open Source Definition permits commercial use; a noncommercial-only publication license should not be described as an open-source software license. This note does not change any ITI license.

## Logistics analogy and its limits
Handoffs can clarify custody and responsibility. Multiple acknowledgments are not automatically cryptographic multisignature. In Bitcoin's documented m-of-n example, a threshold of cryptographic signatures authorizes a specified transaction. That example does not prove that a delivery platform uses the same mechanism.

A signature, a completed job, stopped access, deleted data and settled payment are different events. A successful real-world handoff can motivate a design question without proving worldwide revocability.

## Proposed test
Use fictional data and explicitly scoped permissions. Check that permitted access works, withdraw that permission, then attempt new access through the paths in scope. Record the effective time, existing sessions, cached copies, logs and dependencies. A passed check supports only the tested scope.

Deleting a file locally cannot establish deletion of copies already disclosed. Returning online must not silently release queued private work. Define human authorization for exports, updates and any future connectivity.

## Local acceptance questions
Can the system hold a useful conversation, retrieve a selected local document and export work while internet access is unavailable? What errors occur, how long do responses take, and how much memory and power does it use? Can the user inspect and correct its work? Broader performance and security need separate evidence.

A satellite is not a prerequisite for testing these ideas locally. Satellite storage or relay is a separate long-term engineering question, not an established privacy guarantee.

Sources, reviewed November 15, 2026:
- OSI definition: https://opensource.org/osd
- Bitcoin developer guide, transactions: https://developer.bitcoin.org/devguide/transactions.html
- NIST AI oversight background: https://airc.nist.gov/airmf-resources/playbook/govern/

Related candidates: ITI-RP-007, 014, 015, 018, 019, 020, 047, 049, 095, 098, 100, 102, 106, 113, 116, 117. Catalog remains 118.


Original public text is offered under the repository's [license notice](../LICENSE-NOTICE.md). Third-party sources retain their own terms.
