# Job Hunt Automation Skill

**Automate your job search with Claude.** This skill finds open positions near you, researches employer contacts, writes tailored application emails, and composes them in Gmail — with you in the loop and in control of everything that gets sent.

---

## What it does

1. **Finds jobs** near your location using web search
2. **Researches each employer** — who to contact, what the place is like
3. **Reads your resume** and extracts the right pitch for each employer
4. **Drafts personalized emails** — not form letters, real emails
5. **Shows you everything** for review before touching Gmail
6. **Composes in Gmail** via the Chrome extension once you say go
7. **Guides you through attaching your resume** (see note below)

**Result:** A batch of tailored, ready-to-send job application emails, done in one session.

---

## Requirements

| Requirement | Notes |
|---|---|
| Claude Cowork (desktop) | For file access, web search, and automation |
| Claude in Chrome extension | For composing emails in Gmail |
| Gmail open in Chrome | Logged into your sending account |
| Your resume file | .docx or .pdf, uploaded to the session |

> **Note on attachments:** Due to sandbox restrictions, Claude cannot push files from its workspace directly into Gmail’s file picker. After Claude composes each email, you’ll attach your resume yourself using Gmail’s paperclip icon. It takes 5 seconds.

---

## Quick start

### Option A: Just talk to Claude

Open Claude Cowork, upload your resume, and say: "Help me find and apply to cook jobs near Salem, OR. I’ve attached my resume."

Claude will ask a few questions (location, job type, commute range) and get to work.

### Option B: Use a config file

Copy `config.example.yaml` to `job-hunt-config.yaml`, fill it in, upload it along with your resume, and say: "Use my config file and resume to run the job hunt skill."

---

## Folder structure

```
job-hunt-skill/
├── SKILL.md                     <- Main skill instructions (Claude reads this)
├── README.md                    <- This file
├── config.example.yaml          <- Sample config - copy and fill in yours
└── prompts/
    ├── resume-polish.md         <- How to extract the right pitch per employer
    ├── employer-research.md     <- How to research and profile each employer
    └── email-generation.md      <- Email drafting principles and template
```

---

## Tips for best results

**Upload your real resume.** The more Claude knows about your actual experience, the more specific and compelling the emails will be. Generic input = generic output.

**Review every email.** Claude will write good drafts, but you know yourself better. If something doesn’t sound like you, change it.

**Don’t mass-blast.** 6–8 well-targeted emails beat 25 generic ones.

**Follow up.** After 5–7 business days with no response, a quick follow-up often makes the difference.

---

## Troubleshooting

| Problem | Solution |
|---|---|
| Claude can’t find employer emails | Claude will suggest phone or walk-in alternatives |
| Gmail compose window keeps closing | Expand to fullscreen before filling fields |
| Resume attachment failing | Attach manually using the paperclip icon — this is expected |
| Job boards blocked (Indeed, Craigslist) | Claude uses search snippets to find job info |
| Email tone feels off | Say "make it more casual" or "make it more professional" |

---

## Privacy note

This skill never sends emails without your explicit per-email approval and does not store your information after the session ends. Your resume and personal data are only shared with the employers you choose.

Built with Claude Cowork + Claude in Chrome.
