# Vibe Code a Store Operations Dashboard with Canvas

## Overview

You are a district manager for Cymbal Pharmacies. Tomorrow morning you run a huddle with 18 store managers, and the numbers you need sit in four different spreadsheets: pharmacy wait times, low stock, flu-shot capacity, and open merchandising issues. You want one screen instead.

In this lab, you sketch that screen, then use Gemini Canvas to turn the sketch into a working dashboard page. You also see why a detailed prompt beats a short one.

<p align="left">
  <img src="images/cymbal-pharmacy-storefront.png" width="70%" alt="Cymbal Pharmacies neighborhood storefront" />
</p>

## Objectives

In this lab, you learn how to:

- Sketch a dashboard layout before you write any prompt.
- Generate a working page in Gemini Canvas from a sketch.
- Compare what Canvas builds from a short prompt versus a detailed prompt.
- Improve the styling with follow-up prompts instead of starting over.

## Task 1. Sketch the dashboard

In this task, you draw the screen you want. Canvas builds a much better page when it can see a layout.

Your dashboard needs four regions:

| Region | Contents |
|---|---|
| Header | The title **Cymbal Pharmacies Store Ops**, plus a district name and today's date |
| KPI cards | Four cards: **Rx Wait Time**, **Low Stock SKUs**, **Flu Shot Slots**, and **Open Cases** |
| Charts | Two placeholders: wait time by hour, and immunizations this week |
| Store table | One row per store, with columns for store, wait time, flu slots, open cases, and next action |

1. Take a sheet of paper or open a whiteboard.
2. Draw a labeled box for each region in the table above. Put the header across the top, the four cards in a row beneath it, the two charts side by side, and the table at the bottom.
3. Stop drawing. Do not add colors, icons, logos, or extra panels.
4. Take a photo of your sketch with your phone and send it to yourself so you can paste it into a browser.

> [!TIP]
> If you would rather not draw, skip steps 1 through 4 and use the sketch below. Right-click it and copy it, then use it everywhere this lab says "your sketch."

<p align="left">
  <img src="images/store-ops-dashboard-sketch.png" width="75%" alt="Hand-drawn wireframe showing a header, four KPI cards, two charts, and a store table" />
  <br>
  <em>Example Store Ops wireframe</em>
</p>

## Task 2. Build a first version with a short prompt

In this task, you give Canvas the sketch and almost no instructions. The result shows you what Canvas assumes when you do not tell it what you want.

1. Open [Gemini](https://gemini.google.com/app) and create a new chat.

> [!NOTE]
> Use the Gemini app for this lab. Canvas is not available in Gemini Enterprise.

2. Click the **+** icon, then select **Canvas** from the Tools list.

<!-- TODO IMAGE: Gemini app Tools menu with Canvas selected -->
![Canvas selected in the Gemini Tools list](images/canvas-tool.png)

3. Paste your sketch into the prompt box.

4. Type the following prompt and press Enter:

```text
Program this dashboard.
```

5. Wait for Canvas to finish writing code. Click the **Preview** tab to see the page.

![First Canvas preview of the Store Ops dashboard](images/canvas-preview-v1.png)

6. Compare the preview against your sketch. Find two things Canvas added, renamed, or left out. You will fix them in the next task.

> [!NOTE]
> Short prompts leave the details to Canvas. Expect invented card names, extra panels, or a search box nobody asked for.

## Task 3. Rebuild the page with a detailed prompt

In this task, you start over with the same sketch and a prompt that names the role, the regions, the card labels, and what Canvas may not add.

1. Click **New chat**.

2. Click the **+** icon and select **Canvas** again.

3. Paste your sketch into the prompt box.

4. Read the prompt below so you can see how much of it is instruction rather than description. Then paste it and press Enter:

```text
You are a senior front-end developer building an internal store operations dashboard for Cymbal Pharmacies district managers.

Use the attached sketch to build the first version of the dashboard.

Requirements:
1. Build a clean, responsive page using HTML, CSS, and JavaScript.
2. Match the layout in the sketch as closely as possible.
3. Include a header, four KPI cards, two chart placeholders, and a store table.
4. Label the KPI cards exactly: Rx Wait Time, Low Stock SKUs, Flu Shot Slots, and Open Cases.
5. Fill the table with sample data for eight neighborhood pharmacies.
6. Keep the design simple, accessible, and easy to read.
7. Do not add logins, maps, chat widgets, live APIs, or backend code.
8. Do not include patient names, prescription details, or clinical advice.

Return only the code needed for this page.
```

5. Click **Preview** when the code finishes.

6. Compare this page with the one from Task 2. This version should match your sketch more closely and invent less.

7. If Canvas still added something you did not ask for, send this follow-up:

```text
Remove anything that is not in the sketch.
```

### Success criteria

- The page shows a header, four correctly named KPI cards, two charts, and a store table.
- The layout matches your sketch.
- No patient or prescription information appears anywhere on the page.

## Task 4. Polish the styling

In this task, you improve how the page looks without changing where anything sits. Stay in the same chat you used for Task 3.

1. Paste the following prompt and press Enter:

```text
Improve the styling of this dashboard while keeping the exact same layout.

Improve:
- Spacing and alignment
- Typography and visual hierarchy
- KPI card styling
- Table readability
- Hover states for cards and table rows

Use a professional navy and teal color palette.
Do not add chart libraries, file uploads, or backend code.
Do not move or rename any region.
```

2. Click **Preview** and confirm the regions did not move.
3. Ask for one more small change. Paste either of these:

```text
Highlight any store whose Rx wait time is over 15 minutes.
```

```text
Add a last-updated timestamp to the header.
```

4. If Canvas rearranged the page, send this correction:

```text
Restore the layout from the sketch and keep the new styling.
```


> [!TIP]
> Notice that these prompts ask for appearance changes only. Keeping structure and styling in separate rounds is what stops Canvas from rebuilding the page on you.

## Task 5. Bonus: build a tool for your own work

In this task, you run the same loop on an idea from your own job. There is no Cymbal scenario here.

1. Write down one internal tool you wish you had. Keep it to one screen.
2. List the four numbers or lists that screen must show.
3. Open a new chat, select **Canvas**, and write a prompt that names your role, the four regions, and what Canvas may not add. Do not attach a sketch this time.
4. Click **Preview**, then send one follow-up prompt that fixes the biggest problem you see.
5. Be ready to describe your tool and the follow-up prompt to the group.

## Congratulations!

You sketched a store operations dashboard, built it twice in Gemini Canvas, and saw how a detailed prompt produces a page that matches your intent while a short prompt produces guesses. You also learned to change styling and structure in separate rounds. Use this loop the next time someone asks whether you can mock something up before a meeting.
