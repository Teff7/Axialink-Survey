# Axialink AI Confidence Survey

A single-page survey that measures staff confidence with AI tools. Respondents answer ten
statements on a 0–100 sliding scale, one question at a time, then download a private
confidence-score report. Anonymous responses are stored in Supabase.

## Scoring

| Category | Questions |
| --- | --- |
| Capability | Q1, Q2, Q3 |
| Trust & Governance | Q4, Q5, Q6 |
| Support & Adoption | Q7, Q8 |
| Future Outlook | Q9, Q10 (Q10 reverse scored) |

Each category score is the average of its questions on a 0–100 scale.

## Deploying on Vercel

This is a static site — no build step.

1. Import this repository in Vercel (Add New → Project).
2. Framework preset: **Other**. Leave build command and output directory empty.
3. Deploy.

## Supabase

Responses are inserted into the `survey_responses` table of the `axialink-ai-survey`
project via the public REST API using the publishable (anon) key. Row-level security is
enabled: anonymous visitors can insert a response but cannot read any data back.
