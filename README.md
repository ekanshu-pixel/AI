# MIRA starter kit (Claude Code)

A replica of the MIRA setup Deependra demoed on 1 Oct 2026, adapted for a
Plant / Sales / CFO business. It follows the meeting's decisions: Claude Code (not
chat), Google Sheets dashboards first, data separation through Drive folders.

## What's inside
- CLAUDE.md                  MIRA's identity, rules, and daily-summary format
- ROLES.md                   Who sees what — fill this in first
- .claude/agents/            5 specialists: finance-analyst, sales-analyst, plant-ops,
                             compliance, followup-tracker
- workspace/decisions/       Pending-decisions list
- workspace/followups/       Execution-accountability tracker (pre-filled from the meeting)
- workspace/reports/         Daily summaries land here
- workspace/data-inbox/      Drop CSV/XLSX exports here (manual upload for phase 1)

## Setup (about an hour)
1. Get a Claude plan that includes Claude Code (the meeting suggested the ~$100/month
   tier is enough to start; check current plans at claude.com/pricing).
2. Install Claude Code — see https://code.claude.com/docs
3. Optional but recommended: run it on a small cloud VM (e.g. Google Cloud or AWS) so
   MIRA is reachable from your phone. A laptop is fine for week 1.
4. Unzip this kit, `cd` into it, and run `claude`. It reads CLAUDE.md automatically.
   Type `/agents` to confirm the five specialists are loaded.
5. Fill in ROLES.md. Create one Drive folder + one Google Sheet per role and share each
   only with that role.
6. Connect Google Drive/Sheets/Gmail to Claude Code via MCP connectors (see the MCP
   section of the Claude Code docs). Give MIRA its own Google account if you want it to
   have its own email address, like Deependra's MIRA.

## First prompts to try
- "Read everything in workspace/data-inbox and give me today's executive summary."
- "Here are notes from today's meeting: ... Update the follow-up tracker."
- "What decisions are pending and what's overdue?"
- "Draft the CFO dashboard layout for the CFO Sheet. Don't write to it yet."

## Phase plan
- Week 1: founders only, manual CSV uploads, daily summary in the terminal.
- Week 2-3: role Sheets wired up with IMPORTRANGE; MIRA drafts, you approve updates.
- Week 4: daily summary by email. WhatsApp later — the meeting flagged it as complex.

## Safety
MIRA asks before sending or writing anything (see CLAUDE.md). Keep it that way until
you trust it. Don't use the "Share chat" feature with business data. Keep customer
personal data out of the inbox folder entirely.
