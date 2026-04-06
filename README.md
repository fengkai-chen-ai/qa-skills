# QA Skills

Claude Code custom slash commands for customer cluster deployment QA.

## Setup

1. Copy the files from `commands/` into `~/.claude/commands/`
2. Add the following to `~/.claude/settings.json`:

```json
{
  "env": {
    "TESTRAIL_URL": "https://appliedintuition.testrail.com",
    "TESTRAIL_USER": "your-email@applied.co",
    "TESTRAIL_API_TOKEN": "your-testrail-api-token"
  }
}
```

3. Restart your Claude Code session

## Available Skills

### `/qa-status`

Interactive QA workflow for customer cluster deployments.

1. Shows a list of all customers from TestRail
2. After selecting a customer, displays the full QA checklist (golden standard test cases)
3. Asks for a release version, then pulls the JIRA changelog for that customer + release

**Requires:** TestRail API access, JIRA MCP (mcp-atlassian)
