# Prompt Materials

This directory contains the final prompt templates published with the camera-ready artifact.
Internal development-version labels were removed from the file layout; files are named by pipeline stage.

- `stepaudior1_observation_query.txt` and `qwen_observation_query.txt` request source-specific audio observations.
- `evidence_synthesis.txt` merges full-audio and focused-listener observations into scored evidence.
- `unified_evidence_analysis.txt` compares the two independent speech-LM sources.
- `reliability_evaluation.txt` labels observations as evidence-based, speculative, or potentially hallucinated.
- `contradiction_detection.txt` identifies evidence conflicts and proposes targeted verification hypotheses.
- `hypothesis_result_evaluation.txt` evaluates targeted verification results.
- `observation_reinterpretation.txt` re-evaluates raw observations without source predictions.
- `final_argumentation.txt` generates the final reasoning chain.
- `shortcut_argumentation.txt` generates concise reasoning when evidence is already consistent.
- `reasoning_compaction.txt` shortens over-length reasoning while preserving the answer.

JSON Schemas for structured prompt outputs are in [`../schemas`](../schemas).

The contradiction-detection stage combines rule-based evidence bookkeeping with an LLM prompt. Rule-based code assigns reliability labels, confidence caps, domain-appropriateness adjustments, and initial hallucination-risk indicators. The LLM prompt then assesses relevance, classifies contradictions, proposes status updates, and generates targeted verification hypotheses.
