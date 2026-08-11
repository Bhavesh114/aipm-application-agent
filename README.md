# aipm-application-agent

An agent harness that submits a job application to aipm.erikrogne.com, which
gates its application behind an agent-only path.

`CLAUDE.md` encodes the site's published protocol: read the instructions first,
use the sanctioned continuation control, no user-agent or webdriver spoofing,
no direct API calls, leave unlabeled fields alone. `content.md` is source
material, not answers — the agent writes the form in its own words and stops
for review before the attestation checkbox.

Built with Claude Code and the Playwright MCP server.