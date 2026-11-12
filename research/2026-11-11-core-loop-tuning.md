# Core Loop Tuning: From Player Friction to Traceable Changes

Date: 2026-11-11
Status: Published developer methodology note v0.1; not a validated scientific study.
Origin: Anthony P.'s Interstellar Ants v2.0–v2.2 build notes, uploaded Loop Tuning Graph, and reported November 11 playtest; source methodology organized by ChatGPT. This is a public adaptation, not publication of the internal archive.

## Method
1. Play using an ordinary player path and the actual input device.
2. Record exact friction: action, context, expected result, and observed result.
3. List interacting causes; label each as a hypothesis or supported explanation.
4. Make narrow changes and preserve before/after settings.
5. Replay the affected sequence and adjacent paths; record failures and skipped checks.
6. Log the evidence, remaining uncertainty, and next test.

If several changes ship together, the result cannot establish the separate contribution of each change.

## Case: assigned ants appear not to go
The development notes identified three interacting explanations: orders gated by the day shift, slow assigned movement, and recovery interrupting travel. The recorded revision permits assigned travel through day and night, increases assigned march speed, and changes recovery handling while retaining the rule that recovering ants cannot receive new orders. A gold diamond and arrival feedback make assignment state visible.

| Recorded item | Before | After | Evidence limit |
|---|---|---|---|
| Scaffold build-time index | 100 | 67 | Indexed estimate from build notes; not independently timed |
| Assigned march setting | 1.0× patrol | 1.6× patrol | Configured multiplier; not a measured completion-rate improvement |
| Assignment timing | Day shift | Day and night until completion | Reported behavioral change; no completion sample |
| Assignment feedback | Unclear | Gold diamond, toast, log | Founder reported a visible diamond and working flow on November 11; no usability study |

A single symptom can have several causes. Changing only movement speed may leave timing or state-transition failures unresolved.

## Case: bilingual coverage
The uploaded chart lists ten surfaces: title, HUD, prompts, panels, toasts, conversations, Colony Log, seed, guide, and changelog. It records checklist coverage progressing from 6/10 to 8/10 to 10/10. These are named categories in a developer checklist, not independently audited translation completeness.

The recorded holdouts were log entries that did not update on language switching, untranslated seed labels, and guide/changelog bodies remaining English beneath translated headings. Source notes report 16 guide entries, 46 changelog entries, and roughly 50 additional log events receiving translations.

Known source-reported limitations include legacy log entries retaining their original language, a generated spawn sign potentially requiring a new world, and language resetting on reload. These need verification against the specific current build.

## Next verification pass
Record build identifier, device, input method, day/night state, and save state. Test eligible and recovering ants, assignment completion, feedback accuracy, and save/load. For localization, switch English → Spanish → English at the title and mid-session; inspect body text and long-string layouts across all ten surfaces. Mark each check passed, failed, or skipped.

Measure attempts, completed/blocked assignments, elapsed completion times under recorded conditions, and misunderstood UI states. Keep sample size and conditions attached to results. A configured 60% movement increase does not prove tasks complete 60% faster.

## Reusable log
- Build, date, environment, and input device
- Expected versus observed behavior
- Candidate causes and supporting evidence
- Before/after settings and bundled changes
- Checks passed, failed, or skipped
- Sample size, conditions, and observed outcomes
- Remaining uncertainty and next test

## Provenance and limits
Source: ITI Core Loop Tuning Methodology v1.0 dated November 11, 2026, incorporating the founder's uploaded Loop Tuning Graph and playtest report. Supporting project context: [v2.2 developer update](https://interstellarg0.itch.io/interstellar-ants/devlog/1769365/v22-the-colony-speaks-spanish).

This publication does not independently audit code, translations, or gameplay. It documents the reported case and proposes a repeatable verification process. Transfer to education or other operations remains a hypothesis.

Related candidate topics: ITI-RP-034, ITI-RP-092, ITI-RP-097.
Original public text in this note is designated under the repository's [license notice](../LICENSE-NOTICE.md).
