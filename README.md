# EcoAssist — ESG Sustainability Incident Reporter
**BUS5001 Assessment | Google Conversational Agents (Dialogflow CX)**

---

## Overview
EcoAssist is a conversational AI chatbot prototype designed to support 
organisational ESG (Environmental, Social and Governance) operations. 
The chatbot allows employees to report sustainability and ethical incidents 
through a structured, guided conversation flow.

Built using Google Conversational Agents (formerly Dialogflow CX) as part 
of a university assessment exploring cloud-based AI solutions in an 
enterprise ESG context.

---

## ESG Use Case
**Sustainability Incident Reporter** — employees can report environmental, 
ethical, governance or health and safety incidents through a conversational 
interface. High and critical severity incidents are automatically escalated 
to the ESG response team.

---

## Chatbot Flow

| Page | Purpose |
|---|---|
| Start Page | Entry point, triggers welcome |
| Welcome | Greets user, detects report intent |
| Collect Incident Type | Captures incident category via @incident-type entity |
| Collect Location | Captures incident location |
| Collect Description | Captures free-text description |
| Collect Severity | Captures severity via @severity-level entity |
| Confirmation | Summarises report, routes based on severity |
| Report Submitted | Confirms submission, provides reference number |
| Escalated | Triggers urgent escalation for High/Critical severity |
| Cancelled | Ends session without submitting |

---

## Custom Entities

**@incident-type**
- Environmental
- Ethical
- Governance
- Health and Safety

**@severity-level**
- Low
- Medium
- High
- Critical

---

## Intents

| Intent | Purpose |
|---|---|
| report.incident | Triggers the incident reporting flow |
| confirm.yes | User confirms report submission |
| confirm.no | User cancels submission |
| request.human | Routes user to human ESG team |

---

## Escalation Logic
On the Confirmation page, a conditional route checks 
`$session.params.severity`:
- **High or Critical** → Escalated page (urgent ESG team notification)
- **Low or Medium** → Report Submitted page (standard 5-day review)

---

## Screenshots
All screenshots are located in the `/screenshots` folder:
- Conversational Agents flow canvas
- Entity types configuration
- Intents list
- Confirmation page routing logic
- Simulator test conversation

---

## Technology
- Platform: Google Conversational Agents (Dialogflow CX)
- Region: australia-southeast1
- Language: English (en)
- Project: EcoAssist

---

## Demonstration Video
[Microsoft Stream link — insert here after recording]

---

## References
Google. (2024). *Dialogflow CX documentation*. 
https://cloud.google.com/dialogflow/cx/docs



## NotebookLM Evaluation (Q4)

### Academic Scenario

Comparison of GRI 305 emissions disclosures and BHP greenhouse gas reporting and climate governance.

### Features Evaluated

- Chat with sources
- Notes and summaries
- Mind map
- Audio overview
- Study guide

### Repository Contents

#### screenshots
Contains screenshots of NotebookLM outputs and generated materials.

#### experiment_logs
Contains the experiment log and observations from the NotebookLM evaluation.

#### documents
Contains report drafts and supporting files.

### Key Findings

NotebookLM provided accurate and useful source-grounded answers and study aids. The generated summaries and audio overview were valuable for revision and understanding complex ESG concepts. However, all AI-generated outputs should be verified against original sources because important details may be omitted or simplified.

### Conclusion

NotebookLM is suitable for limited academic use and supports research, revision and ESG policy analysis, but users should validate outputs against the original documents.
