# evidence-first-complaint

A lightweight Agent Skill for analyzing ordinary consumer disputes from the evidence outward.

> **Evidence before rhetoric.**

The skill helps an AI determine what the available record supports, what remains only a claim, what weakens the user's position, and which small next step is most likely to advance the requested remedy. It is deliberately an analysis skill rather than a generic generator for forceful complaint letters.

## What it covers

Representative uses include:

- refund denials and cancellation penalties
- unexpected, duplicate, subscription, or billing charges
- merchant, e-commerce, hotel, airline, and service disputes
- service failures and conflicting customer-service statements
- requests for a refund, credit, correction, replacement, explanation, or proportionate escalation

## How it works

The workflow separates **facts**, **evidence**, **claims**, and **inferences** instead of treating the user's account as established fact. It builds a short chronology, tests disputed claims against direct evidence, surfaces contradictions and weaknesses, and rates the current position as Strong, Moderate, Weak, or Insufficient evidence.

Unlike a generic complaint-writing prompt, it does not automatically advocate, browse broadly, or reach first for legal threats. It seeks only evidence that could change the assessment and recommends the minimum useful next action. A complaint is drafted only when requested or clearly appropriate.

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

If a hotel says transportation remained available, the skill treats the denial as a fact supported by the written response, the hotel's transport statement as a claim, and the status of the user's actual route as critical missing evidence. It may rate the position as Insufficient evidence and recommend obtaining one official route-status record before escalating.

## Limitations

The assessment is only as reliable as the supplied or verifiable record. The skill does not authenticate documents, guarantee a remedy, or replace professional legal advice. Laws, policies, and live service conditions may require targeted verification from an authoritative current source.

## Repository structure

```text
evidence-first-complaint/
├── SKILL.md
├── README.md
└── LICENSE
```
