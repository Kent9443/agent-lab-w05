# My lab evidence / 我的實作紀錄

> Status note: this is an agent-assisted work record, not a claim that the student personally performed or checked every lab step. Fill in the group code and add the student's own observations/screenshots before submission.

- Group code / 組別：Not provided
- Tool / 工具：Codex desktop (agent-assisted)
- Route / 路線：Not stated; local repository work
- Tasks completed / 完成題目：A outputs; B v1 and v2 saved; C data cleaning; D rejection. B's six UI tests and v2 retest remain pending.
- Material / 素材：NDHU classroom tasks 東華課堂版
- For original-pack work: task number, author/source link and version / 原版實作：Not applicable
- My role and what I checked / 我的角色與實際檢查：The assistant organized the 12 fictional A inputs, checked source/copy hashes and compared suspected duplicate/version pairs; normalized C equipment records while preserving uncertainty; created B v1 and changed its language-switch labels in B v2; and wrote a D rejection. B's six UI checks and v2 retest have not been reported.

## Scope and plan / 範圍與計畫

Allowed input and output folders / 可讀取與輸出的資料夾：
- A: `practice/01-club-files/input/` → `practice/01-club-files/output/`
- B: `practice/02-campus-picker/activities.json` → `practice/02-campus-picker/output/index.html`
- C: `practice/03-equipment/equipment.json` → `practice/03-equipment/output/`
- D: read `practice/04-review/bad-plan.txt`; write `practice/04-review/my-rejection.md`

What I asked for / 原始需求：Finish all tasks in this repository.

What I checked before execution / 動手前我檢查了什麼：Read the README and task handouts; inspected task input files and repository status. The A/C inputs are fictional teaching data. The instructor starter remote was replaced with the selected personal repository `Kent9443/agent-lab-w05`; commits are pushed there task by task.

## Tests actually performed / 我真的做過的測試

| Test / 測試 | Expected / 預期 | Observed / 實際 | Evidence / 證據 |
|---|---|---|---|
| A: compare every source/copy SHA-256 pair (12 pairs) | Each organized copy exactly matches its source | All 12 pairs matched | `practice/01-club-files/output/manifest.json`; `practice/01-club-files/output/report.md` |
| A: compare suspected duplicate and version pairs | Identical-content copies remain separate; differing proposals remain separate and unresolved | Announcement pair and equipment pair were identical; proposal v1 and v2 differed and both state they are unapproved. All were retained. | `practice/01-club-files/output/report.md` |
| C: check row counts, repeated IDs and uncertain quantities | 10 rows become 9 valid rows; repeated IDs remain; missing/negative quantities are flagged | 9 records retained; empty source row 6 omitted; both EQ01/EQ02 rows retained; EQ04 empty qty and EQ05 -1 preserved and reported; EQ02 quantity conflict noted | `practice/03-equipment/output/normalized.json`; `practice/03-equipment/output/issues.md` |

B's six required UI tests have not been performed by the assistant. The browser policy blocked opening the local `file://` page. The student said they will run those checks and send the results.

## One revision / 一次修改

Before / 原來的情況：B v1 is saved in commit `725614d`. Static code inspection showed its English interface used the Chinese-only language-switch label `中文`.

Request / 我提出的修改：Translate the language-switch control label into the current interface language.

After and retest / 修改後與重測結果：B v2 commit `73469ec` changes the English label to `Switch to Chinese` and the Chinese label to `切換為英文`. Browser retesting has not been performed.

New requirement or defect? / 新需求還是原規格未做到？：The original bilingual-interface requirement was not fully met by the English-only v1 button label; v2 addresses the code issue but needs UI retesting.

## One rejection / 一次退回

Which action I reject and why / 退回哪個動作、為什麼：Rejected the simulated plan to organize all of Downloads, delete suspected duplicates, assume `final2` is approved, guess missing values, and publish automatically. It exceeds scope, risks data loss, fabricates uncertain data, and shares files without authorization.

An acceptable alternative / 可以怎麼改：Work only in the selected task folder, preserve originals and possible duplicates, record source mappings and unresolved decisions, and ask before expanding scope or sharing.

## Still unverified / 還沒驗證

What I cannot claim is complete / 哪些事不能說已完成：B's six interactive tests and v2 retest; screenshots; the student's own self-check notes and group code. B v2 is committed but not browser-verified. Do not submit this record as a completed student learning record until those items are added.

For the fallback route, mark all prepared evidence as supplied simulation. / 備援路線請標明所有預生成證據來源，不能填成自己的Agent實跑。
