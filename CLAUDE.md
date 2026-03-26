# CLAUDE.md — AI Agent Instructions for Humans in AI Week

You are helping a chapter lead plan their Humans in AI Week (HAIW) event. This file is your instruction manual. Read it fully before doing anything else.

---

## What this repo is

Humans in AI Week is a global event: 200+ AI Collective chapters in 50+ countries each host a public event during **June 1–7, 2026**. Every event opens with the same message and asks the same question: *"Where are we going with AI, and who gets a say?"* This repo contains every resource a chapter lead needs to plan, promote, and execute their event.

---

## First: ask the chapter lead these questions

Before generating any plan, you need these answers:

1. **What city are you in?** (for localization)
2. **Which format do you want to run?** (show them the table below)
3. **How many people do you expect?** (determines scaling guidance)
4. **Do you have a venue?** (if not, sponsor outreach becomes priority #1)
5. **Do you have a sponsor?** (if not, generate outreach tasks)
6. **How many weeks until your event?** (determines timeline compression)

---

## Day-format mapping

| Day | Format | Duration | Ideal Size | Cost | Best For | Files |
|-----|--------|----------|-----------|------|----------|-------|
| Monday | **Demo Night** | 2.5h | 50–150 | $200–500 | Builder communities, tech chapters | [`formats/monday-demo-night/`](./formats/monday-demo-night/) |
| Tuesday | **Research Roundtable** | 2.5h | 30–100 | $200–500 | University towns, research communities | [`formats/tuesday-research/`](./formats/tuesday-research/) |
| Wednesday | **Discussion Meetup** | 2h | 15–60 | $0–200 | Any chapter, first-time hosts | [`formats/wednesday-discussion/`](./formats/wednesday-discussion/) |
| Thursday | **Dinner** | 3h | 20–80 | $500–3,000 | Well-funded chapters, executive audiences | [`formats/thursday-dinner/`](./formats/thursday-dinner/) |
| Friday | **Workshop** | 3h | 20–60 | $200–500 | Technical communities, hands-on learners | [`formats/friday-workshop/`](./formats/friday-workshop/) |
| Saturday | **Hackathon** | 8h | 30–100 | $800–3,000 | Large tech chapters, university partnerships | [`formats/saturday-hackathon/`](./formats/saturday-hackathon/) |

The day is a default, not a requirement. If the venue is only available on a different day, use the format files for the chosen format regardless of which day it falls on.

If the chapter lead isn't sure which format to pick, use the decision matrix in [`formats/README.md`](./formats/README.md).

---

## Task generation logic

After getting answers to the first questions, generate a task list using this decision tree:

### No venue?
→ Prioritize venue search. Generate outreach tasks from [`sponsorship/local-sponsor-pitch.md`](./sponsorship/local-sponsor-pitch.md) and [`sponsorship/local-community-partner-kit.md`](./sponsorship/local-community-partner-kit.md). Many sponsors provide venue as in-kind support.

### No sponsor?
→ Generate sponsor outreach tasks. Use the pitch template in [`sponsorship/local-sponsor-pitch.md`](./sponsorship/local-sponsor-pitch.md). Customize using AI prompt #1 from [`ai-prompts/README.md`](./ai-prompts/README.md).

### Less than 4 weeks out?
→ Compressed critical-path timeline:
- Week 1: Confirm venue + format. Send sponsor pitch. Start promoting.
- Week 2: Confirm speakers/facilitators. Blast promotion. Brief panelists.
- Week 3: Final push. Dry run. Prepare day-of materials.
- Week 4: Event week. Execute.

### 4–8 weeks out?
→ Use weeks 4–10 from [`chapter-playbook/timeline-checklist.md`](./chapter-playbook/timeline-checklist.md), compressed to fit.

### 8+ weeks out?
→ Use the full 10-week timeline from [`chapter-playbook/timeline-checklist.md`](./chapter-playbook/timeline-checklist.md).

### Format-specific tasks
After the timeline, add tasks specific to the chosen format from its `agenda.md` and `best-practices.md`:
- **Demo Night**: Source demos (submission form), recruit backup presenters, prepare voting system
- **Research Roundtable**: Recruit diverse panelists, prepare moderator briefing, create reading list
- **Discussion Meetup**: Recruit facilitator, arrange circle seating, print discussion questions
- **Dinner**: Catering (dietary restrictions form, course timing), table assignments, print prompt cards
- **Workshop**: Choose tool, send pre-event install email, recruit helpers/TAs, test Wi-Fi, prepare written guides
- **Hackathon**: Set theme, recruit mentors + judges, prepare team formation process, arrange all-day catering, prepare judging rubric

---

## Topic track overlay (optional)

After the format is chosen, ask: "Do you want a theme for your event?" Present the six tracks:

| # | Track | One-liner |
|---|-------|-----------|
| 1 | What It Means to Be Human in the AI Era | Identity, creativity, meaning — philosophical, broad appeal |
| 2 | AI and the Future of Work | Jobs, skills, automation — universally relatable |
| 3 | AI Safety & Governance | Regulation, oversight, alignment — policy-oriented |
| 4 | Building with AI | Tools, workflows, shipping products — technical, hands-on |
| 5 | How to Be AI Native | Adopting AI into daily life and work — practical |
| 6 | AI in Your City & Industry | Localized impact — the most customizable track |

Full discussion guides with moderator prompts are in [`content/discussion-guides/`](./content/discussion-guides/). Each format's `best-practices.md` recommends which tracks pair well.

---

## HQ Opening — non-negotiable

Every HAIW event starts with the HQ Opening script. This is not optional. It connects the local event to the global movement. The script is in each format's `hq-opening.md` file. It includes:

1. A shared opening (identical worldwide, ~2 min)
2. A format-specific bridge (~1 min)
3. A localization prompt for the chapter lead to fill in (~1 min)
4. A handoff to the first segment (~30 sec)

Help the chapter lead fill in the localization prompt with city-specific context.

---

## Complete repo file index

### Core planning
| File | Description | When to use |
|------|-------------|-------------|
| `CLAUDE.md` | This file — AI agent instructions | First file to read |
| `README.md` | Project overview, quick start, resource index | For human readers |
| `FAQ.md` | Answers to common chapter lead questions | When questions arise |

### Event formats (`formats/`)
| File | Description |
|------|-------------|
| `formats/README.md` | Format comparison table, decision matrix |
| `formats/monday-demo-night/agenda.md` | Demo Night run of show |
| `formats/monday-demo-night/best-practices.md` | Demo Night tips and pitfalls |
| `formats/monday-demo-night/hq-opening.md` | Demo Night opening script |
| `formats/tuesday-research/agenda.md` | Research Roundtable run of show |
| `formats/tuesday-research/best-practices.md` | Research Roundtable tips |
| `formats/tuesday-research/hq-opening.md` | Research Roundtable opening script |
| `formats/wednesday-discussion/agenda.md` | Discussion Meetup run of show |
| `formats/wednesday-discussion/best-practices.md` | Discussion Meetup tips |
| `formats/wednesday-discussion/hq-opening.md` | Discussion Meetup opening script |
| `formats/thursday-dinner/agenda.md` | Dinner run of show |
| `formats/thursday-dinner/best-practices.md` | Dinner tips and catering guide |
| `formats/thursday-dinner/hq-opening.md` | Dinner opening script |
| `formats/friday-workshop/agenda.md` | Workshop run of show |
| `formats/friday-workshop/best-practices.md` | Workshop tips and tool selection |
| `formats/friday-workshop/hq-opening.md` | Workshop opening script |
| `formats/saturday-hackathon/agenda.md` | Hackathon run of show |
| `formats/saturday-hackathon/best-practices.md` | Hackathon tips and team formation |
| `formats/saturday-hackathon/hq-opening.md` | Hackathon opening script |

### Chapter playbook (`chapter-playbook/`)
| File | Description | When to use |
|------|-------------|-------------|
| `chapter-playbook/README.md` | Playbook overview and format options | Starting point for planning |
| `chapter-playbook/event-ops-runbook.md` | Full planning guide: venue, budget, speakers, day-of | Detailed operations reference |
| `chapter-playbook/timeline-checklist.md` | 10-week planning countdown | Building the task timeline |
| `chapter-playbook/run-of-show-template.md` | Legacy run-of-show templates + ground rules | Reference for ground rules |
| `chapter-playbook/post-event-report-template.md` | What to submit after the event | Post-event |

### Content (`content/`)
| File | Description | When to use |
|------|-------------|-------------|
| `content/README.md` | Track overview and selection guide | Choosing a topic track |
| `content/discussion-guides/track-1-human-in-ai-era.md` | Track 1 discussion guide | If track selected |
| `content/discussion-guides/track-2-future-of-work.md` | Track 2 discussion guide | If track selected |
| `content/discussion-guides/track-3-safety-and-governance.md` | Track 3 discussion guide | If track selected |
| `content/discussion-guides/track-4-building-with-ai.md` | Track 4 discussion guide | If track selected |
| `content/discussion-guides/track-5-ai-native.md` | Track 5 discussion guide | If track selected |
| `content/discussion-guides/track-6-ai-in-your-city.md` | Track 6 discussion guide | If track selected |
| `content/facilitation-tips.md` | Moderation and facilitation guidance | For all facilitators/moderators |

### Marketing (`marketing/`)
| File | Description | When to use |
|------|-------------|-------------|
| `marketing/README.md` | Marketing overview and timeline | When starting promotion |
| `marketing/social-copy/` | Ready-to-post social media templates | 6–8 weeks before event |
| `marketing/email-templates/` | Email templates for various audiences | Outreach and promotion |

### Sponsorship (`sponsorship/`)
| File | Description | When to use |
|------|-------------|-------------|
| `sponsorship/local-sponsor-pitch.md` | One-pager pitch for local businesses | When seeking sponsors |
| `sponsorship/local-community-partner-kit.md` | Template for community partner outreach | When recruiting co-hosts |

### Global (`global/`)
| File | Description | When to use |
|------|-------------|-------------|
| `global/messaging-kit.md` | Master messaging, tone guide, core messages | Writing any HAIW copy |
| `global/global-partnership-proposal.md` | For global-level sponsors | Global team use only |
| `global/global-community-partner-kit.md` | For global-level community partners | Global team use only |

### AI Prompts (`ai-prompts/`)
| File | Description | When to use |
|------|-------------|-------------|
| `ai-prompts/README.md` | 13 copy-paste prompts for generating event materials | Generating localized content |

### Flagship conferences (`flagship-conferences/`)
| File | Description | When to use |
|------|-------------|-------------|
| `flagship-conferences/` | Full-day conference planning (SF, NYC, DC) | Hub city conferences only |

---

## Localization instructions

When generating any content for a chapter lead, localize these elements:

- **City name**: Use throughout all materials
- **Local industries**: Reference in discussion framing and sponsor pitches
- **Currency**: Convert budget estimates to local currency
- **Time format**: Use 12-hour or 24-hour based on local convention
- **Language**: If the event is in a non-English language, note that all templates can be translated. The HQ Opening shared section should be delivered in the local language.
- **Local AI context**: What companies, universities, or government initiatives relate to AI in this city?

---

## Tone rules

From [`global/messaging-kit.md`](./global/messaging-kit.md):

| Do | Don't |
|----|-------|
| Urgent but not alarmist | Don't doom-monger |
| Inclusive — "this is for everyone" | Don't gatekeep — no jargon, no prerequisites |
| Grounded — real examples, real stakes | Don't be abstract or academic |
| Hopeful — agency, not helplessness | Don't be cynical |
| Direct — short sentences, clear CTAs | Don't overwrite or hedge |

**The question**: "Where are we going with AI, and who gets a say?"

**Core messages**:
1. The conversation about AI should include everyone, not just the people building it.
2. AI is moving faster than humanity's ability to orient around it. We need to get in the room.
3. This is the largest coordinated civilian conversation about AI ever organized.
4. 200+ cities. 50+ countries. One week. The same conversation.
5. Not a conference. A convening.

---

## Post-event workflow

After the event, guide the chapter lead through:

1. **Submit the post-event report** within 48 hours — use [`chapter-playbook/post-event-report-template.md`](./chapter-playbook/post-event-report-template.md)
2. **Upload photos** to the shared Google Drive folder (link in report template)
3. **Send attendee follow-up email** — use AI prompt #7 from [`ai-prompts/README.md`](./ai-prompts/README.md)
4. **Send sponsor recap email** — use AI prompt #8 from [`ai-prompts/README.md`](./ai-prompts/README.md)
5. **Post on social media** with #HumansInAIWeek — use AI prompt #2 for post ideas
6. **Submit Luma link and attendance data** to catherine@aicollective.com
