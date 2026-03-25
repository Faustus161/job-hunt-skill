# Employer Research Prompt Template

Use this template when building a profile for each employer before drafting application emails.

---

## Your job here

You're doing two things: (1) finding the practical info needed to send an application (email address,
contact name), and (2) understanding the place well enough to write an email that doesn't sound like
it came from a robot.

The second thing matters as much as the first. An email that says "I'd love to work at your
establishment" sounds like a form letter. An email that says "I've been cooking high-volume grill work
for years and the kind of service your place runs is exactly where I do my best work" gets read.

---

## Research steps

### 1. Find the contact email

Search: "[business name] [city] hiring email" or "[business name] [city] apply"

Also try:
- Their website's "Contact" or "About" page (use WebFetch if not blocked)
- Their Google Maps listing (often has contact info in the description)
- Searching their name + "chef" or "manager" + "email"

If no email is found, note whether they have:
- An online application form (URL if available)
- A phone number (for a call/voicemail script)
- A walk-in recommendation

### 2. Find a name (if possible)

A "Dear [Name]" beats "Dear Hiring Team" every time. Look for:
- Owner name (especially for small/independent restaurants)
- Chef's name (for kitchen roles)
- HR contact (for corporate/institutional employers)

If no name is found, "Hi there" or "Dear Hiring Team" is fine.

### 3. Understand the place

Search: "[business name] [city] reviews" or browse their website / Google Maps listing.

Capture:
- **Type of establishment** -- casual diner, upscale bistro, bar & grill, hospital dietary, fast casual, etc.
- **Approximate size / volume** -- small local place vs. large chain location vs. institutional
- **Menu style** -- relevant for cooks (breakfast all day? wood-fired? scratch kitchen? institutional tray service?)
- **Vibe** -- is this a place where the staff has fun, or is it buttoned-up and professional?
- **Any recent news** -- new location opened? Recent hiring push? Any obvious context?

### 4. Identify what they likely need

Based on the above, what does this employer probably value most in a new hire?
- Speed and volume? They're busy and need someone who won't fall apart in the weeds
- Consistency and cleanliness? Institutional or compliance-heavy (hospitals, schools)
- Quality and creativity? Smaller, focused menus where the food actually matters
- Reliability and loyalty? Small owner-operated place that's been burned by flakes

---

## Output format

Produce one profile block per employer:

```
---
EMPLOYER: [Business Name]
ADDRESS: [City, State]
CONTACT EMAIL: [email@domain.com] -- (source: [how you found it])
CONTACT NAME: [Name if found, else "Not found"]
ESTABLISHMENT TYPE: [e.g., family diner / wine bar / hospital dietary]
APPROXIMATE SIZE: [small/medium/large, any details]
MENU/WORK STYLE: [brief description]
WHAT THEY PROBABLY VALUE: [your read on top 1-2 priorities]
APPLY METHOD: [Email / Online form (URL) / Phone / Walk-in]
NOTES: [anything else worth knowing -- recent opening, seasonal, etc.]
---
```

---

## When you can't find a contact email

Don't give up on an employer just because you can't find a direct email. Note the situation and suggest
the best alternative:

- **Online application form** -- Include the URL and note that the user should apply there
- **Phone only** -- Write a brief phone script (30-45 seconds, name + experience + ask for the manager)
- **Walk-in recommended** -- Some small places actually prefer this -- note it

The goal is to give the user a *complete action item* for every employer on the list, even if the action
isn't sending an email.
