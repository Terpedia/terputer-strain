# Terputer: Cannabis Strain Chemistry and Terpotype

The [executed Terputer notebook](notebooks/analysis.ipynb) counts rows and columns in the archived export and extracts the upstream classification summary. Its saved cell outputs document the results of this audit. The [execution receipt](research/execution-receipts/analysis.json) identifies the exact notebook version.

Standalone package for source archive variability and name-independent chemical-profile classification. The 43,018-row source export, selected derived tables, and source analysis summary are included. The notebook audits available outputs and performs a small data inventory; it does not silently rerun or claim to reproduce every upstream Colab model result.

## Run

Install `requirements.txt`, then open `notebooks/analysis.ipynb` in Jupyter. Raw profile data is in `data/cannabis_terpene_profiles.csv`.

## Interpretation

Observed name associations are not genotype effects. The source archive lacks matched genotype and cultivation metadata, so causal genomic/environmental effects remain unestimated.


## Terpedia access

The optional client in `src/terpedia_access.py` calls the Terpedia Knowledge API at `/v1/tabular/search`. It reads `TERPEDIA_KNOWLEDGE_API_KEY` and `TERPEDIA_KB_API_URL` from the process environment and sends the key in the `x-knowledge-key` header. Copy `.env.example` as a configuration reference, then provide the real key through a local secret manager, Codespaces secret, or authorized GitHub Actions secret. Never commit `.env` or print the key in notebook output.
