# LLM-based Error Detection and Correction in Process Event Logs

This repository contains the source code and experimental notebooks for the research project **"Detection and Correction of Activity Label Errors in Event Logs using Large Language Models (LLMs)"**.

The project investigates how LLMs like GPT-3.5-turbo and GPT-4o can be used to detect and correct label-level anomalies (e.g., typos, pollution, homonyms, synonyms) in business process event logs. It focuses on evaluating the effectiveness of different abstraction strategies and prompt designs in improving event log quality.


## Datasets

We used the following benchmark datasets with injected activity label errors:

- **BPIC15**: Public permit application process (complex, high label variety)
- **Credit**: Structured credit application process (used for hom/syn experiments)
- **Pub**: Simplified civil complaint processing (used for comparative analysis)

Error types include:

- `DIST`: Distorted Labels (typos, character swaps)
- `POL`: Polluted Labels (concatenated tokens)
- `HOM`: Homonymous Labels (semantic conflict)
- `SYN`: Synonymous Labels (semantic similarity)

# Evaluation
All experiments are evaluated using F1 Score, Precision, and Recall, both for detection accuracy (whether an error is correctly identified) and fix accuracy (whether the output matches the clean log label exactly).

We also analyze:

- Abstraction impact (DFG vs. Variant)
- Model performance (GPT-3.5-turbo vs. GPT-4o)
- Prompt example sensitivity (0 to 4-shot)
