
# AIDev PR Outcome: Early-Signal Prediction

This repo trains simple models (Logistic Regression, Random Forest) to predict
**PR outcome** (merged vs closed) using the **AIDev** dataset hosted on Hugging Face,
plus generates basic EDA visuals.

## Dataset
We read directly from the Hub via `hf://` paths:
- `hao-li/AIDev` (`pull_request.parquet`, `repository.parquet`)
- Optional: `pr_commit_details.parquet`, `pr_review_comments.parquet`

Public datasets need no token. If you do need auth:
```python
from huggingface_hub import login
login()  # paste token
