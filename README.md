# Atlassian CLI (acli) Skill

An agent skill that provides a complete reference for the [Atlassian CLI (acli)](https://developer.atlassian.com/cloud/acli/guides/introduction/) — enabling AI agents to help you manage Jira work items, projects, boards, sprints, filters, and more from the command line.

Available on [ClawHub](https://clawhub.ai/peetzweg/atlassian-cli).

## What's Included

```
skill/
├── SKILL.md                                # Core guide: auth, command structure, common patterns
└── references/
    ├── jira-workitem-commands.md            # 23 workitem commands (create, edit, search, transition, ...)
    └── other-commands.md                    # Project, board, sprint, filter, dashboard, field, admin, rovodev
```

Covers **58 commands** across all acli command groups with flags, descriptions, and usage examples.

## Prerequisites

This skill does **not** bundle the `acli` binary. You need to:

1. **Install acli** — follow the [official install guide](https://developer.atlassian.com/cloud/acli/guides/install-acli/)
2. **Authenticate** — via OAuth, API token, or admin API key:
   ```bash
   # Interactive (browser-based)
   acli jira auth login --web

   # API token (non-interactive / CI)
   echo "$API_TOKEN" | acli jira auth login --site "yoursite.atlassian.net" --email "you@example.com" --token
   ```
3. **Verify** — `acli jira auth status`

## Usage

Once installed, just ask your agent to perform Jira operations naturally:

- *"Create a bug in project TEAM about the login timeout"*
- *"Search for all in-progress issues assigned to me"*
- *"Transition KEY-123 to Done"*
- *"List all sprints on board 42"*
- *"Bulk assign these issues to user@company.com"*

The agent will use the skill's reference to construct the right `acli` commands.

## Reference

- [Atlassian CLI official docs](https://developer.atlassian.com/cloud/acli/guides/introduction/)
- [acli command reference](https://developer.atlassian.com/cloud/acli/reference/commands/)
