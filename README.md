# evidence-first-complaint

A lightweight Agent Skill for analyzing ordinary consumer disputes from the evidence outward.

> **Evidence before rhetoric.**

The skill helps an AI show the user's viable options immediately, determine what the available record supports, and recommend the smallest useful next step. It analyzes the evidence while concurrently checking applicable regulations and official complaint routes. It is deliberately an analysis skill rather than a generic generator for forceful complaint letters.

## What it covers

Representative uses include:

- refund denials and cancellation penalties
- unexpected, duplicate, subscription, or billing charges
- merchant, e-commerce, hotel, airline, and service disputes
- service failures and conflicting customer-service statements
- requests for a refund, credit, correction, replacement, explanation, or proportionate escalation

## How it works

The workflow first identifies the jurisdiction and presents an option menu with a recommendation, fallback, and conditional escalation. It then separates **facts**, **evidence**, **claims**, and **inferences**, while a parallel track verifies current applicable law and the relevant government consumer body, regulator, ombudsman, or official complaint procedure.

Unlike a generic complaint-writing prompt, it does not automatically advocate, browse broadly, or reach first for legal threats. Regulatory research is mandatory but targeted and based on official sources; case law is checked only when it could resolve a material ambiguity. A complaint is drafted only when requested or clearly appropriate.

## Install

Clone the repository into your agent's skills directory. For Codex:

```bash
git clone https://github.com/stephenlin999/evidence-first-complaint.git ~/.codex/skills/evidence-first-complaint
```

Compatible Agent Skill systems can instead copy the repository folder into their configured skills location. The skill has no runtime, package dependencies, build step, or configuration.

## Use

Ask the agent to analyze a dispute and provide the relevant records where possible:

```text
Use evidence-first-complaint to assess this hotel refund denial.
I want the cancellation fee waived. Here are the booking terms,
the hotel's response, and the transport operator's cancellation notice.
```

On systems that support model-invoked skills, the description in `SKILL.md` also enables automatic activation for matching consumer-dispute requests.

## Small example

If a hotel says transportation remained available, the skill first shows plausible paths such as merchant reconsideration, a booking-platform process, insurance, and any applicable official complaint route. In parallel, it checks the governing rules while treating the denial as a fact supported by the written response, the hotel's transport statement as a claim, and the status of the user's actual route as critical missing evidence.

## Limitations

The assessment is only as reliable as the supplied or verifiable record and the correctly identified jurisdiction. The skill does not authenticate documents, guarantee a remedy, or replace professional legal advice. Laws, policies, and live service conditions require verification from authoritative current sources.

## Repository structure

```text
evidence-first-complaint/
├── SKILL.md
├── README.md
└── LICENSE
```
