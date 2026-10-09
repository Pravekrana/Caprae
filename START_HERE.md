# Caprae assessment submission

LeadBench is a working full-stack prototype for reviewing company quality and acquisition fit before enrichment. It implements two focused features: conservative CSV reconciliation with source evidence, and explainable buy-box prioritization with shortlist and export actions.

## Run the application

Open `caprae-lead-workbench/README.md` for the complete instructions. On Windows, run `caprae-lead-workbench/launch.ps1`; on a machine with Python 3.10 or later, run `python server.py` from that folder. Open http://127.0.0.1:8765, choose **Import leads**, then **Use demo CSV** and **Review leads**.

The application uses Python's standard library, SQLite, and HTML/CSS/JavaScript. It needs no API key, paid enrichment subscription, or package installation. Its synthetic records use reserved example domains. Importing the demo repeatedly does not create duplicate companies.

## Contents

| Material | Location |
| --- | --- |
| Application, setup instructions and API examples | `caprae-lead-workbench/` |
| Architecture, decisions and hosting path | `caprae-lead-workbench/docs/ARCHITECTURE.md` and README |
| Synthetic dataset | `caprae-lead-workbench/data/demo_leads.csv` |
| Portable Git history | `LeadBench_Source.bundle` |
| Publication instructions | `submission-materials/PUBLISHING.md` |
| Automated tests | `caprae-lead-workbench/tests/` |
| Validation evidence | `submission-materials/VALIDATION.md` |
| 108-second captioned walkthrough | `submission-materials/walkthrough.webm` |
| Walkthrough outline and recording notes | `submission-materials/VIDEO_NOTES.md` |
| Business understanding and applicant answer fields | `submission-materials/BUSINESS_RESPONSES.md` |
| Handbook requirement mapping | `submission-materials/REQUIREMENTS.md` |
| Recruiting email draft | `submission-materials/EMAIL_DRAFT.md` |

The video explains the actual prototype through captured screens and captions. It has no spoken narration. If an applicant-presented recording is expected, use the included outline to record a version in your own voice.

## Submission items that still require the applicant

- Publish the prepared source repository to your authenticated GitHub account and insert the URL in the email draft. No authenticated GitHub publishing capability was available in this session.
- Supply your actual full name, current resume, US work status, salary expectation, availability, earliest start date, and agreement to the employment terms. These facts have not been invented.
- Review the proposed motivation responses so they reflect your own reasons.
- Add the repository and video links, attach the resume, and send the email when those fields are complete. The draft has not been sent.

The source handbook is private and confidential and is not redistributed in this package. The implementation is an independent assessment prototype, with public SaaSquatch information used for product research. It does not access a SaaSquatch account, scrape live websites, verify contact deliverability, or use a trained AI scoring model.

## Review approach

A lower-cost GPT-6-luna agent with medium reasoning implemented the code and technical documentation. The primary agent reviewed the brief, product scope, backend boundaries, source preservation, prioritization semantics, and browser behavior, then prepared the business responses, walkthrough, and package. Development remained within the handbook's five-hour limit; a production deployment was not performed.
