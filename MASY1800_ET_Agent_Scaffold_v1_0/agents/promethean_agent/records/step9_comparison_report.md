# Step 9 Same-Case Retest Comparison
Session date: 2026-10-17 (America/New_York)
Baseline: 0.1-student | Revised: 0.2-student | Evidence: EP-A4-0.1 unchanged

## Outcome
W1 improved in the observed Primary retest: the wrong Section 11.5 suppression attribution is absent and Sections 11.2/11.7 are correctly identified. W2 improved in framing, but complete removal or material reduction of manufacturing discussion was not demonstrated. Main classification gates, evidence scope, withholding, and contextual recommendations remain intact. A minor new omission appears in one Contrast reassessment trigger. This is not an unqualified declaration that v0.2 is better.

## Controlled changes and preserved baseline
Only specialist_instructions.md (two approved analytical passages) and agent_metadata.json (version only) changed among pre-existing files. records/specialist_instructions_v0_1.md preserves exact baseline bytes. The two case JSON files, EP-A4-0.1, v0.1 prompts/responses, Step 8 records, Agent Record, common schemas and all protected files remain unchanged. Each v0.2 packet's parsed case, including the complete evidence payload, equals its v0.1 counterpart. No test was changed to improve the appearance of results.

## Execution and structural results
Same procedure as Step 8: a fresh no-history specialist session per case, same neutral read/execute/save wrapper, no parent-authored classification or response repairs. Input and output filenames and metadata version changed as documented. No deliberate model/sampling changes; exact model build and seed are unavailable. The shared-filesystem and delivery-wrapper limits remain. See step9_execution_record.md.

| Check | Primary v0.2 | Contrast v0.2 |
| --- | --- | --- |
| Professor validator | VALIDATION PASSED, exit 0 | VALIDATION PASSED, exit 0 |
| JSON parsing/duplicate keys | Valid; no duplicates | Valid; no duplicates |
| Supplemental checks of constraints used by actual schema | No violations | No violations |
| Independent standards-complete JSON Schema engine | Not performed | Not performed |
| Frozen-core checker | FROZEN CORE INTACT, exit 0 | Shared unchanged scaffold |

Actual command output is in step9_command_results.txt. Structural success does not establish analytical correctness. Supplemental checks are the same standard-library approach as Step 8, not a full standards-engine certification.

## Passage-level comparison
Excerpts are exact contiguous text from named fields in the preserved JSON outputs. Findings concern these runs only.

