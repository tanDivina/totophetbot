# Product: Tot op het Bot

An open-source skeleton for AI interviewers, built for Kiroween 2026 (Skeleton Crew category). Deadline: December 4, 2026, 2:00 pm PT.

A schema describes what must be known. The interviewer asks a person questions until every required field is filled, checks each answer, flags gaps and conflicts, shows a summary the person approves, and exports the approved result. Four apps in `apps/` prove the skeleton is reusable: devpost-writer (English, text), finca-report (Spanish, voice), abuela (family stories and recipes), tour-onboarding (tour listing).

The test of the skeleton: adding a new app should mostly mean writing a schema and a small skin, not new engine code.

Principles:
- Never invent an answer. A field is filled only from what the person said or from a source the app was given; otherwise it stays empty and becomes a question.
- Ask a few questions at a time, in the person's language, in plain words.
- The approval summary is built by code from the stored answers, never written freely by the model.
- The person can skip a question, go back, and change an answer.
- Personal data stays in the session; nothing is logged with answer text.

Copy rules: no em dashes in any user-facing text, README or docs. Plain, warm language. No stock icon sets or emoji as UI icons.
