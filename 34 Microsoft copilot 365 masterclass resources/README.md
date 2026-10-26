# Pashun Sports T-Shirts — Demo Environment Setup

**Lesson 4: "Meet Pashun Sports — The Real Business You Will Use for Every Demo in This Course"**

This README walks you through seeding a Microsoft 365 tenant with the Pashun Sports T-Shirts demo environment, using the files in this bundle. Follow the steps **in order** — several later steps depend on things created earlier (the SharePoint list needs the team site to exist; the Planner task references the fabric order from the Outlook thread; and so on).

This environment is used across the whole course, not just Lesson 4 — the Word, Excel, PowerPoint, Teams, agent and governance lessons later in the course all demo against these same files, people and figures.

## How this bundle is organised

Resource files are grouped into one folder per lecture (e.g. `Lecture 24`, `Lecture 54`) — open the folder for the lecture you're working on and its README tells you what's inside and how to use it.

A file used by more than one lecture lives once in the top-level **Shared Resources** folder instead of being copied into every lecture folder. When a lecture needs one of these, that lecture's own README says so and points you to Shared Resources — you won't need to go hunting for it. The Shared Resources folder holds the Pashun Sports demo environment files (Outlook threads, the sales forecast workbook, the launch pitch deck, the fabric specification, the customer-facing policy documents, and so on) plus the wholesale price list used across the Agents lectures.

## Course lecture map

| Section | Lectures | Resource folders |
|---|---|---|
| 1. Introduction | 1–5 | none |
| 2. Understanding Microsoft 365 Copilot | 6–11 | none |
| 3. Prompting | 12–17 | none |
| 4. Copilot in Outlook | 18–23 | none |
| 5. Copilot in Word | 24–30 | `Lecture 24`–`Lecture 30` (Shared Resources) |
| 6. Copilot in Excel | 31–37 | `Lecture 31`–`Lecture 37` (Shared Resources) |
| 7. Copilot in PowerPoint | 38–42 | `Lecture 38`–`Lecture 42` |
| 8. Copilot in Teams and Meetings | 43, 44, 48 | `Lecture 43`, `Lecture 44`, `Lecture 48` |
| 10. Copilot Agents — Your AI Teammates | 54–60 | `Lecture 54`–`Lecture 60` |
| 11. Security, Governance and Responsible Use | 61–64 | none |

## ⚠️ Before you start: read this about the SharePoint list

**Step 3 below must be done on the Teams "Pashun Sports T-Shirts" team's own site — not in your personal OneDrive.**

This trips people up because both places let you create a list, and a list created in personal OneDrive *looks* fine at first glance. The problem shows up later: several lessons in this course rely on grounding and permissions coming from content living in a **Team's shared document library / site**, not an individual's personal storage. If the list — or any of the Word/Excel/PowerPoint files below — lives in OneDrive instead:

- Other course demos that reference "the Pashun Pro Tee supplier list on the team site" won't find it.
- Permission and sharing lessons (which assume Team-level access) will behave unpredictably, because personal OneDrive items are only shared with whoever you've explicitly shared them with.
- The Production channel's own Files tab will appear empty, because nothing was actually saved into the Team's document library.

If you're ever unsure whether something landed in the right place, check the Team's own **Files** tab for that channel — if it's not visible there, it's not on the team site.

## Setup checklist (do these in order)

### 1. Create the Teams team
- Create a new **Standard, Private** team named **"Pashun Sports T-Shirts"**.
- Add **Paul Ashun** (Founder & Director) as owner.
- Add **Jamie Jordan** (Project Manager) and **Morgan Reyes** (Head of Finance) as members — both real, licensed directory users, so Copilot can recognise them as people.

### 2. Create the Production channel
- Inside the team, create a channel named **"Production"**.
- Post the channel message and reply from `Teams-Seed-Script.docx`, using the dates shown.
- Seed the 1:1 chat history between Paul and Jamie Jordan from the same file.

### 3. Create the SharePoint list — on the team site
- From the **Pashun Sports T-Shirts team site** (not OneDrive), create a new list named **"Pashun Pro Tee - US Supplier Contacts"**.
- Import `Pashun Pro Tee - US Supplier Contacts.csv` (Create list → From CSV/Excel), giving you three supplier rows: Ridgeline Apparel Supply, Summit Trim & Labels Co., and Harbor Freight Logistics.

