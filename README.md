# Clinical-NLP-Pipeline-for-Symptom-Extraction-and-Classification
Built an NLP pipeline using spaCy, SecTag, INCEpTION, and LangChain-integrated LLMs to extract and classify symptoms from clinical notes. Identified presence/absence of symptoms and evaluated tool performance using annotated datasets.

Objective
To develop an NLP pipeline to:
Extract the Subjective section from clinical notes using SecTag.
Extract symptoms/diseases using spaCy.
Classify the presence/absence of symptoms using LangChain + Ollama (LLM).
Evaluate tools' utility and limitations.

Tools' Utility and Limitations

INCEpTION
1. Utility: Used for manual annotation of diseases and symptoms as present or absent for evaluation.

2. Strengths:
Easy-to-use web interface.
Supports multiple annotators.
Allows schema customization for annotation types.

3. Limitations:
Manual annotation is time-consuming.
No automatic extraction capabilities.
Does not support direct NLP pipeline integration.

SecTag
1. Utility: Used to extract structured sections (like "Subjective") from unstructured clinical notes.
   
2. Strengths:
Based on clinical section header patterns.
Good for section-specific NLP tasks.


4. Limitations:
Relies on accurate headers.
Misses data if headings are inconsistent or missing.

spaCy
1. Utility: Used to extract symptoms and disease keywords from the Subjective section.
2. Strengths:
Fast, efficient NLP processing.
Flexible rule-based pattern matching.

3. Limitations:
Limited contextual understanding.
May extract false positives (e.g., mentioned but not experienced symptoms).

LangChain + Ollama (LLM)
1. Utility: Used to classify whether extracted symptoms are present or absent based on patient context.
2. Strengths:
Strong contextual reasoning.
Easy prompt customization.
3. Limitations:
Requires local Ollama setup.
May produce variable results without prompt tuning.

Detailed Implementation Steps
Set Up the Environment.
Install dependencies.
Start Ollama: ollama run llama3.2
Create sectag_utils.py with Header Functions.
Write and Run clinlp_pipeline.py
Annotate Using INCEpTION.
