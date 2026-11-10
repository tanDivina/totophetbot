# Structure

```
skeleton/                 core library (@totophetbot/skeleton)
  src/schema/             schema loading, x-interview extension, Ajv validation
  src/session/            interview state machine, save/resume
  src/planner/            picks the next questions
  src/extract/            turns a reply into proposed field values (model, structured)
  src/summary/            code-built approval summary + content hash
  src/export/             JSON and Markdown exporters
  src/providers/          ModelProvider interface, Bedrock provider, fake provider
  test/
apps/<name>/              one app each: schema.json, prompts, skin, sample sessions, README
.kiro/steering/           these files
.kiro/specs/              one folder per feature (requirements, design, tasks)
.kiro/hooks/              agent hooks
```

Naming: kebab-case files, PascalCase types, camelCase functions. Each app's schema lives at `apps/<name>/schema.json`.