### 4. Create the Planner plan
- Create a new Planner plan named **"Pashun Pro Tee - US Launch"**, associated with the Pashun Sports T-Shirts team.
- Add the buckets and tasks from `Pashun Pro Tee - US Launch Plan.xlsx`, including the task **"Confirm Ridgeline Apparel Supply fabric order for US range"** assigned to **Jamie Jordan**, due 23 Jan 2026, and the Finance tasks assigned to **Morgan Reyes**.

### 5. Seed the two Outlook threads
- Using `Outlook-Seed-Threads.docx`, recreate the two threads in Outlook:
  - **Fabric Quote** (Paul ↔ Jamie Jordan, re: Ridgeline Apparel Supply) — 14 messages, 12 Jan–23 Jan 2026.
  - **US Sales & Invoice** (Paul ↔ Morgan Reyes), 2–9 Feb 2026.
- Send/reply using the dates and subject lines given so the thread displays correctly.
- Do **not** create a directory account for Ridgeline Apparel Supply — it's used as a typed Outlook contact only, which is what makes it useful later for teaching the difference between a real directory "person" and a manually-typed contact.

### 6. Create the two recurring meetings
- Import `Weekly-Production-Catch-Up.ics` (Mondays 09:30–10:00, Paul + Jamie Jordan).
- Import `Monthly-US-Sales-Review.ics` (first Thursday of the month, 15:00–16:00 UK, Paul + Morgan Reyes).

### 7. Upload the Word/Excel/PowerPoint files to the team site
Upload the following into the **Pashun Sports T-Shirts** team's document library (e.g. the Production channel's Files tab), so they sit alongside the SharePoint list from Step 3:
- `Pashun Pro Tee - US Range Brief.docx`
- `Pashun Sports - US Sales and Stock Forecast.xlsx` — four tabs: **US Forecast** (per state/size/colourway), **Sales Summary** (per-state actuals, region and stock cover — also the Region lookup source), **Quarterly Forecast** (the same annual total phased by quarter), and **KPI Summary** (headline rollups). All convert cleanly to named Excel Tables (`USForecast`, `SalesSummary`) with Ctrl+T.
- `Pashun_Pro_Tee_Pitch.pptx`
- `Ridgeline Apparel Supply - Pro Tee Fabric Specification.docx` — a long, technical supplier document (materials, test standards, tolerances, commercial terms) used later for practising document summarisation on something nobody wants to read in full.
- `Pashun Sports - US Returns and Exchanges Policy.docx`, `Pashun Pro Tee - US Sizing and Fabric FAQ.docx`, `Pashun Sports - US Delivery Timescales.docx` — the three grounding documents for the customer service agent built later in the course. Keep these three final, dated and free of internal notes, since anything in them is something an agent may repeat to a customer.
- `Pashun Pro Tee - US Wholesale Price List.xlsx` — **added for Section 10.** Wholesale price, RRP, MOQ and case pack by SKU/size/colourway, plus a Terms tab. This is internal pricing, not customer-facing — never ground a customer-facing agent (e.g. the Section 10 Customer Service Agent) on this file, and never let an agent quote a wholesale figure to a customer.

### 8. Create the OneNote notebook
- Create (or open) a OneNote notebook for the team.
- Add a page named **"Pashun Pro Tee - US Launch Checklist"** using the content in `Pashun Pro Tee - US Launch Checklist.docx` (Insert → Files as Printout, or copy/paste the checklist items).

### 9. Keep the data-cleanup practice file separate
`Pashun Sports - US Sales and Stock Forecast (Before Cleanup - Practice Copy).xlsx` is a deliberately messy sample (merged title row, a blank spacer row, text stored where numbers belong, a stray total row inside the data) for practising the "clean your data before you ask Copilot to work with it" lesson. Keep it in a **Practice** subfolder rather than the main document library — it's meant to be fixed as an exercise, not mistaken for the real, already-clean workbook from Step 7.

## Once complete

