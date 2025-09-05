# Update Contacts In Notion

n8n workflow that automatically adds and updates CRM contacts in a Notion database, keeping your team's contact directory always in sync.

## Features

- Auto-create Notion pages for new contacts
- Update existing entries when contact info changes
- Sync from multiple CRM sources (Close, HubSpot)
- Deduplicate contacts by email
- Tag contacts by source and status

## Setup

1. Import the workflow JSON into n8n
2. Create a Notion integration at notion.so/my-integrations
3. Share your Notion database with the integration
4. Configure the following credentials in n8n:
   - Notion API key
   - CRM API key (Close or HubSpot)

## Notion Database Schema

| Property | Type | Description |
|----------|------|-------------|
| Name | Title | Contact full name |
| Email | Email | Primary email |
| Company | Text | Company name |
| Title | Text | Job title |
| Source | Select | CRM source |
| Status | Select | Active/Inactive |
| Last Synced | Date | Last sync timestamp |
| Notes | Text | Additional notes |

## Schedule

Default: Runs every 6 hours. Configurable via n8n cron settings.
