# CrossStrait-AuditKit

Reproducible counterfactual audit pipeline and diagnostic literature database accompanying:
> **Explainable Detection of Cross-Strait Disinformation in Chinese-Language Social Media: A Critical Survey of Datasets, Methods, Explanations, and Evaluation Practice** (Adarsh R Shenoy & Brij B Gupta, 2026)

## Contents
- `run_cofacts_audit.py`: Deterministic OpenCC script (`t2s` / `s2t`) and regional-lexicon (`tw2sp` / `s2twp`) counterfactual generator with exact McNemar testing and bootstrap confidence intervals.
- `cofacts_audit_results.csv`: Empirical Audit 1 results on temporally held-out Cofacts LINE messages ($N=400$) across `Chinese-RoBERTa-wwm`, `Chinese-MacBERT`, `Qwen2.5-7B-Instruct`, and `Breeze-7B-Instruct`.
- `appraised_studies.json`: Structured 6-feature diagnostic rubric matrix across 12 core Chinese-language empirical studies (Appendix A).

## Data Attribution
Cofacts evaluation records are accessed via [`Cofacts/line-msg-fact-check-tw`](https://huggingface.co) under **CC BY-SA 4.0**.
