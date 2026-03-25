---
name: job-hunt
description: >
  Automated job hunting skill for Claude Cowork and Claude in Chrome. Given a resume and job preferences,
  this skill searches for open positions, researches employer contacts, polishes the resume pitch for each
  role, drafts a tailored application email, and then walks through Gmail compose via the Chrome extension
  — pausing for human approval before anything is ever sent. Use this skill when the user wants to find
  jobs, apply to jobs, send application emails, search for work, or automate their job search. Also trigger
  when the user says things like "help me find a job", "apply to these places", "send my resume around",
  "I need work", or "draft job emails for me".
---

# Job Hunt Automation Skill

This skill automates the hard, repetitive parts of job hunting — finding openings, researching employers,
writing tailored emails — while keeping you firmly in control of what actually gets sent.

## Setup: What you need

- Your resume uploaded to the conversation
- Gmail open in Chrome with Claude in Chrome connected
- Your location, job type, and commute range

## Workflow

### Phase 1 — Job Discovery
Search for open positions using WebSearch. Try queries like:
- "[job title] hiring near [city, state] [year]"
- "[job title] jobs [city, state] apply"

Find 6-10 candidate employers. For each capture: name, location, job type, source URL.

### Phase 2 — Employer Research
For each employer find: contact email, contact name if possible, type of establishment, what they value.
Search: "[business name] [city] contact email" or "[business name] apply email"
If no email found, note phone number or online application URL instead.
See prompts/employer-research.md for the full profile template.

### Phase 3 — Resume Pitch Polish
Read the user's resume carefully. For each employer identify the 2-3 most relevant experiences.
Match the tone to the employer type. See prompts/resume-polish.md for guidance.

### Phase 4 — Email Drafting
Draft one tailored email per employer. Under 200 words. Real, specific, human-sounding.
See prompts/email-generation.md for the template and principles.

### Phase 5 — HUMAN APPROVAL GATE
STOP. Present all drafted emails to the user clearly showing To, Subject, and Body for each.
Ask: "Please review each email. Say 'send', 'edit [changes]', or 'skip' for each one.
I will not open Gmail until you give me the go-ahead."
Wait for explicit approval before proceeding.

### Phase 6 — Gmail Compose via Chrome
For each approved email, use Claude in Chrome to open Gmail and compose:
1. Navigate to mail.google.com
2. Click Compose button
3. IMMEDIATELY expand to fullscreen before filling any fields
4. Click To field, type email address, press Return
5. Click Subject field directly (do not Tab), type subject
6. Click in body area (y=300), type message paragraph by paragraph
7. Tell user: "Please attach your resume using the paperclip icon, then say 'send it'"
8. Wait for confirmation, then click Send

### Phase 7 — Confirmation
After sending: confirm which emails went out, suggest follow-up timing (5-7 business days).

## Key principles
- Nothing sends without explicit user approval per email
- Emails should sound like the person, not a template
- 6-8 good emails beat 25 generic ones
- File upload from VM to Chrome is not supported — user must attach resume manually
