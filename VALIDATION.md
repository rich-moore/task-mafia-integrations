# Provider validation — 7 November 2026

This is an initial candidate. Checks completed on 7 November 2026:

- Gemini CLI **0.67.0**: `gemini extensions validate` passes.
- The exact candidate installs into an isolated Gemini CLI configuration. The
  real `gemini extensions list` reports version 0.1.0 enabled, the context file,
  Task Mafia MCP server and `task-mafia-tasks` skill.
- Cursor's official `cursor/plugin-template` validator passes. Its only warning
  is the intentionally absent optional hooks file. No hooks are bundled.
- The reviewed public inventory contains only two Cursor manifests, a Gemini
  manifest, MCP configuration, two instruction files, two documentation files
  and the existing public icon. There are no executable hooks, credentials,
  private app source, private task content or environment files.

The Cursor validator script used for this check has SHA-256
`826f55f546ce59500a6e3d7d32a15d90f3373cecc3b41486e75ae28b60647a4a`.

Authenticated Gemini CLI/Cursor operation, Cursor marketplace approval and
Gemini gallery indexing are separate unverified gates. Existing ChatGPT/Claude
protocol evidence is not a substitute for an authenticated test in those hosts.
No model request, production task mutation, OAuth grant or worker schedule was
created by these checks. Gemini CLI state is isolated from the owner's settings.