You should have: a Teams team with a Production channel (post + chat history), a SharePoint list on the team site with three supplier rows, a Planner plan with tasks split between Jamie Jordan (Sourcing/Production) and Morgan Reyes (Finance), a 14-message Outlook thread plus a shorter invoice thread, two recurring meetings, seven files in the team's document library (three from the original launch, four supporting later lessons), a data-cleanup practice file kept separately, and a OneNote checklist page.

Every artefact in this bundle uses the same people, dates and figures — Paul Ashun, Jamie Jordan, Morgan Reyes, Ridgeline Apparel Supply, invoice PSP-INV-1042, $9.00 wholesale / $19.99 RRP, 2,500-unit first order, 22,000-unit 2026 forecast — so anything you demo against one artefact will line up with the others.

---

# Section 7: Copilot in PowerPoint — Presentations in Minutes

**Lectures 38–42: "Copilot in PowerPoint" — How to Create, Brand, Edit, Rehearse and Interrogate Decks With the Pashun Pro Tee Story**

This section covers the additional resources for Section 7. It does **not** change anything in Steps 1–9 above — those remain the full setup for the Section 4 demo environment. Section 7 reuses several of those same Shared Resources files rather than duplicating them, so make sure Steps 1–9 have already been completed before working through this section.

## What's new in this bundle

| File | Used in |
|------|---------|
| `Deck-Generation-Prompt-Card.docx` | Lecture 38 |
| `Heading-Structure-Checklist.docx` | Lecture 38 |
| `Ridgeline_Apparel_Supply_-_Pro_Tee_Fabric_Specification.pdf` | Lecture 38 |
| `Scanned-Fabric-Spec-Sample.pdf` | Lecture 38 |
| `Pashun_Sports_-_Brand_Template.potx` | Lecture 39 |
| `Brand-Safe-Deck-Prompt-Card.docx` | Lecture 39 |
| `Slide-Master-Setup-Checklist.docx` | Lecture 39 |
| `Slide-Editing-Prompt-Card.docx` | Lecture 40 |
| `Speaker-Notes-Prompt-Set.docx` | Lecture 41 |
| `Speaker-Coach-Rehearsal-Checklist.docx` | Lecture 41 |
| `Ridgeline_Apparel_Supply_-_Pashun_Pro_Tee_Capability_Deck.pptx` | Lecture 42 |
| `Received-Deck-Interrogation-Prompt-Card.docx` | Lecture 42 |

## Setup checklist — Section 7

### 10. Set up the "Create presentation from file" sources (Lecture 15 / slide 38)
- No new upload needed for the prompt-only method (Method A) — it's run from a blank deck.
- For Method B, use the already-uploaded `Pashun Pro Tee - US Range Brief.docx` and `Pashun_Pro_Tee_Pitch.pptx` from the team site (Step 7 above) as the "Create presentation from file" sources. Don't recreate them.
- For Method C, upload the new **text-layer PDF**, `Ridgeline_Apparel_Supply_-_Pro_Tee_Fabric_Specification.pdf`, to the team site alongside `Ridgeline Apparel Supply - Pro Tee Fabric Specification.docx`. This PDF is a genuine export of that same content with a real, selectable text layer, so "Create presentation from file" can read it properly.
- Also keep `Scanned-Fabric-Spec-Sample.pdf` on hand as the deliberate failure case — it's a page rendered purely as an image, with no underlying text, so Copilot cannot extract anything from it. You can use this file as-is, or substitute any genuinely scanned/photographed PDF you have to hand — the exact content doesn't matter for this demo point, only that it has no text layer.
- Use `Deck-Generation-Prompt-Card.docx` and `Heading-Structure-Checklist.docx` as your own reference while running the demo; they don't need to be uploaded anywhere for Copilot to use.

### 11. Upload and apply the brand template (Lecture 16 / slide 39)
- Upload `Pashun_Sports_-_Brand_Template.potx` to the **Pashun Sports T-Shirts** team's document library (the same location as the Section 4 files), so the whole team starts new decks from it.
- The template already has its five named layouts in place — **Pashun Title, Pashun Section Header, Pashun Two Content, Pashun Data, Pashun Product Shot** — plus the Montserrat/Open Sans font pairing and the red/charcoal/off-white palette set at the theme level, so you can demo starting a new deck from it without further setup.
- Use `Brand-Safe-Deck-Prompt-Card.docx` and `Slide-Master-Setup-Checklist.docx` as your own reference material for the demo and for building or reviewing the template itself.

