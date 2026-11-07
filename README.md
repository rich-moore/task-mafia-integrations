# Task Mafia integrations

Connect your own Task Mafia account to compatible developer tools. Read selected
lists, capture tasks and shopping items, and propose changes for human review.

This public repository contains integration manifests, instructions and the Task
Mafia icon. The application source, account data and credentials are separate.
Copyright Richard Moore. Task Mafia's service and trademarks remain proprietary.

## Release status

Version 0.1.0 is the initial provider candidate. Local validation and installation
results are recorded in [VALIDATION.md](VALIDATION.md). An installable repository
does not establish marketplace approval, gallery indexing or an authenticated
receiving-host test. Google Connected Apps preview is a separate application.

## Requirements and access

Create or use an account at https://taskmafia.com. Authorize the existing HTTPS
MCP endpoint through the host's OAuth flow and choose the lists/capabilities that
connection may access. Revoke it in Task Mafia's account controls when needed.
Keep host confirmation settings enabled. No API key, token or password belongs
in these files. Task Mafia is free to start, with optional Crew account limits;
the integration has no checkout and supplies no AI credits or model.

## Gemini CLI

Install from the public repository:

```sh
gemini extensions install https://github.com/rich-moore/task-mafia-integrations
```

Restart Gemini CLI. Inspect `/extensions list`, then authenticate the Task Mafia
connection with `/mcp auth task-mafia`. Choose only the lists you want to use.
The extension declares 15 interactive task/list tools and leaves confirmations
under host control. It creates no scheduler or agent-worker configuration.

## Cursor

The repository includes a Cursor plugin manifest, a task/list skill and the
existing remote MCP endpoint. Once the marketplace listing is approved, install
Task Mafia through Customize. Until then, follow Cursor's documented local
plugin workflow or add `https://taskmafia.com/mcp` as a custom remote MCP server
in Customize. Authenticate with OAuth and select the intended lists.

The general-purpose server may expose additional consent-controlled tools. This
plugin's instructions do not configure those advanced workflows or prove that
an unattended agent is running. No hook, shell command, credential or scheduler
is bundled.

## Try it

- “Which Task Mafia lists can this connection access?”
- “Add coffee beans to my selected shopping list, without a date.”
- “Suggest moving this task to my selected Weekend plans list.”

New captures appear immediately. Existing-task edits, moves and list changes
remain subject to human review. Adding a new list does not automatically grant
this connection access. The integration cannot invite people, purchase items,
expand its own permissions or approve its own work.

## Support and policies

- Website: https://taskmafia.com
- Setup: https://taskmafia.com/agents
- Support: https://taskmafia.com/support or hello@taskmafia.com
- Privacy: https://taskmafia.com/privacy
- Terms: https://taskmafia.com/terms

Report security concerns privately through the support address. Never include
credentials, private tasks, transcripts, account exports or sensitive logs in a
public issue.