| Evaluation | Result | v0.1 passage | v0.2 passage | Interpretation |
| --- | --- | --- | --- | --- |
| 1. W1 course attribution | Observed improvement in the Primary retest | primary v0.1 / `general_et_finding`: “Under Section 11.5, return of the old state would indicate reduction and Breakthrough at most, not automatically Breakthrough.” | primary v0.2 / `general_et_finding`: “Barrier Statement, reduction/dissolution, and Suppression Test belong to Section 11.2, operationally restated in Section 11.7; Section 11.5 concerns the framework's provenance and working status” | The old misattribution is absent; the new passage supplies the correct mapping. Both v0.2 outputs also acknowledge that they follow supplied locators rather than independently reading the full chapter. |
| 2. W2 contrast application relevance | Partial improvement; complete removal or material reduction not demonstrated | contrast_1 v0.1 / `application_finding`: “Distinguish model construction, operational scheduling and disruption recovery:” | contrast_1 v0.2 / `application_finding`: “no manufacturing comparison is required to judge the company's actual coordination task.” | The forced three-way manufacturing framing is removed. However, the response still includes the scheduling-model metric and manufacturing commentary. The application field grows from 163 to 196 whitespace-delimited words; length is descriptive, not a quality score. See residual discussion below. |
| 3. Ordered classification gates | Main analyses preserved; monitoring summary qualified | contrast_1 v0.1 / `general_et_finding`: “GATE 3, suppression: not established and cannot rescue Gate 2.” | contrast_1 v0.2 / `general_et_finding`: “Gate 3, Suppression Test, is not reached as an affirmative classification test.” | Both v0.2 main findings retain system, barrier, suppression, tiers, six criteria, and prospective conclusion, with later scoring not reached. The contrast follow-up trigger omits an explicit suppression-before-tiers order; see N1. |
| 4. General classification and context stability | Stable withholding observed across all four outputs | primary v0.1 / `general_et_finding`: “Gate 6, conclusion: withhold a positive significance category at Gate 2.” | primary v0.2 / `general_et_finding`: “Gate 6 conclusion: withhold a significance category because Gate 2 is unresolved.” | Contrast v0.1 and v0.2 likewise withhold at Gate 2. No new positive label or organization-driven classification shift appears. This is stable withholding, not an established Incremental/Breakthrough/Promethean classification or reliability estimate. |
| 5. C1-C5 attribution and limitations | Retained in reviewed content | primary v0.1 / `application_finding`: “it is not a tenfold productivity result or a live fab deployment. [C5]” | primary v0.2 / `application_finding`: “does not establish operational schedule feasibility, production throughput, or recovery effectiveness in semiconductor manufacturing [C5].” | Both v0.2 responses preserve five matched sources, dates/versions, experimental conditions, and transfer limits. No invented external source or local performance result was found. Syntactic ID checks do not replace manual entailment review. |
| 6. Context-specific management implications | Preserved, with different wording and emphasis | primary v0.1 / `recommendation_management_implication`: “Initiate the proposed six-month effort only as a gated evaluation” | primary v0.2 / `recommendation_management_implication`: “Authorize prerequisite definition and offline/shadow evaluation as a staged route toward a conditional six-month pilot.” | Contrast v0.2 conditionally considers the unchanged eight-week internal evaluation with read-only/draft-only authority. Both separate expansion from initial evaluation. Stronger Primary phrasing is a bounded judgment, not evidence that readiness changed. |
| 7. Critique, confidence and qualification | Observable behavior retained; robustness untested | contrast_1 v0.1 / `contrary_evidence_or_limitations`: “Reconsideration: the conclusion remains withheld” | contrast_1 v0.2 / `contrary_evidence_or_limitations`: “Reconsideration: the counterargument does not change the withheld conclusion” | Both v0.2 outputs contain a provisional judgment, strongest counterargument, affected gate, and reconsideration, plus separate GENERAL CLASSIFICATION/ORGANIZATION PILOT READINESS sections. No new contrary-evidence perturbation was run; within-answer critique is not proven self-correction under changed evidence. |
| 8. New errors, contradictions or omissions | No new major classification/empirical error found; minor omission N1 | contrast_1 v0.1 / `change_monitoring_triggers`: “after supported dissolution, reassess suppression” | contrast_1 v0.2 / `change_monitoring_triggers`: “only after dissolution is supported, assess distinct human-life tiers and all six criteria” | The revised contrast main analysis remains correct, but this follow-up instruction is less explicit about suppression-first order. No primary infrastructure or six-month premise was adopted by the contrast; references to manufacturer/wafer quality are explicit exclusions, not local assumptions. |

## W2 residual relevance issue
The contrast v0.2 application finding still says:
"The scheduling-model study concerns computational model construction, with 32/54 versus 8/54 strict successes for multi-agent+MCP versus direct LLM, not a measured administrative-work benefit. [C5]"
It then explains lack of transfer to the actual application. This is a more relevant explanation than requiring the manufacturing tripartite distinction, but it retains nonessential scheduling-study detail. Therefore: partial improvement in framing; no claim of complete removal or material reduction in discussion. The revised instruction did not require eliminating all C5 references, so this is not automatically a rule violation or context contamination. Do not infer better analytical performance merely from changed wording.

## N1 New minor omission in a reassessment trigger
Contrast v0.2 change_monitoring_triggers[1] says:
"RECOMMENDATION: only after dissolution is supported, assess distinct human-life tiers and all six criteria with supporting and contrary evidence; monitor demonstrated access changes, dependent innovations, and consequences of removing the same Agentic AI class, separating observation, counterfactual, and speculation."
It mentions removal consequences later, but does not explicitly place the Suppression Test before breadth/criteria as the main analysis and v0.1 trigger do. This is an abbreviated follow-up sequence, not a demonstrated incorrect classification: the actual v0.2 general finding stops at Gate 2 and explicitly includes Gate 3 before tiers. Preserve this as a remaining limitation. No third instruction change or extra retest is authorized/performed here.

## Other limits
- The candidate Barrier Statements remain explicitly unverified hypotheses; the packet still lacks the comparison needed to substantiate uniqueness or dissolution.
- Both v0.2 outputs request original course text if independent textual verification is required. This accurately reflects that the execution packets summarize the method without reproducing the full chapter. The parent review can check attribution against the supplied course files; the model does not claim to have done so.
- Self-critique remains a concise one-response judgment summary. No evidence-update challenge was introduced.
- One v0.2 run per case supports observed improvement on W1 and qualified W2 findings only. Sampling variation, metadata change, and uncontrolled model details preclude proof of causation or broad reliability.
- No successful organizational pilot, financial return, production-effectiveness result, safety certification, or independent professional judgment by the student is established.

## Stop boundary
No v0.2 response was rewritten. No additional instruction changes, case changes, evidence additions, further retests, Agent Record completion, independent student judgment, or Self-Reflection were performed. The remaining relevance and trigger limitations are documented for the user's review rather than silently repaired.
