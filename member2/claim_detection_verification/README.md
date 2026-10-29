# Member 2 — Claim Detection and Verification

This folder implements the M2 stage of the Dehallucination Add-On Module for Enhancing Reliability of AI Applications.

## Implemented functionality
- DH-009: sentence-like claim segmentation and stable claim IDs.
- DH-010: heuristic risk signals for numbers, dates/years, possible named entities, superlatives, polarity, and missing evidence.
- DH-011: claim-evidence verification labels: supported, partially_supported, contradicted, and unverified.
- DH-012: configurable scoring thresholds and claim-level risk scores.

## Run
Requires Python 3.10+; uses only Python's standard library.

```bash
python demo.py
python -m unittest discover -s tests -v
```

## Limitations
This is a deterministic rule/lexical-overlap MVP, not a trained NLI model. Lexical overlap is not proof of semantic entailment and the reliability score is not a calibrated probability. Use a reviewed, sourced benchmark before reporting accuracy or using it for high-risk decisions. Synthetic examples are software fixtures only.
