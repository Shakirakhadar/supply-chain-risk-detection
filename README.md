#Supply Chain Risk Detection
This project explores anomaly detection in supply chain data, enhanced with Large Language Models (LLMs). It combines traditional tabular methods with semantic embeddings from textual logs to better identify fraud and disruption risks.

#Project Structure

notebooks/
│
├── supply_chain_fraud_analysis.ipynb   # main notebook (final pipeline)
├── fraud_analysis.py                   # sample script with smaller dataset
results/     # saved plots, metrics, evaluation outputs
report/      # final structured report (≤6 pages)
README.md    # project overview and setup instructions

`notebooks/supply_chain_fraud_analysis.ipynb` : Main notebook containing the final workflow and experiments.
`notebooks/fraud_analysis.py` : Sample script used for initial testing with a smaller dataset (kept for reference).



#Setup Instructions
Clone the repository

*bash
git clone https://github.com/Shakirakhadar/supply-chain-risk-detection
cd supply-chain-risk-detection


Install dependencies

*bash
pip install -r requirements.txt


Dataset  
Download the dataset from: https://www.kaggle.com/datasets/shashwatwork/dataco-smart-supply-chain-for-big-dataanalysis
Place the file in the root folder.

API Key  
This project uses the OpenAI API for embeddings.

Set your key as an environment variable:

*Windows PowerShell: setx OPENAI_API_KEY "your_api_key_here"
*macOS/Linux: export OPENAI_API_KEY="your_api_key_here"

Or replace "YOUR_API_KEY_HERE" in the notebook.

#Note: Running the notebook requires an active OpenAI account with credits. Without credits, API calls will return a RateLimitError.

#Methodology
Baseline: Isolation Forest and Gradient Boosting on numeric features (order amounts, shipping days, delays).

LLM Enhancement: Textual details (order descriptions, customer notes, logs) converted into embeddings and merged with numeric features for hybrid anomaly detection.

#Results
Evaluation outputs (plots, metrics, confusion matrices) are saved in the results/ folder.
The detailed analysis and discussion are available in the report/ directory.

#Reproducibility
This repository contains:

Clean, documented notebooks and scripts.
Dataset link for download.
Saved metrics and plots.
A structured project report.

Anyone with an OpenAI API key and credits can reproduce the experiments end‑to‑end.