\# Hoax Detection System



This project is a \*\*hybrid Fake News / Hoax Detection System\*\* combining \*\*AI (Transformers)\*\*, \*\*NLP\*\*, a \*\*rule-based expert system\*\*, and \*\*Gemini API fact verification\*\*. It provides \*\*reliable real-time classification\*\* of text into \*\*real\*\*, \*\*fake\*\*, or \*\*misleading\*\*.



---



\## Features



1\. \*\*AI-Based Classification\*\*  

&nbsp;  Uses a fine-tuned \*\*DistilRoBERTa/BERT\*\* model to classify news text accurately.



2\. \*\*Gemini Fact Verification\*\*  

&nbsp;  Automatically queries \*\*Google Gemini\*\* to verify factual claims and returns a \*\*short, evidence-based explanation\*\*.



3\. \*\*Rule-Based Expert System\*\*  

&nbsp;  Analyzes content using \*\*heuristic rules\*\* (keyword patterns, exaggeration, propaganda indicators, emotional terms, formatting anomalies) and outputs a \*\*Suspicion Score\*\*.



4\. \*\*Batch Processing\*\*  

&nbsp;  Supports `.txt`, `.csv`, and `.xlsx` files and produces combined results containing:

&nbsp;  - Model prediction

&nbsp;  - Rule analysis

&nbsp;  - Gemini verification



5\. \*\*Secure API Handling\*\*  

&nbsp;  Uses \*\*Google Colab Secrets\*\* to store the API key safely inside the notebook.



---



\## Project Structure

HoaxDetectionSystem/

├── HoaxDetectionSystem.ipynb

├── README.md

├── sample\_data/

│   ├── True.csv

│   └── Fake.csv

└── output/



---



\## Pipeline



```mermaid

graph TD

&nbsp;   A\[Input Text] --> B\[Preprocess]

&nbsp;   B --> C\[Transformer Model<br/>(DistilRoBERTa/BERT)]

&nbsp;   B --> D\[Rule-Based Heuristics<br/>(Suspicion Score)]

&nbsp;   B --> E\[Gemini Fact-Check<br/>(Evidence)]

&nbsp;   C --> F\[Combine Results]

&nbsp;   D --> F

&nbsp;   E --> F

&nbsp;   F --> G\[Final Verdict:<br/>Real / Fake / Misleading]



---



\## Requirements



Install required dependencies:



```bash

pip install transformers datasets evaluate pandas google-generativeai openpyxl

