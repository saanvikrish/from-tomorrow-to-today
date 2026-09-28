# Website Editor Guide

This guide explains how to update and publish the **From Tomorrow to Today** program website without manually writing HTML.

## Website and Repository

- Public website: https://saanvikrish.github.io/from-tomorrow-to-today/
- GitHub repository: https://github.com/saanvikrish/from-tomorrow-to-today
- Main editable page: `outputs/lan-mobile-agenda.html`
- Published page: `outputs/index.html`
- Images and logos: `outputs/`

The two HTML files must match when a change is published. Codex can handle this automatically.

## What You Need

1. Your own GitHub account.
2. Collaborator access to the GitHub repository.
3. The Codex desktop app installed and signed in.
4. A local copy of the repository on your computer.

Do not ask for or use Saanvi's GitHub password. Saanvi should invite your GitHub account as a repository collaborator.

## First-Time Setup

### 1. Accept the GitHub Invitation

Open the invitation email from GitHub and accept access to `saanvikrish/from-tomorrow-to-today`.

### 2. Download the Project

The simplest visual option is GitHub Desktop:

1. Install GitHub Desktop.
2. Sign in with your GitHub account.
3. Select **File > Clone Repository**.
4. Choose `saanvikrish/from-tomorrow-to-today`.
5. Choose a location on your computer and click **Clone**.

The terminal option is:

```bash
git clone https://github.com/saanvikrish/from-tomorrow-to-today.git
```

### 3. Open the Project in Codex

Open the cloned `from-tomorrow-to-today` folder as a project in Codex. Always work inside this folder so Codex can edit and publish the correct website.

## Before Every Editing Session

Make sure you have the newest version before changing anything.

In GitHub Desktop, click **Fetch origin**, then **Pull origin** if it appears.

Or ask Codex:

> Pull the latest version of the main branch before making changes. Do not overwrite unpublished local work.

Only one person should make major changes at a time. If two people edit the same file simultaneously, GitHub may report a merge conflict.

## The Easiest Editing Workflow

### 1. Give Codex the New Information

Attach the newest agenda PDF, Word document, headshots, or logos directly to the Codex task.

Use a prompt like:

> Update the From Tomorrow to Today website using the attached files. Treat the newest agenda as the source of truth. Do not publish internal notes, invitation statuses, costs, draft prompts, or unconfirmed information. Do not invent missing details. Update the local website first and tell me about any conflicts.

### 2. Review the Local Website

The local preview file is:

`outputs/lan-mobile-agenda.html`

Open it in a browser and check:

- Event date and time
- Session titles, times, and rooms
- Speaker names and titles
- Headshots matched to the correct people
- Biography popups
- Mobile readability
- Sponsor logos and external links

Tell Codex what needs to change in ordinary language. Screenshots are helpful when pointing to a visual issue.

### 3. Publish

When the local version looks correct, tell Codex:

> Sync `outputs/index.html` with `outputs/lan-mobile-agenda.html`, validate all biography and session links, commit the changes, push them to `main`, and confirm the GitHub Pages deployment succeeds.

Codex should:

1. Copy the finished page to `outputs/index.html`.
2. Check the HTML, JavaScript, images, and links.
3. Commit the changes to GitHub.
4. Push to the `main` branch.
5. Wait for GitHub Pages to finish publishing.
6. Confirm the change on the public website.

Publishing normally takes a few minutes.

## Information Needed for Common Updates

### Adding a Speaker

Provide:

- Full name with confirmed spelling
- Professional title and organization
- Session name and role, such as moderator or panelist
- Full biography
- Headshot in JPG or PNG format
- Any confirmed pronunciation, honorific, or credential

Ask Codex to add the person to both the relevant session popup and the **Panelists & Facilitators** timeline.

### Adding or Changing a Session

Provide:

- Session title
- Start and end time
- Room
- Attendee-facing description
- Moderator
- Panelists or facilitators

If documents disagree about a time, room, spelling, or speaker list, Codex should flag the conflict instead of choosing silently.

### Adding a Sponsor

Provide:

- Sponsor name
- High-resolution PNG or JPG logo
- Sponsor website, if the logo should be linked
- Preferred display order

### Replacing a Headshot

Attach the new image and clearly name the person. Ask Codex to replace that person's image everywhere it appears and verify the crop on mobile.

## Important Content Rules

- The website is public. Do not include private phone numbers or email addresses without permission.
- Exclude catering information, costs, outreach notes, invitation statuses, and planning comments.
- Do not publish labels such as `REVISE`, `MISSING`, `PROPOSED COPY`, or embedded AI prompts.
- Do not invent biographies, rooms, titles, or schedule details.
- Preserve supplied meaning when shortening long descriptions.
- Keep names, credentials, titles, and headshots matched carefully.
- Keep both LAN links:
  - Latino Action Network: https://lan.nationbuilder.com/
  - Latino Action Network Foundation: https://www.lanfoundation.org/

## If Something Goes Wrong

### The Public Website Did Not Update

Ask Codex:

> Check the latest GitHub Pages workflow, confirm the push reached `main`, and verify that the public website contains the latest commit.

### A Change Broke the Website

Do not delete files or use `git reset --hard`. Tell Codex:

> Identify the commit that caused the problem, revert that commit safely, push the revert, and confirm the site is working again.

### GitHub Reports a Conflict

Stop editing and ask Codex to inspect the conflict. Do not choose **Accept all** without reviewing what would be removed.

## Final Publishing Checklist

Before approving publication, confirm:

- The schedule is correct.
- Every listed speaker appears in the correct session.
- Every biography opens and closes correctly.
- Every available headshot belongs to the correct person.
- Speakers without supplied photos use initials rather than invented images.
- The mobile layout has no clipped or overlapping text.
- LAN, LAN Foundation, sponsor, and portfolio links work.
- `outputs/index.html` and `outputs/lan-mobile-agenda.html` match.
- GitHub Pages reports a successful deployment.

