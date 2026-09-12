# Apply Prompt Engineering Best Practices

## Overview

You are a district operations analyst at Cymbal Pharmacies. Every Monday you receive a messy dump of store texts, pharmacy wait-time exports, clinic calendars, and campaign notes. Your district leader needs a briefing they can run a call from, not a summary they have to rewrite.

In this lab, you work that memo with Gemini. You start with a plain request, rebuild it using a repeatable 5-step framework, then apply persona instructions, delimiters, one-shot examples, and meta-prompting.

## Objectives

In this lab, you learn how to:

- Compare a raw prompt with a structured prompt that names role, audience, and format.
- Use the 5-step framework to make prompts repeatable.
- Separate instructions from examples with delimiters.
- Use a one-shot example to lock tone and structure.
- Use meta-prompting to improve a prompt before you rely on it.


<p align="left">
  <img src="images/cymbal-pharmacies-logo.png" width="45%" alt="Cymbal Pharmacies logo" />
</p>

## Task 1. Compare a raw prompt with a basic prompt

In this task, you see why prompt engineering matters before you learn a formal framework.

You cover District 14: 18 neighborhood stores and 6 CymbalCare clinics near a large school system. Flu season is starting, Back-to-School product is still on endcaps, and pharmacy wait times spiked last week. This week's ops dump is below.

<p align="left">
  <img src="images/cymbal-district-huddle.png" width="70%" alt="Cymbal Pharmacies district leaders reviewing a briefing before a huddle" />
</p>

1. Sign in to Gemini Enterprise (or the Gemini app) and start a new chat.

2. Paste the ops dump below into the chat. Do not press Enter yet.

```text
CYMBAL PHARMACIES — DISTRICT 14 WEEKLY OPS DUMP
Week of September 8 | Unofficial notes compiled from store texts, Rx queue exports, and clinic calendars
From: ops-inbox@cymbalpharmacies.example

Store 2482 (high school corner): Rx ready-time average 28 min Thu-Sat, target is 15. Pharmacist called out Friday. Tech overtime 11 hours. Flu shot board says walk-ins welcome but only 2 slots left on Saturday by 11am. Back-to-School endcap still 40% empty on binders. Photo kiosk jammed twice.

Store 1904: Wait time 12 min. Flu clinics fully booked through next Wednesday. Manager asking if we can borrow 1 immunizing RPh from 2482. OTC kids fever aisle looks good. ExtraValue sign on door is faded.

Store 771: CymbalCare nurse practitioner out Monday-Tuesday. 14 physicals already on the book. Front-shop recovered well after truck delay. One customer complaint: consultation window conversation could be overheard from greeting cards.

Store 3305: Cooler temp log missed Wednesday night. Assistant manager says it was "probably fine." Infant formula fully stocked. Immunization poster still shows last year's dates.

Campaign: ExtraValue members get $5 off a flu shot through September 30. Marketing wants stores to mention photo prints in the same breath as school supplies. No one is sure which stores actually did.

Random: Corporate asked for "a one-pager on where we are hurting and what to do this week." Also someone forwarded a rumor that a nearby competitor is offering same-day flu shots with no appointment. Not verified.
```

3. Add this plain request under the memo, then press Enter:

```text
Summarize this memo.
```

4. Review the output. Note whether it is too long, too generic, missing owners, or burying the items a district leader must act on this week.

5. Start a new chat, paste the same memo, and try a slightly improved prompt:

```text
You are a district operations analyst for Cymbal Pharmacies.
Summarize the weekly ops dump for a Monday district huddle.
Use only the facts in the memo.
Return 4 bullets: where we are hurting, what is working, this week's actions, and what is still unverified.
```

6. Compare the two responses. The second prompt should usually be easier to run a huddle from because it provides a role, an audience, and a target format.

## Task 2. Use the 5-step framework

In this task, you turn the same kind of request into a reusable prompt pattern.

The five steps help turn a vague request into a repeatable prompt:

- Task: state exactly what you want the model to do.
- Context: explain who the output is for and how it will be used.
- References: define what sources the model should rely on.
- Evaluation: set the quality bar for the answer.
- Iteration: tell the model what to do if the result is incomplete or uncertain.

1. Start a new chat and paste the District 14 memo again.

2. Copy and paste the framework prompt:

```text
Task:
Turn the weekly ops dump into a decision-oriented district briefing and recommend the top three actions for this week.

Context:
The audience is a District Leader who has 10 minutes before a call with 18 store managers. They care about pharmacy wait times, immunization capacity, store standards, and anything that could become a customer or compliance issue.

References:
Use only the information in the pasted ops dump. Treat rumors as unverified.

Evaluation:
The answer should be accurate, concise, and tied to named stores. Do not invent volumes, budgets, or clinical advice.

Iteration:
If a recommendation is uncertain, say why and name the missing information.

Output:
Return:
1. Situation in five lines
2. Top three actions, each with an owner role and a due date
3. Stores that need a same-day check-in
4. One question to ask Store 2482 and one question to ask Store 3305
```

