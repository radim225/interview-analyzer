# Interview Answer Analyzer

Streamlit app that scores a “Why should we hire you?” answer with Azure AI Language (sentiment + key phrases).

## Security

The Azure key and endpoint are read from environment variables or a local `.env` file, which is listed in `.gitignore`, so no credentials are stored in the repository.

## Setup

1. Create a Python virtual environment and install dependencies:

   ```bash
   python3 -m venv .venv
   source .venv/bin/activate
   pip install -r requirements.txt
   ```

2. Copy the env template and fill in **your** Azure Language resource values (placeholders only — never commit real keys):

   ```bash
   cp .env.example .env
   ```

   Required variables:

   | Variable | Description |
   | --- | --- |
   | `AZURE_COGNITIVE_KEY` or `AZURE_LANGUAGE_KEY` | Subscription key from Azure Portal → your resource → Keys and Endpoint |
   | `AZURE_COGNITIVE_ENDPOINT` | Endpoint URL, e.g. `https://YOUR-RESOURCE.cognitiveservices.azure.com/` |

3. Run the app:

   ```bash
   streamlit run sentiment_test.py
   ```

`.env` is gitignored. Do not hardcode keys in source, PRs, or screenshots.
