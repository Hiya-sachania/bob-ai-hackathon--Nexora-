# Solution Overview

## What We Built
We built a Clinical Trial Risk Monitor that helps risk managers quickly find problems in clinical trial data before they become bigger issues.
The system checks patient visit records against the study protocol and identifies problems such as missed visits, visits outside the allowed time window, incorrect dosing, prohibited or restricted medicines, missing assessments, and eligibility or consent issues.
Each detected problem is classified as Major, Minor, or Administrative. The system then combines these findings to calculate a risk score for each clinical trial site and places the site into a High, Medium, or Low risk tier.

## How It Works

1. We add the clinical trial data like sites, patients, visits, medicines, and doses.
2. The system checks the data with the study protocol.
3. It finds problems like missed visits, wrong doses, restricted medicines, or missing information.
4. Each problem is given a level — Major, Minor, or Administrative.
5. The system calculates a risk score for every site.
6. Sites are shown as High, Medium, or Low risk on the dashboard.
7. The user can click on a site to see its problems and recommended actions.
8. A CAPA report can be generated, and the site data can also be exported as a CSV file.

## Architecture Diagram

> See [`architecture.md`](architecture.md) for the detailed diagram.

[Optionally include a simple ASCII or Mermaid diagram here for quick reference.]

```
graph TD
    ["Clinical Trial Data<br>Sites, Subjects, Visits,<br>Dosing, Medications"] --> ["Frontend Web Application<br>HTML + CSS + Vanilla<br>JavaScript"] --> ["Protocol Specification"] --> ["Protocol Comparison &<br>Rules Engine"] --> ["Deviation Detection"] --> ["Deviation Records"] --> ["Severity Classification<br>Major / Minor /<br>Administrative"] --> ["Site-Level Risk Scoring"] --> ["Risk Tier<br>High / Medium / Low"] --> ["Risk Dashboard"] --> ["Site Investigation"] --> ["Portfolio CSV Export"] --> ["CAPA Recommendations &<br>Report"]
```

## Key Design Decisions

| Decision | Rationale |
|---|---|
| [e.g., Used watsonx.ai for anomaly detection] | [e.g., Pre-trained models reduced time-to-value vs. building from scratch] |
| [Decision 2] | [Rationale 2] |
| [Decision 3] | [Rationale 3] |

## IBM Technologies Used

[Explain specifically HOW you used each IBM technology — not just that you used it.]

- **[IBM Tech 1, e.g., watsonx.ai]:** [How it was used — e.g., "Used the `ibm/granite-13b-instruct-v2` model via the Python SDK to classify anomaly types from log text."]
- **[IBM Tech 2]:** [How it was used]
