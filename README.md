# Superlog plugin for Claude Code

Manage your [Superlog](https://superlog.sh) workspace from Claude Code. Ask Claude to create an automation, start a run, check why a run failed, change tag mode, or connect an integration.

The plugin connects Claude Code to the Superlog MCP server at `https://superlog.sh/api/mcp`. You sign in with your Superlog account the first time you use it.

## Install

```bash
claude plugin marketplace add superloglabs/claude-plugin
claude plugin install superlog@superlog
```

Inside a session, the same commands work as `/plugin marketplace add superloglabs/claude-plugin` and `/plugin install superlog@superlog`.

## Sign in

1. Start Claude Code and run `/mcp`.
2. Select `plugin:superlog:superlog` and choose **Authenticate**.
3. Sign in to Superlog in your browser, choose a workspace, and approve access.

Claude acts as you in the workspace you chose. To switch workspaces, choose **Clear authentication** in `/mcp` and sign in again.

## Example requests

- "Create an automation that reviews new Sentry regressions in the `api` project and opens a pull request in `acme/api`."
- "Connect GitHub to my Superlog workspace."
- "Why did the last run of the triage automation fail?"
- "Let tag mode read the `acme/web` repository."

Workspace secrets and model API keys are not available as tools, so their values never pass through the model. Add them in the Superlog app.

## Documentation

- [Use Superlog in Claude](https://docs.superlog.sh/assistants/claude)
- [MCP server reference](https://docs.superlog.sh/api-reference/mcp)

## Support

Email [support@superlog.sh](mailto:support@superlog.sh). See the [privacy policy](https://superlog.sh/privacy) and [terms](https://superlog.sh/terms).