3. Review whether Gemini stayed inside the memo and produced actions a real district team could take.

4. If the briefing is still too essay-like, reply: "Shorten each action to one sentence and move unverified items to a separate list."


## Task 3. Apply advanced prompting techniques

In this task, you keep the same chat open and tighten control over tone and format.

### Part A. Set system-style instructions

1. Paste a persona block before the next request:

```text
You are a senior operations communications assistant for Cymbal Pharmacies.

Behavior rules:
- Write in concise operations language.
- Prefer clarity over flair.
- Use Markdown headings and bullets when it improves readability.
- Never invent wait times, inventory counts, clinical guidance, or competitor facts.
- Flag uncertainty explicitly.
- Keep recommendations practical for store and pharmacy teams working during open hours.

Now help me write a huddle-ready briefing from the District 14 ops dump in this chat.
```

2. You do not need to repeat the persona in every follow-up as long as you stay in this chat.

### Part B. Separate instructions from the format with delimiters

1. Ask Gemini to rewrite the briefing using a locked format:

```text
Rewrite the huddle briefing for District 14.

Rules:
- Base the briefing only on the ops dump in this chat.
- Do not invent missing facts.
- Match the structure of the template below.
- Keep it concise and decision-oriented.

<briefing-format>
Title: [District and week]

Snapshot:
[Two sentences]

Priorities:
- [Store or program]: [Action]
- [Store or program]: [Action]
- [Store or program]: [Action]

Watch-outs:
- [Compliance or customer-experience risk]

Unverified:
- [Item that still needs a phone call]
</briefing-format>
```

2. Check whether Gemini stayed inside the template and avoided extra sections.

### Part C. Use a one-shot example to lock the style

One-shot prompting means embedding a complete example of the output you want. The model copies structure, tone, and level of detail.

1. Paste the prompt below:

```text
Here is one example of a well-written district huddle note. Use it as a one-shot example. Match its structure, tone, and level of detail.

--- EXAMPLE START ---
Title: District 8 — Week of August 25

Snapshot:
Wait times are stable except Store 1120 after a midweek call-out. Flu booking is ahead of last year at clinic stores. Front-shop recovery from the truck delay is complete.

Priorities:
- Store 1120: Borrow one immunizing pharmacist on Saturday to protect the 15-minute ready-time target.
- Store 880: Replace last-year immunization posters before Friday open.
- District: Confirm ExtraValue flu-shot signing is posted at all 12 stores by Thursday 5 p.m.

Watch-outs:
- Store 880 consultation window is still readable from the card aisle. Move the queue stanchion today.

Unverified:
- Competitor weekend clinic hours are a rumor only. Manager at 1120 will confirm after their lunch break.
--- EXAMPLE END ---

Now write a huddle note in the same format for District 14 using only facts from the current chat. Do not invent metrics.
```

2. Compare Parts A, B, and C. Which version would you actually paste into the district Slack channel?
3. Notice that the one-shot example is most useful when you already have a note your leaders liked. The richer the example, the less the model has to guess.

## Task 4. Improve the prompt with meta-prompting

In this task, you ask Gemini to rewrite the prompt itself before you use it on real work.

1. Start a new chat and paste:

```text
Act as a prompt engineer for retail pharmacy operations.

Review the prompt below and rewrite it using the 5-step framework:
1. Task
2. Context
3. References
4. Evaluation
5. Iteration

--- PROMPT START ---
Help me write a huddle-ready briefing from the District 14 weekly ops dump using the structure, tone, and level of detail of a good district note.

Mirror a practical, skeptical operations tone. Use the same section headings (Snapshot, Priorities, Watch-outs, Unverified).

Pull specific store numbers, wait times, and open issues from the memo. Do not invent clinical advice.

Use clean Markdown with bold headers and bullets.
--- PROMPT END ---
```

2. Copy the improved prompt. Open a new chat, paste the District 14 memo, then paste the improved prompt.
3. Compare the result with your Task 3 Part C note. Did the rewritten prompt reduce fluff or invented detail?

## Task 5. Apply the techniques to your own work

In this task, you transfer the pattern to a real briefing you owe someone.

1. Pick a task from your role: a store recap, a campaign readout, a clinic schedule problem, or a vendor issue.
2. Write a raw first prompt and note where the output falls short.
3. Rewrite it with the 5-step framework. Optionally add a persona block, delimiters, or a one-shot example from a note you were proud of.
4. Be ready to share the before and after with the group and name the technique that helped most.

## Congratulations!

You compared weak and structured prompts, used a 5-step framework, applied persona instructions, delimiters, and one-shot examples, and used meta-prompting to improve the prompt itself. That is the same craft you can take back to district huddles, pharmacy ops reviews, and campaign readouts.
