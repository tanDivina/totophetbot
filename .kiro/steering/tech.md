# Tech

- TypeScript (strict), Node 20+, npm workspaces. Packages: `skeleton/` (the core library) and one package per app in `apps/<name>/`.
- Core library has no UI and no framework dependency. Apps are small web apps (Next.js App Router) that import the skeleton.
- Schema format: JSON Schema (draft 2020-12) for the data, plus an `x-interview` extension per field for question hints, examples, language and sensitivity. Validate with Ajv.
- Model access goes through a `ModelProvider` interface. Default provider: Claude on Amazon Bedrock (`us.anthropic.claude-sonnet-4-6`, region us-east-1) via the AWS SDK, using the standard AWS credential chain. A scripted fake provider is used in all tests.
- Model output that changes state is structured (tool use / JSON) and validated before it is applied. Free text from the model is only ever a message to the person.
- Tests: Vitest, plus fast-check property-based tests for the state machine, validator and summary builder.
- Secrets come from environment variables or `.env.local` only. Never write keys, tokens or account ids into code, tests or docs.
- Deploy target: Vercel, one project per app.
