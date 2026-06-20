# Agent Track Winning Solution - MMAR Audio Reasoning Challenge (Interspeech 2026)

This repository contains the public artifact materials for TalTech's Agent Track winning solution in the **MMAR Audio Reasoning Challenge**, held as part of Interspeech 2026.

It accompanies the camera-ready paper, "Multi-Source Evidence Fusion for Audio Question Answering", and provides the materials promised there: example reasoning outputs, prompt templates, and structured output schemas.

## Contents

- [`prompts/`](prompts) contains the final prompt templates, with development-version labels removed.
- [`schemas/`](schemas) contains JSON Schemas for structured outputs expected from prompt-driven stages.
- [`samples/`](samples) contains detailed reasoning chains for all 1,000 public MMAR benchmark samples.

## Prompts and Schemas

The camera-ready paper refers readers here for detailed prompt text and output schemas.

The prompt files are named by pipeline stage rather than by internal development version. They cover source observation queries, evidence synthesis, reliability evaluation, contradiction detection, targeted hypothesis evaluation, answer selection, reasoning generation, and reasoning compaction.

The schema files describe the JSON outputs used by structured stages such as evidence synthesis, contradiction detection, reliability evaluation, and hypothesis-result evaluation.

## About the Challenge

The MMAR (Multimodal Music, Audio, and Reasoning) benchmark comprises **1,000 samples** spanning speech, sound, music, and mixed-modality audio. Each sample includes an audio clip, a question, a correct answer, and annotated reasoning rationales.

Submissions are evaluated on both **answer correctness** and **reasoning quality**. When the predicted answer is correct, an LLM evaluator scores the reasoning chain on a scale of 0.2 to 1.0. Each submission undergoes five independent evaluation runs, with the final score being the mean of the three middle runs.

The benchmark metadata are public. This repository does not redistribute raw audio files; it publishes prompt materials, output schemas, and generated reasoning outputs for the public benchmark samples.

## Citation and License

Please cite the paper and this artifact if you use these materials. Citation metadata is provided in [`CITATION.cff`](CITATION.cff). The repository's own prompt text, schemas, documentation, and generated reasoning outputs are licensed under CC BY 4.0; third-party benchmark content remains subject to the original MMAR dataset terms.

## Reasoning Outputs

The repository includes generated reasoning chains for all 1,000 public MMAR benchmark samples in [`samples/`](samples). The complete index is in [`samples/INDEX.md`](samples/INDEX.md).

The examples below are selected to show the behavior discussed in the paper rather than to mirror the dataset table:

| Sample | What it illustrates | Paper concept |
|---|---|---|
| [`3juD91EThtY_00-00-00_00-00-26`](samples/3juD91EThtY_00-00-00_00-00-26.md) | Resolves an invalid question premise and a conflicting speaker-count tool result. | Contradiction-driven verification |
| [`WQ_wO0r16ww_00-00-01_00-00-26`](samples/WQ_wO0r16ww_00-00-01_00-00-26.md) | Separates real animal presence from human imitations using transcript evidence and source disagreement. | Reliability-tiered evidence |
| [`qZbf5zdg4JU_00-00-00_00-00-07`](samples/qZbf5zdg4JU_00-00-00_00-00-07.md) | Weighs contradictory sport-impact claims in a music-dominated clip against energy and spectral checks. | Tool relevance scoring |
| [`BV1nH4y1u7kt_00-00-00_00-00-30`](samples/BV1nH4y1u7kt_00-00-00_00-00-30.md) | Resolves semantic ambiguity in a music question where "cat" may mean a musician rather than an animal. | Question-aware evidence interpretation |
| [`BV1sf4y1i7Ec_00-00-06_00-00-31`](samples/BV1sf4y1i7Ec_00-00-06_00-00-31.md) | Filters an external movie-identification claim and grounds the answer in transcript and acoustic cues. | Hallucination-risk filtering |
| [`BV1VN411H7nt_00-00-18_00-00-35`](samples/BV1VN411H7nt_00-00-18_00-00-35.md) | Weighs conflicting claims about female vocals against corroborated observations and limited tool outputs. | Evidence weighting under uncertainty |
