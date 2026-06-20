# Artifact Manifest

This repository is the public artifact companion for the camera-ready paper
"Multi-Source Evidence Fusion for Audio Question Answering".

## Scope

The artifact documents TalTech's Agent Track winning solution for the
Interspeech 2026 MMAR Audio Reasoning Challenge. It is intended to provide the
materials referenced by the paper:

- example reasoning outputs,
- prompt templates,
- output schemas.

## Included

- `prompts/`: final prompt templates named by pipeline stage. Internal
  development-version labels are intentionally omitted from the public layout.
- `schemas/`: JSON Schemas for prompt-driven stages that return structured
  JSON.
- `samples/`: generated reasoning outputs for the 1,000 public MMAR benchmark
  samples. Each file records the sample ID, final answer, and reasoning chain.
- `README.md`: index table linking every sample to its reasoning output,
  question, choices, and answer.

## Not Included

- Raw audio files are not redistributed here.
- Challenge evaluation infrastructure and private submission services are not
  included.
- The codebase used to run local acoustic tools is not part of this archive;
  this repository is the public prompt/schema/output artifact referenced by the
  paper.

## Dataset Note

The MMAR benchmark metadata are public. Benchmark questions, answer choices,
and answer labels are included only to make the generated reasoning outputs
readable and traceable. Third-party benchmark content remains subject to the
original MMAR dataset terms.
