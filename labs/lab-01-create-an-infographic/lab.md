# Create a Back-to-School Infographic

## Overview

<p align="left">
  <img src="images/cymbal-pharmacy-storefront.png" width="70%" alt="Cymbal Pharmacies neighborhood storefront with a back-to-school window display" />
</p>

Cymbal Pharmacies is a national neighborhood pharmacy retailer with a pharmacy counter in every store and CymbalCare clinics in larger sites. Marketing needs a promotional infographic for the Back-to-School Super Sale, and it has to look like a pharmacy campaign, not a big-box school-supply ad.

The Marketing team needs a horizontal infographic for the **Back-to-School Super Sale**. The brief: show the contrast between the stress of August spending and the relief a neighborhood pharmacy can provide. The asset must include school supplies, kids wellness items, photo prints, ExtraValue member savings, and the Cymbal Pharmacies logo.

## Objectives

In this lab, you learn how to:

- Compare a short image prompt with a detailed prompt that includes role framing, visual metaphors, and specific campaign copy.
- Attach a brand logo as visual context for a generated asset.
- Iterate on a prompt by changing one or two elements at a time.
- Generate a branded promotional infographic grounded in real campaign details.

## Task 1. Generate the baseline infographic

In this task, you attach the Cymbal Pharmacies logo, try a short ad request, then send a detailed prompt so you can see how much specificity changes the image.


1. Sign in to Gemini Enterprise (or the Gemini app) in your browser. Start a new chat.


2. In the chat bar, select the **Tools** icon and choose the images tool.

![Tools menu with the images tool selected](images/images-tool.png)

3. Copy the Cymbal Pharmacies logo below, and paste it into the chat:

<p align="left">
  <img src="images/cymbal-pharmacies-logo.png" width="50%" alt="Cymbal Pharmacies logo" />
  <br>
  <em>Cymbal Pharmacies logo</em>
</p>

4. Start with a short prompt. Copy and paste the following into the chat, then press Enter:

```text
Create a Back-to-School ad for Cymbal Pharmacies. Use the attached logo.
```

5. Review the first image. Note what is missing or generic: campaign offers, readable text, pharmacy-specific products, or a layout Marketing could actually post.

6. Create a new chat, and paste the logo again. This time, copy and paste the detailed prompt below, then press Enter:

```text
You are a data visualization artist who creates infographics with dramatic, physical metaphors. Create a striking, horizontal infographic-style image promoting the "Cymbal Pharmacies: Back-to-School Super Sale."

The scene is a dramatic, split landscape. On the left side, labeled "THE AUGUST MOUNTAIN," stands a massive, precarious, towering pile of crumpled homework, worn-out backpacks, broken pencils, empty first-aid boxes, and dull grays. A sign on this pile reads: "$1,200+ National Average Spend (2025)." A cartoon parent below looks overwhelmed and exhausted, shielding their eyes.

On the right side, labeled "THE CYMBAL SOLUTION," the same mountain has been replaced by a sprawling, organized neighborhood made entirely of fresh, colorful school supplies, kids vitamins, first-aid kits, and photo-print envelopes. Notebook skyscrapers, pencil-case buses, and a small CymbalCare clinic kiosk gleam with primary colors. An energetic student wearing a "Cymbal Approved" backpack runs toward the scene, pulling a wagon stacked with glowing deals labeled "50% OFF" and "$1 BACK-TO-SCHOOL DEALS."

A large, friendly Cymbal Pharmacies logo is integrated seamlessly as the central archway entrance. Along the bottom, clean data callouts read: "$40 ExtraValue Family Savings," "1,000+ Items Under $5," and "Same-Day Store Pickup and 4x6 Prints." The final banner text across the bottom reads: "Cymbal Pharmacies: Ready for School. Ready for Anything."

See the attached image for the official Cymbal Pharmacies logo.
```

7. Review the second image and compare it with the short-prompt result. Note what worked well and what you would still change: logo accuracy, readable text, split-scene balance, and whether the scene feels like a pharmacy.

<p align="left">
  <img src="images/back-to-school-infographic-example.png" width="75%" alt="Example Back-to-School infographic with a stressed August mountain on the left and a colorful Cymbal solution on the right" />
  <br>
  <em>Example result. Your image will differ. Watch for misspellings in generated text, such as a mistyped brand name.</em>
</p>

> [!TIP]
> Generated text in images is often the weakest part of the first pass. If the logo or tagline is wrong, treat that as the first thing to fix in Task 2 rather than regenerating the entire concept.

## Task 2. Iterate to improve the result

In this task, you practice prompt engineering for images by changing one or two things at a time.

Try at least two of the following refinements:

1. **Adjust the style.** Add a style instruction to the end of the detailed prompt, for example:

```text
The style should be a bold, flat vector illustration with thick outlines, similar to a children's book or modern editorial design.
```

2. **Fix a specific element.** Isolate one problem instead of rewriting the whole brief:

```text
Regenerate the image. Move the Cymbal Pharmacies logo to the upper-right corner, spell the brand name exactly as Cymbal Pharmacies, and make the tagline text larger and easier to read.
```

3. **Change the campaign.** Swap Back-to-School for a **flu season** version. Replace the mountain metaphor with a crowded waiting room versus a calm CymbalCare immunization lane. Update the callouts to flu shot walk-in hours, ExtraValue member pricing, and same-week appointments.

> [!NOTE]
> Each iteration should change only one or two things at a time. Changing everything at once makes it hard to understand what improved the result.

### Success criteria

- The image is horizontal and reads as a campaign infographic, not a random store photo.
- The Cymbal Pharmacies name is spelled correctly.
- You can explain which prompt change improved the second or third version.

## Task 3. Create an infographic for your own campaign

In this task, you transfer the same pattern to a campaign you actually care about.

1. Start a new chat and attach the Cymbal Pharmacies logo, or a logo from your own work if your instructor allows it.
2. Write a prompt that includes a role, a visual metaphor, specific prices or offers, and a tagline.
3. Generate the image, then run one focused refinement.

> [!NOTE]
> Good pharmacy-retail ideas include a vaccination weekend, a photo-center promotion, a diabetes-awareness endcap, or a caregiver wellness event.

## Congratulations!

You compared a short Back-to-School request with a detailed prompt, iterated with focused changes, and applied the same pattern to a campaign of your own. You can reuse this workflow any time Marketing needs a first-pass visual before a designer takes over.
