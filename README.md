# CrossStrait-AuditKit

Reproducible counterfactual audit pipeline and diagnostic literature database accompanying:
> **Explainable Detection of Cross-Strait Disinformation in Chinese-Language Social Media: A Critical Survey of Datasets, Methods, Explanations, and Evaluation Practice** (Adarsh R Shenoy & Brij B Gupta, 2026)

## Quickstart & Reproducibility
1. **Accept Dataset Terms:** Request access to [`Cofacts/line-msg-fact-check-tw`](https://huggingface.co/datasets/Cofacts/line-msg-fact-check-tw) (CC BY-SA 4.0) on Hugging Face.
2. **Set Your Hugging Face Read Token:**
   - **Local / Google Colab:** `export HF_TOKEN="your_hf_read_token"`
   - **Kaggle:** Add `HF_TOKEN` under **Add-ons → Secrets** and enable a GPU accelerator (T4 or P100).
3. **Install & Execute:**
   ```bash
   pip install -r requirements.txt
   jupyter nbconvert --to notebook --execute cofacts-audit.ipynb
   ```

## Contents
- `cofacts-audit.ipynb`: End-to-end temporal split loader, deterministic OpenCC script (`t2s`) and regional-lexicon (`tw2sp`) counterfactual generator, encoder fine-tuning, 4-bit LLM next-token log-odds audit, exact McNemar/bootstrap testing, and figure generation.
- `cofacts_audit_results.csv`: Empirical Audit 1 results on temporally held-out Cofacts LINE messages ($N=400$) across `Chinese-RoBERTa-wwm`, `Chinese-MacBERT`, `Qwen2.5-7B-Instruct`, and `Breeze-7B-Instruct` (Table 9).
- `appraised_studies.json`: Structured 6-feature diagnostic rubric matrix across 12 core Chinese-language empirical studies (Appendix A, Table 11).
- `requirements.txt`: Exact Python package dependencies for reproducing the benchmark environment.

## Data Attribution
Cofacts evaluation records are accessed via [`Cofacts/line-msg-fact-check-tw`](https://huggingface.co/datasets/Cofacts/line-msg-fact-check-tw) under **CC BY-SA 4.0**.
