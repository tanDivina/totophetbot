# Tasks

- [ ] 1. Set up the npm workspace (root package.json, `skeleton/` package, TypeScript strict, Vitest, fast-check). Write `design.md` in this folder: module boundaries, the session state type, the ModelProvider interface, and the extractor's structured output format.
- [ ] 2. Schema loading and `x-interview` validation (req 1), with tests.
- [ ] 3. Session state machine, skip / reopen / change, serialize and resume (req 2), with property-based tests.
- [ ] 4. Planner (req 3) and extractor with the fake provider (req 4), with tests including conflict and vague-answer cases.
- [ ] 5. Code-built summary with content hash, approval, JSON and Markdown export (req 5), with property-based tests.
- [ ] 6. Bedrock provider behind the interface; a small CLI (`npx totophetbot interview <schema.json>`) to run any schema in the terminal. Smoke-test it against `apps/tour-onboarding/schema.json` once that exists.
- [ ] 7. Add Kiro agent hooks: run the tests on save in `skeleton/src`, and validate every `apps/*/schema.json` when it is saved.