### 12. Prepare for the slide-editing demo (Lecture 17 / slide 40)
- No new files to upload — this lecture reuses `Pashun_Pro_Tee_Pitch.pptx`, `Pashun Pro Tee - US Range Brief.docx` and `Pashun Sports - US Sales and Stock Forecast.xlsx`, all already on the team site from Step 7.
- Keep `Slide-Editing-Prompt-Card.docx` on hand as your prompt reference.

### 13. Prepare for the speaker notes and rehearsal demo (Lecture 18 / slide 41)
- No new files to upload — reuses `Pashun_Pro_Tee_Pitch.pptx` and `Pashun Sports - US Sales and Stock Forecast.xlsx`.
- Use `Speaker-Notes-Prompt-Set.docx` for the prompt sequence and `Speaker-Coach-Rehearsal-Checklist.docx` when running Speaker Coach.

### 14. Set up the "received deck" for the summarisation demo (Lecture 19 / slide 42)
- Upload `Ridgeline_Apparel_Supply_-_Pashun_Pro_Tee_Capability_Deck.pptx` to a **Received** (or similarly named) folder in the team's document library — **not** the main Pashun Sports document library used for files Pashun Sports itself produced. This deck represents something Ridgeline Apparel Supply sent *to* Pashun Sports, so it should look and feel like an inbound file, not an internal one.
- This is a real 22-slide deck covering Ridgeline's facility, fabric capability, pricing, MOQs, lead times, delivery dates and commercial terms. Slide 16 ("Indicative Margin Analysis") deliberately has its figures pasted in as a picture rather than as real text or a table — that's what makes the "Copilot can't read a screenshot" failure case work when you run the gap-analysis prompt.
- Use `Received-Deck-Interrogation-Prompt-Card.docx` for the four-prompt sequence (orientation summary, price/MOQ/lead-time extraction table, cautious-buyer RTCA read, and gap analysis).

## Once complete (Section 7)

You should have: the text-layer and scanned-sample PDFs of the Ridgeline fabric spec uploaded alongside the existing Section 4 files, `Pashun Sports - Brand Template.potx` saved to the team site with its five named layouts and brand fonts/colours in place, and the 22-slide Ridgeline capability deck sitting in a **Received** folder distinct from the team's own document library — plus eight new prompt cards and checklists for you to work from during each demo.

Every new artefact in this section stays consistent with the same people, dates and figures used throughout the course — Paul Ashun, Jamie Jordan, Morgan Reyes, Ridgeline Apparel Supply (Dana Whitfield), the $9.00 wholesale / $19.99 RRP Pashun Pro Tee, the 2,500-unit first order and the 22,000-unit 2026 forecast — so anything you demo in Section 7 lines up with everything built for Section 4.

---

# Section 8: Copilot in Teams and Meetings

**Lectures 43, 44, 48: "Copilot in Teams and Meetings" — Setting Up Transcription, Getting Help During and After a Meeting, and Turning Actions Into Follow-Ups**

This section covers the additional resources for Section 8. It does **not** change anything in Steps 1–14 above. Section 8 reuses the same people, meetings and Shared Resources files already set up for Section 4 rather than duplicating them, so make sure those steps have already been completed.

## What's new in this bundle

| File | Used in |
|------|---------|
| `Meeting-Options-and-Transcription-Setup-Checklist.docx` | Lecture 43 |
| `Recording-Consent-Wording-Card.docx` | Lecture 43 |
| `Live-Meeting-Prompt-Card.docx` | Lecture 44 (Part 1 — live) |
| `Meeting-Recap-Prompt-Set.docx` | Lecture 44 (Part 2 — after the meeting) |
| `Teams-Catch-Up-Prompt-Card.docx` | Lecture 44 (Part 3 — chats and channels) |
| `Meeting-Action-Conversion-Prompt-Set.docx` | Lecture 48 |
| `Action-to-Destination-Routing-Card.docx` | Lecture 48 |

## Setup checklist — Section 8

