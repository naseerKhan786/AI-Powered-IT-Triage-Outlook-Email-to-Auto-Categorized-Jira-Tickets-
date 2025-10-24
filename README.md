# n8n: Outlook -> OpenAI -> Jira (triage and create tickets)

This repository details an n8n workflow designed to automate the initial triage of IT support requests, transforming unstructured emails into fully structured Jira tickets. This solution creates an AI-driven pipeline that connects your support inbox, an advanced language model, and your service management tool.

Files included:
- `0511-outlook-jira-ai-tickets.json` — n8n workflow export (import into n8n Editor UI)
- `README.md` — this file
- `.gitignore` — basic ignores
- `LICENSE` — MIT

Import into n8n Editor:
1. Open your n8n Editor UI.
2. Click the menu → Import from file and paste or upload the `0511-outlook-jira-ai-tickets.json` contents.
3. Review each node and set credentials for:
   - Microsoft Outlook (OAuth2)
   - OpenAI (API key)
   - Jira Software Cloud (API credentials)
4. Configure project IDs and issue types in the "Create Issue" node to match your Jira instance.

Notes:
- The workflow uses a scheduled trigger and will fetch messages received in the last hour. Adjust the schedule or filters as needed.
- The AI model and labels/priorities are configured inside the "Generate Issue From Support Request" node. Update the prompt/messages and output parser schema if you want different labels or priorities.

Security:
- Do NOT commit real API keys or credentials to this repository. Use n8n credentials or environment variables.

License: MIT
