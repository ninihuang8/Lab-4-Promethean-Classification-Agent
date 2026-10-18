# Specialist revision v0.2
Session date: 2026-10-17 (America/New_York)

## Preserved baseline
Original metadata version: 0.1-student.
Original specialist instructions SHA-256: 9a39ca5aeab52c680fe112675a039936e9b4598e7f5e1fcffafbc1ce3fc34538
Exact baseline copy: records/specialist_instructions_v0_1.md.
The unchanged v0.1 prompt packets also embed the complete original instructions and metadata. Both original responses and all Step 8 records are preserved. Cases, evidence EP-A4-0.1, frozen files and schemas are unchanged.

## Approved changes and observed evidence
W1: primary_response_v0_1.json / general_et_finding says "Under Section 11.5, return of the old state would indicate reduction and Breakthrough at most, not automatically Breakthrough." The rule is in Section 11.2 (printed p.144), restated in Section 11.7 (p.150); Section 11.5 concerns framework provenance and working status. Add the user-approved section-attribution rule verbatim. Expected effect: accurate method locators without changing the diagnostic.

W2: contrast_1_response_v0_1.json / application_finding says "Distinguish model construction, operational scheduling and disruption recovery: the scheduling study assesses construction of constraint-programming models in computational experiments, not demonstrated operational scheduling or disruption recovery; none of those manufacturing functions is the present application [C5][H1]." The original bullet required this manufacturing distinction for every case. Restrict it to semiconductor scheduling applications and require relevant transfer limits for other applications. Retain the general benchmark-scope safeguard. Expected effect: a more relevant contrast application finding without relaxing evidence discipline.

Metadata-only version change: agent_metadata.json version 0.1-student -> 0.2-student; name and specialty unchanged. No additional analytical changes were made. Expected effects are hypotheses to test, not reported improvements.

## Exact instruction diff
```diff
--- v0.1/specialist_instructions.md
+++ v0.2/specialist_instructions.md
@@ -12,6 +12,8 @@
 
 ## Analytical framework the agent must apply
 Follow the gates in order. State the earliest unresolved or failed gate; later promise cannot bypass it.
+
+Attribute the Barrier Statement, dissolution/reduction distinction, and Suppression Test to Chapter 11 Section 11.2, with the operational restatement in Section 11.7. Section 11.5 concerns the provenance and working status of the framework, not the suppression diagnostic. Check cited section locators before returning the response.
 
 1. **System or component.** Fix the object of assessment. Agentic AI means a bounded class of integrated, model-directed systems that select tool-mediated actions and use environmental feedback to pursue delegated goals within permissions and human oversight. This operational definition is not proof of capability. Distinguish the class from Generative AI generally, a model alone, fixed automation, and the proposed unbuilt semiconductor deployment. Establish usable-system evidence from the packet. An unassembled component is Not Yet Evaluable; unknown system existence or scope requires qualification or withholding and a request for evidence.
 
@@ -31,7 +33,7 @@
 - `agent`: copy supplied metadata.
 - `analytical_question`: bounded specialist question and decision.
 - `general_et_finding`: fixed system boundary, prospective mode, ordered gates, criteria if reached, and final qualified classification or withholding rationale.
-- `application_finding`: implications for the intended use; distinguish model construction, operational scheduling, and disruption recovery. Benchmark success is not semiconductor effectiveness.
+- `application_finding`: implications for the intended use. For semiconductor scheduling applications, distinguish scheduling-model construction, operational scheduling, and disruption recovery; benchmark success is not semiconductor effectiveness. For other applications, explain the actual application's evidence-transfer limits without requiring an irrelevant manufacturing comparison. In every application, retain the rule against transferring benchmark results beyond their demonstrated scope.
 - `organization_specific_finding`: conditional implications of hypothetical premises. Ask Section 11.8's question: which barrier is changing, and is this intended or occurring without management direction? Distinguish assistance from delegated scheduling authority.
 - `evidence`: verified claims actually used, formatted below.
 - `contrary_evidence_or_limitations`: strongest supporting and opposing cases, followed by concise entries labeled Provisional classification, Strongest credible counterargument, Affected gate, and Reconsideration. Explain whether the conclusion changes and why, even if it remains withheld. Keep the final finding consistent. This is an observable decision summary, not a guarantee of correctness or an invented prior run.
```

## Retest plan and bounds
Regenerate primary_prompt_v0_2.txt and contrast_1_prompt_v0_2.txt using the original builder and unchanged cases. Check embedded case/evidence equality with v0.1 and validate the instruction diff is limited to W1/W2. Execute one first response per case in fresh no-history sessions using the Step 8 delivery procedure; preserve raw output without repair. Compare actual passages for W1/W2, gate order, general stability, evidence scope, local recommendations, critique, confidence and new errors. No causal or reliability guarantee follows from two retests. No Agent Record, personal judgment, or self-reflection is authored in this step.

Revised instructions SHA-256: 4347d10be4687ef65cb4645421da09a3c676cd1c6c8ac072d021ed9c77235075
