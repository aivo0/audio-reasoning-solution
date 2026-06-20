# Prompt Materials

The final system used both v10 and v11 prompt families.

- `v10/` covers evidence-only tool-loop prompts, including reliability evaluation, contradiction detection, hypothesis-result evaluation, answer selection, shortcut argumentation, and compaction.
- `v11/` covers source observation queries, evidence synthesis, and the final reasoning-generation prompt used after answer selection.
- `contradiction_detection_schema.json` summarizes the JSON object expected from `v10/contradiction_detection.txt`.

The contradiction-detection stage combines rule-based evidence bookkeeping with an LLM prompt. Rule-based code assigns reliability labels, confidence caps, domain-appropriateness adjustments, and initial hallucination-risk indicators. The LLM prompt then assesses relevance, classifies contradictions, proposes status updates, and generates targeted verification hypotheses.
