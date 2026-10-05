# Learning record — NDHU Campus Agent Lab

> Prepared from the repository and work completed in Codex. This is not an export of the handout website's browser-only self-checks, and it does not claim the student personally performed the checks below. Add the student's own reflection, UI observations, and screenshots before submission.

## Work completed

- **Task A — organize club files:** Copied all 12 input files into categories without deleting or merging candidates. Added a source-to-destination list, `report.md`, and a 12-entry `manifest.json`. SHA-256 comparison confirmed that all 12 copies match their sources. Compared suspected duplicate pairs and both proposal versions; kept both proposals because they differ and are unapproved.
- **Task B — activity picker:** Saved the first version and a revision. The revision changes the language switch labels to “Switch to Chinese” in English and “切換為英文” in Chinese. B v1 is commit `725614d`; B v2 is commit `73469ec`.
- **Task C — equipment records (optional):** Retained 9 valid rows, removed only the fully empty row, kept repeated IDs, normalized text/status fields, and preserved and reported the empty and negative quantities without guessing.
- **Task D — rejection:** Rejected the simulated plan's overbroad scope, duplicate deletion, unsupported version choice, guessed values, and automatic publishing; suggested a scoped, reviewable alternative.

## Checks recorded

| Check | Expected | Observed | Evidence |
|---|---|---|---|
| A: compare source/copy hashes for all 12 files | Each copy is identical to its source | All 12 matched | `practice/01-club-files/output/report.md`; `manifest.json` |
| A: inspect two suspected duplicate pairs and proposal versions | Retain identical candidates separately; preserve differing versions and uncertainty | The announcement pair and equipment pair were identical; proposal versions differed and both were unapproved. All were retained. | `practice/01-club-files/output/report.md` |
| C: counts, repeated IDs, and uncertain quantities | 10 inputs → 9 valid rows; repeated IDs remain; uncertain quantities are flagged | 9 retained; empty row 6 removed; repeated EQ01/EQ02 rows retained; EQ04 empty quantity and EQ05 `-1` kept and flagged; EQ02 quantity conflict reported | `practice/03-equipment/output/issues.md`; `normalized.json` |
| B: six interactive UI scenarios | Match the handout's expected behavior | Not performed; local HTML browser access was blocked | No UI result claimed |

## Revision and retest

B v1's English interface used the Chinese-only language-switch label `中文`. B v2 changes the labels to match the current interface language. The B v2 browser retest is pending, as are all six interactive checks.

## Rejection

The simulated `bad-plan.txt` proposal to organize all of Downloads, delete suspected duplicates, infer approval from `final2`, guess missing data, and publish automatically was rejected. The safer alternative is to stay within the task folder, preserve source files and uncertainty, document mappings, and ask before expanding scope or sharing.

## Still needed from the student

- Run the six B UI checks on `practice/02-campus-picker/output/index.html` and record actual observations.
- Retest the language switch in both languages after B v2.
- Add screenshots and personal learning notes; fill in the group code and actual student role.
- Review the evidence and repository before submitting. Do not present pending checks as complete.
