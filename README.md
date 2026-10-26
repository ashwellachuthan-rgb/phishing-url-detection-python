# Phishing Website Detection Using Machine Learning

**Student:** A. Ashwell  
**Programme:** B.Tech Cyber Security  
**Programme context:** IBM SkillsBuild Cyber Security 2026

## Project description
This educational project extracts simple text-based features from website URLs and uses a Random Forest classifier to demonstrate phishing-URL classification.

## Files
- `Ashwell_PhishingDetection.ipynb` — complete runnable notebook
- `requirements.txt` — Python dependencies
- `Ashwell_ProjectReport.docx` — project report
- `README.md` — project overview and run instructions

## Dataset
The notebook first looks for a CSV named `phishing_site_urls.csv` in the same folder. It must have:
- `URL` — website URL text
- `Label` — labels such as `good` / `bad`, `legitimate` / `phishing`, or `benign` / `malicious`

If that CSV is absent, the notebook uses a tiny hand-written demo dataset so the workflow can run. **The fallback dataset is only for demonstration. Its score is not evidence of real-world accuracy.**

For a proper evaluation, obtain a reputable, permitted phishing/legitimate URL dataset from a trusted research or educational source. Record its exact source, date, terms/licence and any preprocessing in your report. Do not download datasets from unknown sites or run suspicious URLs.

## Setup
1. Install Python 3.10 or later.
2. Extract this project folder.
3. Open a terminal in the folder.
4. Install dependencies:

   ```bash
   python -m pip install -r requirements.txt
   ```

5. Start Jupyter:

   ```bash
   jupyter notebook
   ```

6. Open `Ashwell_PhishingDetection.ipynb` and run the cells from top to bottom.

## How it works
1. Reads labelled URL data or loads the demonstration sample.
2. Extracts lexical features such as URL length, punctuation counts, HTTPS indicator, IP-address host indicator and selected suspicious words.
3. Trains a Random Forest classifier.
4. Prints evaluation metrics for the available data split.
5. Predicts a label for a user-provided URL.

## Important limitations
This is a student learning prototype, not a production anti-phishing tool. It does not visit or scan websites and cannot guarantee that any URL is safe. A model trained on the fallback demo sample is especially unreliable. Never enter credentials into a suspicious site based on this model's prediction alone.

## Suggested future improvements
- Evaluate with a larger, documented, labelled dataset.
- Remove duplicate URLs and prevent train/test leakage.
- Add cross-validation and precision/recall/F1 reporting.
- Add time-based testing to measure performance on newer URLs.
- Consider page/domain reputation signals only from trusted, legally permitted sources.
