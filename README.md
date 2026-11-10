# Tot op het Bot

**The bones of every AI interview.**

*Tot op het bot* is Dutch for "to the bone": digging into something until you know all of it. And yes, *bot*.

Tot op het Bot is an open-source skeleton for AI interviewers. You give it a schema. It interviews a person until every field is filled, checks each answer, flags gaps and conflicts, shows a summary the person approves, and exports the result. Change the schema and you have a different app.

Built for **Kiroween 2026**, Skeleton Crew category, with [Kiro](https://kiro.dev).

## One skeleton, four apps

| App | Who it interviews | What comes out | Language / input |
|---|---|---|---|
| [`apps/devpost-writer`](apps/devpost-writer) | A hackathon builder (reads their repo and the rules first) | Devpost story + rules checklist | English, text |
| [`apps/finca-report`](apps/finca-report) | A farmer after a day in the field | Dated field report | Spanish, voice |
| [`apps/abuela`](apps/abuela) | A grandparent | A family story or recipe card | Any, voice or text |
| [`apps/tour-onboarding`](apps/tour-onboarding) | A tour operator | A booking-ready tour listing | English / Spanish, text |

## Layout

```
skeleton/     the shared interviewer core (schema -> interview -> validate -> approve -> export)
apps/<name>/  one folder per app: its schema, prompts, skin and sample data
.kiro/        steering, specs and hooks used to build this with Kiro
```

## Status

Work in progress, started November 10, 2026. See `.kiro/specs/` for what is being built.

## License

MIT
