# Build a Competitive Brief in Gemini Notebook

## Overview

You are the Director of Clinical Programs at Cymbal Pharmacies. Leadership wants a readout on fall immunizations: can stores and CymbalCare clinics absorb the demand, and how are competitors advertising walk-ins, booking, and price? You have an internal capacity brief. You have nothing reliable from outside the company.

In this lab, you build a Gemini Notebook that holds the internal brief beside live web sources, ask questions that need both, and save a cited paragraph for the readout.

## Objectives

In this lab, you learn how to:

- Create a notebook and add an internal source as copied text.
- Use the Notebook Guide to get a structured overview of a source.
- Search the web from Gemini Notebook and add live sources.
- Ask questions that combine private internal data with public competitor and public-health sources.
- Save a short note you could drop into a leadership brief.

<p align="left">
  <img src="images/cymbal-pharmacies-logo.png" width="45%" alt="Cymbal Pharmacies logo" />
</p>

## Task 1. Create the notebook and add the internal brief

In this task, you load your internal capacity brief. It is the only private source in the notebook, and for now it is the only source at all.

<p align="left">
  <img src="images/cymbal-district-huddle.png" width="70%" alt="Cymbal Pharmacies clinical and operations leaders reviewing immunization planning" />
</p>

1. Open [Gemini Notebook](https://notebook.google.com/) and create a new notebook.

2. Close the **Add sources** screen if it blocks the notebook, then name the notebook `Cymbal Fall Immunization Brief`.


![New notebook titled Cymbal Fall Immunization Brief](images/new-notebook.png)

3. In the **Sources** panel, click **+ Add sources**, select **Copied text**, paste the brief below, and click **Insert**:

```text
CYMBAL PHARMACIES — CONFIDENTIAL
Fall Immunization and CymbalCare Capacity Brief
Prepared for: Clinical Programs, Pharmacy Operations, and Store Operations
Date: September 8
Owner: Director of Clinical Programs

PROGRAM GOAL
Protect neighborhood access to influenza, COVID-19, and back-to-school required vaccines while keeping pharmacy ready-time at or below 15 minutes.

NETWORK
- 1,240 neighborhood stores with immunizing pharmacists
- 310 CymbalCare clinics (nurse practitioners) co-located in larger stores
- ExtraValue members: $5 off flu shot through September 30
- Non-members: standard posted cash price; insurance billed when eligible

CAPACITY SNAPSHOT (INTERNAL)
- Average flu-shot slots remaining this Saturday across District 14: 18 per store
- Stores near large high schools (including Store 2482): Saturday walk-in boards are clearing by 11 a.m.
- CymbalCare physicals and school-form visits are already 70 percent booked for the next 10 weekdays
- Immunizing pharmacist vacancy: 4 percent district-wide, 11 percent in District 14
- Last season's no-show rate for scheduled shots: 12 percent

PROTOCOL NOTES
- Standing order allows trained pharmacists to administer seasonal influenza vaccine to eligible patients per current CDC timing
- Pediatric vaccines outside standing-order age ranges route to CymbalCare or the patient's medical home
- Consultation window conversations must not be audible from the greeting-card aisle
- Stores may not handwritten-change vaccine prices on posters

KNOWN GAPS
- 22 percent of stores still display last season's immunization poster
- Same-day flu walk-in messaging is inconsistent on store door hours stickers
- Competitive walk-in and membership pricing is rumored but not verified in this brief
- No head-to-head internal study of ExtraValue $5 offer versus competitor cash prices

QUESTIONS LEADERSHIP WILL ASK
1. Are we a walk-in brand or an appointment brand this fall?
2. Which competitors are advertising no-appointment shots in our metro markets?
3. Does the ExtraValue $5 offer still look meaningful?
4. What should District 14 do this week about Saturday capacity?
```

4. After the source is added, rename it to `Cymbal Fall Immunization Capacity Brief`.
5. Read the Notebook Guide or chat overview. Confirm that Gemini identified the store network, ExtraValue offer, District 14 pressure, and the open leadership questions.

> [!NOTE]
> With only this source loaded, Gemini knows Cymbal's plan and nothing reliable about competitors or current public-health guidance. That changes in the next task.

## Task 2. Search the web and add live sources

In this task, you use Gemini Notebook's built-in web search so you do not copy links from a browser.

1. In the **Sources** panel, find **Search the web for new sources**.

![Search the web for new sources box in Gemini Notebook](images/web-search-box.png)

2. Open the research-mode dropdown next to the search box. Choose **Fast Research** for this lab. 


![Research mode dropdown with Fast Research selected](images/research-mode.png)

3. Run each search. After each one, review the suggested sources and add the most relevant results (or all of them).

**Search 1 — current public-health guidance:**

```text
CDC influenza vaccination recommendations current season timing
```

Look for CDC or other official public-health pages on who should be vaccinated and when the season starts.

**Search 2 — national drugstore competitor:**

```text
Walgreens flu shot walk-in appointment price
```

Look for booking pages, season announcements, and any stated walk-in or membership offer.

**Search 3 — mass-retail competitor:**

```text
Walmart Pharmacy flu shots and clinic services
```

Look for pharmacy immunization pages and any in-store clinic language.

**Search 4 — digital or cash-pay pressure:**

```text
Amazon Pharmacy prescriptions delivery membership
```

This source will not answer flu-clinic questions by itself. It is there so you can see how digital pharmacy changes customer expectations.

> [!NOTE]
> Prefer official public-health sites, company investor or help pages, and established news outlets. Skip random blogs when a primary page is available. You can add more sources later.

4. Your notebook should now contain the Cymbal internal brief plus live web sources.

## Task 3. Ask questions that need both kinds of sources

In this task, you ask questions no single source can answer well.

1. Start with a public-guidance question:

```text
According to the public-health sources in this notebook, who should receive an influenza vaccine this season and when should vaccination begin? How should Cymbal Pharmacies talk about timing in store without inventing clinical advice beyond those sources?
```

2. Ask a competitive comparison:

```text
Compare Cymbal Pharmacies' ExtraValue $5 flu-shot offer and Saturday walk-in pressure with what the Walgreens and Walmart sources say about booking, walk-ins, and price. Where is Cymbal clearly different, and where is the public evidence too thin to claim a win?
```

3. Ask an operations question that uses the internal brief:

```text
Using the Cymbal capacity brief and the competitor sources, what should District 14 do this week about Saturday immunization capacity at school-adjacent stores? Give three actions and label anything that depends on unverified competitor claims.
```

4. Ask a gap question:

```text
Based on the sources in this notebook, what is the single most important question Cymbal leadership will ask that the current sources cannot yet answer?
```

> [!NOTE]
> A question the notebook cannot fully answer is useful. It tells you what still belongs in a human phone call or a store visit.

5. Deselect the Cymbal internal brief and re-ask the District 14 question. The answer should get weaker or more generic. That is how you confirm the internal source was doing real work.

## Task 4. Save a note for the leadership readout

In this task, you capture a paragraph you could paste into a slide.

1. Ask:

```text
Write a one-paragraph Competitive and Capacity Summary for the first page of the Cymbal Pharmacies fall immunization readout. Use only notebook sources. Cite the public sources in plain language. Do not invent prices or store counts.
```

2. Save the paragraph as a note in the notebook.
3. If a sentence is not backed by a source, delete it or ask Gemini to rewrite with citations only.

### Success criteria

- The notebook contains the internal brief and at least three web sources.
- Answers to Task 3 questions include citations you can open.
- The saved note does not invent competitor prices that were not in a source.

## Task 5. Try the pattern on your own topic

In this task, you build a second, smaller notebook for a problem from your role.

1. Create a new notebook.
2. Paste a short internal memo as copied text. It can be fictional or a sanitized version of real work.
3. Run two Fast Research queries on a competitor, a regulation, or a clinical guideline.
4. Ask one question that requires both the internal text and the web sources.

Good pharmacy-retail topics include cash-pay generics, retail-clinic staffing, photo-center seasonal offers, or a new immunization schedule.

## Congratulations!

You built a Gemini Notebook that holds Cymbal Pharmacies' internal immunization brief beside live public sources, asked cited questions across both, and saved a leadership paragraph. That is the research workspace pattern clinical, compliance, and operations partners can reuse when the protocol and the public story must stay connected.
