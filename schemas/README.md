# Output Schemas

This directory contains JSON Schemas for the prompt-driven stages that return structured JSON.
They document the output contracts used by the public prompt templates in [`../prompts`](../prompts).

- `evidence_synthesis.schema.json`: scored evidence list from multi-listener observations.
- `unified_evidence_analysis.schema.json`: comparison of two speech-LM observation sources.
- `reliability_evaluation.schema.json`: reliability labels for individual observations.
- `contradiction_detection.schema.json`: contradiction analysis, evidence status updates, and verification hypotheses.
- `hypothesis_result.schema.json`: result of targeted hypothesis verification.
- `observation_reinterpretation.schema.json`: source-blind re-evaluation of raw observations.
