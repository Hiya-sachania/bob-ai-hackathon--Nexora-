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
| [Used rules to check the protocol] | [The protocol has specific rules for visits, doses, medicines, and tests, so rules make it easier to find mistakes.] |
| [Divided deviations into Major, Minor, and Administrative] | [This helps us understand how serious each problem is.] |
| [Created a risk score for each site] | [It helps us quickly find which sites have more problems and need attention first.] |
| [Added site details and CAPA recommendations] | [The risk manager can see the problem, understand why the site is risky, and decide what action to take.] |
| [Used synthetic data] | [We can test and demonstrate our project without using real patient data.] |

## IBM Technologies Used

IBM BOB: We used IBM BOB as part of the hackathon to help develop web page/solution. The final prototype focuses on clinical trial protocol checking, deviation detection, site risk scoring, and CAPA recommendations.