### 15. Confirm transcription and recording are switched on (Lecture 43)
- No new file to upload. In the Teams admin centre, confirm **Allow transcription** and **Allow cloud recording** are on before anything else in this section will work.
- On the recurring **Weekly Production Catch-Up** (already scheduled from `Weekly-Production-Catch-Up.ics`), open Meeting options and set Copilot to **During and after the meeting**, with **Record and transcribe automatically** ticked.
- Use `Meeting-Options-and-Transcription-Setup-Checklist.docx` to confirm every step, and `Recording-Consent-Wording-Card.docx` for the line to say out loud when starting transcription live or on a supplier call.

### 16. Prepare the live-meeting demo (Lecture 44, Part 1)
- No new files to upload — this reuses the Weekly Production Catch-Up meeting and `Pashun Sports - US Sales and Stock Forecast.xlsx`, already on the team site.
- Use `Live-Meeting-Prompt-Card.docx` for the in-meeting prompt sequence (fact-checking, grounding in a file, checking what's open, checking your own exposure, and pasting a decision into the meeting chat).

### 17. Prepare the after-the-meeting demo (Lecture 44, Part 2)
- No new files to upload — run this against a Weekly Production Catch-Up or Monthly US Sales Review (`Monthly-US-Sales-Review.ics`) that has already been recorded and transcribed.
- Use `Meeting-Recap-Prompt-Set.docx` for the decision and action-item extraction prompts, including the quoted-sentence and confidence-flag techniques.

### 18. Prepare the busy chats and channels demo (Lecture 44, Part 3)
- No new files to upload — this uses the Production channel and the Paul–Jamie 1:1 chat in the **Pashun Sports T-Shirts** team, and a Planner task from `Pashun Pro Tee - US Launch Plan.xlsx` created outside the chat (to demonstrate the honest limitation).
- Use `Teams-Catch-Up-Prompt-Card.docx` for the time-scoping comparison and the "find your own actions" prompt.

### 19. Prepare the action-conversion demo (Lecture 48)
- No new files to upload — this picks up directly from the action list already extracted in Lecture 44 (Part 2), so there's no need to re-run that extraction.
- Use `Meeting-Action-Conversion-Prompt-Set.docx` for the task-title rewrite, supplier email, chat nudge, decision record and catch-up email prompts, and `Action-to-Destination-Routing-Card.docx` to decide which of the three destinations each action belongs to before typing anything.

## Once complete (Section 8)

You should have: transcription and recording confirmed on in the admin centre and set as the default on the Weekly Production Catch-Up, plus seven new prompt cards and checklists covering setup, live and after-the-fact meeting help, busy chat/channel summaries, and converting actions into tasks, emails and follow-ups. No new demo files were needed for Section 8 — it runs entirely on the meetings, chats and files already set up in Sections 4 and earlier in Section 8 itself.

Every new artefact in this section stays consistent with the same people and scenario used throughout the course — Paul Ashun, Jamie Jordan, Morgan Reyes, Ridgeline Apparel Supply, and the Pashun Pro Tee US launch — so anything you demo in Section 8 lines up with everything built earlier in the course.

---

# Section 10: Copilot Agents — Your AI Teammates

**Lectures 54–60: "Building Agents with Microsoft 365 Copilot" — When to Build One, the Ready-Made Agents, Building Your First No-Code Agent, Grounding, a Customer Service Agent, a Sales Reporting Agent, and the Share/Test/Monitor/Improve Lifecycle**

This section covers the additional resources for Section 10. It does **not** change anything in Steps 1–19 above, except that Step 7 (uploading files to the team site) now also includes `Pashun Pro Tee - US Wholesale Price List.xlsx`, a grounding file this section introduces (see the updated Step 7 note above). Section 10 otherwise reuses the same people, files and figures already set up for Section 4 rather than duplicating them, so make sure Steps 1–9 have already been completed.

## What's new in this bundle

| File | Used in |
|------|---------|
| `Agent-vs-Prompt-Decision-Worksheet.docx` | Lecture 54 |
| `Built-In-Agents-Reference-Card.docx` | Lecture 55 |
| `Researcher-Analyst-Starter-Prompts.docx` | Lecture 55 |
| `Agent-Instruction-Template.docx` | Lecture 56 |
| `Pashun Pro Tee - US Wholesale Price List.xlsx` | Lectures 54, 57, 58 (grounding file — also uploaded to the team site in Step 7) |
| `Agent-Grounding-Checklist.docx` | Lecture 57 |
| `Customer-Service-Agent-Build-Sheet.docx` | Lecture 58 |
| `Sales-Reporting-Agent-Instruction-Template.docx` | Lecture 59 |
| `Agent-Test-Set-and-Monitoring-Log.docx` | Lecture 60 |

## Setup checklist — Section 10

### 20. Upload the wholesale price list (Lecture 54 / 57 / 58)
- Upload `Pashun Pro Tee - US Wholesale Price List.xlsx` to the **Pashun Sports T-Shirts** team's document library, alongside the Section 4 files.
- This is internal pricing — never ground a customer-facing agent on it, and never let any agent quote a wholesale figure to a customer. Use `Agent-vs-Prompt-Decision-Worksheet.docx` to score your own repeated tasks against the three-question test, using the four worked Pashun Sports examples as a guide.

### 21. Try the ready-made agents (Lecture 55)
- No new file to upload — Researcher and Analyst ship with the Copilot licence.
- Use `Built-In-Agents-Reference-Card.docx` to see the full list of built-in agents and where to find each one, and `Researcher-Analyst-Starter-Prompts.docx` for the exact Pashun Pro Tee prompts used in the demo (US market sizing with Researcher; margin-per-unit with Analyst against `Pashun Sports - US Sales and Stock Forecast.xlsx`).

### 22. Build your first no-code agent (Lecture 56)
- No new file to upload — this reuses `Pashun Sports - US Returns and Exchanges Policy.docx` as the sole grounding file for the practice returns-assistant build.
- Use `Agent-Instruction-Template.docx` to draft the Role/Tone/Rules/Escalation instruction blocks before opening the agent builder.

### 23. Ground an agent properly (Lecture 57)
- Add `Pashun Pro Tee - US Range Brief.docx`, `Pashun Pro Tee - US Wholesale Price List.xlsx` and `Pashun Sports - US Returns and Exchanges Policy.docx` as knowledge sources on a new or existing agent — this is the sample knowledge set used in the demo.
- Use `Agent-Grounding-Checklist.docx` to scope the sources narrowly, write the anti-hallucination instruction, and run the three test questions (product spec, supplier lookup, deliberate failure).

### 24. Build the customer service agent (Lecture 58)
- Ground the agent on `Pashun Sports - US Returns and Exchanges Policy.docx`, `Pashun Pro Tee - US Sizing and Fabric FAQ.docx` and `Pashun Sports - US Delivery Timescales.docx` — all already on the team site from Step 7. Turn web search off.
- Use `Customer-Service-Agent-Build-Sheet.docx` for the full instruction text, the four starter prompts, and the happy-path/out-of-scope test questions (the out-of-scope one deliberately asks for the wholesale price, which the agent must decline).

### 25. Build the sales reporting agent (Lecture 59)
- Ground the agent on `Pashun Sports - US Sales and Stock Forecast.xlsx` and the Production channel's files — check the workbook headers are clean first (no merged title row, one row per record).
- Use `Sales-Reporting-Agent-Instruction-Template.docx` for the full instruction text, starter prompts, and the known-answer / deliberate-failure test questions.

### 26. Share, test, monitor and improve (Lecture 60)
- No new file to upload — this lecture works on whichever agent you built in Lectures 56–59.
- Use `Agent-Test-Set-and-Monitoring-Log.docx` to run the four-part test set (happy path, edge case, out of scope, hallucination bait), log your own eight-prompt test set, and set up the weekly/monthly maintenance cadence with a version note log.

## Once complete (Section 10)

You should have: the wholesale price list uploaded to the team site as a new grounding file, and nine new resources covering the build-vs-prompt decision, the built-in agents and their starter prompts, a no-code agent instruction template, a full grounding checklist and sample knowledge set, build sheets for a customer service agent and a sales reporting agent, and a test-set/monitoring log for keeping an agent healthy after launch.

Every new artefact in this section stays consistent with the same people, files and figures used throughout the course — Paul Ashun, Jamie Jordan, Morgan Reyes, Ridgeline Apparel Supply, and the Pashun Pro Tee US launch — so anything you demo in Section 10 lines up with everything built earlier in the course.
