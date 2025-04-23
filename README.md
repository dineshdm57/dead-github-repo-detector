# Inactive GitHub Repo Detector (OpenOps Workflow)

Detects GitHub repositories with no commit activity in the last 30 days — especially useful for teams tracking projects with linked billing or subscriptions.

---

## What This Workflow Does

This OpenOps workflow:
- Pulls all repositories from a GitHub org/account
- Checks the date of the last commit for each repo
- Flags any repo with **no commits in the last 30 days**
- Sends a Slack alert with the inactive repo's name and last activity

You can easily edit it to change the time threshold or notification method.

---

## Files

- `inactive-github-repo-detector.json` — the actual OpenOps workflow (import this in OpenOps)
- `README.md` — this guide

---

## Why Use This

Most orgs forget to clean up inactive repos, even if:
- They’re linked to paid tools (like CI/CD, backups)
- They consume access/monitoring resources
- They trigger alerts or permissions reviews

This workflow gives you a simple, automated way to detect and take action.

---

## Requirements

- GitHub API access token (for reading repos)
- Slack Webhook or Bot connection (for notifications)
- OpenOps account (to import and run the workflow)

---

## How To Use

1. **Import the JSON** file into OpenOps
2. **Update credentials**:
   - Add your GitHub access token
   - Add your Slack connection and channel/user
3. Run manually or schedule it monthly
4. Customize as needed (change time window, add filters, etc.)

---

## Customization Tips

- Replace Slack with Teams, Email, or Google Sheets
- Add filters for specific repo types or prefixes
- Adjust commit window (e.g., 60 or 90 days)
- Combine with Jira/Monday APIs to correlate active tasks

---

## Can Be Extended To

- Any Git-hosted repo with API access (Bitbucket, GitLab)
- CI/CD pipeline usage tracking
- License or subscription usage matching
