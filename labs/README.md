# Labs

Hands-on lab Markdown for this course lives in this folder.

These labs use **Cymbal Pharmacies**, a fictional national neighborhood pharmacy retailer similar to a large U.S. drugstore chain. Stores include a front-shop, a pharmacy counter, ExtraValue member offers, and CymbalCare clinics in larger locations.

## Course labs

| # | Lab | Role it speaks to | What learners do |
|---|---|---|---|
| 1 | [Create a Back-to-School Infographic](lab-01-create-an-infographic/lab.md) | Marketing and merchandising | Generate and iterate a campaign infographic in Gemini Enterprise |
| 2 | [Analyze a Store Walkthrough Video](lab-02-video-analysis-store-walkthrough/lab.md) | Store operations and field merchandising | Audit instructor-provided video against a pasted standards checklist |
| 3 | [Apply Prompt Engineering Best Practices](lab-03-prompt-engineering-best-practices/lab.md) | Pharmacy and district operations | Turn a messy weekly ops memo into a huddle-ready briefing |
| 4 | [Run Competitive Deep Research](lab-04-deep-research/lab.md) | Strategy and competitive intelligence | Research a real pharmacy competitor and write a leadership note |
| 5 | [Build a Competitive Brief in Gemini Notebook](lab-05-gemini-notebook/lab.md) | Clinical, compliance, and L and D | Combine an internal immunization brief with live web sources |
| 6 | [Vibe Code a Store Operations Dashboard with Canvas](lab-06-vibe-coding-with-canvas/lab.md) | Store and district managers | Turn a sketch into a Store Ops dashboard shell in Gemini Canvas |

Each lab is standalone. There are no Google Drive dependencies. Sample memos and checklists are embedded as copy-paste text. UI screenshots that still need capture are marked with `TODO IMAGE` comments.

## Layout

```text
labs/
  lab-01-create-an-infographic/
    lab.md
    images/
  lab-02-video-analysis-store-walkthrough/
    lab.md
    images/
  lab-03-prompt-engineering-best-practices/
    lab.md
    images/
  lab-04-deep-research/
    lab.md
    images/
  lab-05-gemini-notebook/
    lab.md
    images/
  lab-06-vibe-coding-with-canvas/
    lab.md
    images/
```

## Authoring

Follow the **Lab Generator** skill:

- [.agents/skills/lab-generator/SKILL.md](../.agents/skills/lab-generator/SKILL.md)
- [.agents/skills/lab-generator/examples/lab-template.md](../.agents/skills/lab-generator/examples/lab-template.md)

## Preview

Use the [HTML Lab Viewer](https://github.com/roitraining/md-to-html-lab-viewer) with a `?lab=` URL pointing at the lab folder or its `lab.md`.

## Sample

See [lab-01-sample-lab-viewer-format](lab-01-sample-lab-viewer-format/lab.md) for a minimal reference manual. It is not part of the Cymbal Pharmacies series.
