# trueforge-agent-harness
TrueForge agent that drafts approval-gated emails and analyzes data via sandboxed SQL

## Qodo Code Review Evidence

Qodo reviewed [PR #1](https://github.com/shehreen1/trueforge-agent-harness/pull/1) and found no bugs, rule violations, or requirement gaps.

## How to Run
1. Run TrueForge locally: `npx @truefoundry/trueforge@latest` (opens at localhost:8790)
2. Connect Gmail via Composio in Settings → Connectors, using the fixed URL `https://connect.composio.dev/mcp` with an API Key auth type (header: `x-consumer-api-key`)
3. Configure Daytona as the sandbox provider in Settings → Sandbox providers
4. Open a new chat in TrueForge, enable the Gmail connector, and paste the prompt from `prompts/inbox-triage-agent.txt`
5. Approve the tool calls when prompted — the agent will score emails by urgency, create a Gmail draft, and pause for approval before sending
