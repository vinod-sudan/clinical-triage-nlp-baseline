# Clinical Triage NLP & Safety-Gate Baseline (`MIMIC-IV-ED`)
A reproducible baseline comparing classical multimodal feature fusion (`TF-IDF + Structured Vital Signs + Logistic Regression`) against domain-adapted Clinical Transformers (`Bio_ClinicalBERT`) for Emergency Severity Index (`ESI 1–2` vs. `ESI 3–5`) triage classification.
## Key Highlights
- **Clinical Text Normalization:** Expands emergency nursing shorthand (e.g., `sob` → *shortness of breath*, `cp` → *chest pain*).
- **Multimodal Fusion:** Combines unstructured chief-complaint representations with standardized arrival vital signs (`heartrate`, `sbp`, `dbp`, `resprate`, `o2sat`, `temperature`).
- **Clinical Safety Evaluation:** Evaluates **AUROC**, **Macro-F1**, **Critical Under-Triage Rate** (false negatives on life-threatening `ESI 1–2` cases), and **Uncertainty-Based Clinician Escalation** (`0.35–0.65` confidence deferral zone).
## Data Governance Note
No raw `MIMIC-IV-ED` clinical text or patient records are stored in this repository in compliance with the PhysioNet Credentialed Health Data Use Agreement. Set `USE_SYNTHETIC = False` locally with credentialed `triage.csv.gz` access to reproduce full cohort benchmarks.
