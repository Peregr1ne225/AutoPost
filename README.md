# AutoPost — n8n Social Media Automation

An **n8n workflow automation project** for streamlining social media content publishing. The goal is to use n8n to orchestrate the steps involved in preparing content and uploading or publishing it to supported social platforms.

## Overview

AutoPost is designed to centralize repetitive social media posting tasks in an automated workflow. Depending on the configured nodes and platform APIs, a workflow may:

1. Receive or prepare content for a post.
2. Process post text and media.
3. Send content to a supported social platform using its API or an available integration.
4. Handle the publishing result and report success or errors.

The exact behavior and supported platforms depend on the workflow exported to this repository.

## Built With

- **n8n** — workflow automation and orchestration
- **Social platform APIs / integrations** — publish content to the platforms configured in the workflow
- **Optional content sources and storage** — configured according to the workflow

## Repository Structure

The repository is intended to store exported n8n workflow JSON files and related documentation. For example:

```text
AutoPost/
├── README.md
└── workflows/
    └── autopost.json
```

The workflow path above is a suggested structure. Add the exported workflow JSON when it is ready to share or import.

## Import a Workflow into n8n

1. Open your n8n instance.
2. Create a workflow or open the workflow menu.
3. Select **Import from File** (the menu wording may vary by n8n version).
4. Choose the exported workflow `.json` file.
5. Review the nodes and configure the required credentials and settings.
6. Test with a sample post before activating the workflow.

## Configure Social Platform Access

Each platform has its own API, permissions, publishing requirements, and supported media formats. Before running the workflow:

- Create or select the required developer app or platform account.
- Configure the necessary API permissions and access tokens.
- Add credentials securely in n8n.
- Confirm that the account is eligible to publish through the relevant API.
- Check each platform's rules for media types, captions, rate limits, and publishing restrictions.

Only document a platform as supported once its nodes and credentials are configured in the actual workflow.

## Security

- **Never commit access tokens, client secrets, passwords, cookies, or other credentials.**
- Use n8n credentials or a suitable secrets manager for sensitive values.
- Sanitize workflow exports before committing them; remove secrets and sensitive instance-specific data.
- Use placeholders for example configuration values.
- Restrict access to the n8n instance and any webhook endpoints.

## Testing Checklist

- [ ] Add the exported n8n workflow JSON to this repository
- [ ] Import the workflow into n8n
- [ ] Configure required credentials and platform permissions
- [ ] Test text-only publishing, if supported
- [ ] Test media uploads, if supported
- [ ] Verify the published post on the target platform
- [ ] Test error handling and API rate-limit behavior
- [ ] Activate the workflow after successful testing

## Updating the Workflow

After changing the workflow in n8n, export the latest version as JSON, remove any sensitive information, and update the corresponding file in this repository. Keep this README in sync with the actual workflow and the social platforms it supports.

---

**Project status:** Documentation starter. The repository should include the sanitized n8n workflow export for others to import and inspect. Platform-specific setup instructions can be added once the workflow and target platforms are available.
