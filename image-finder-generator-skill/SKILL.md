# Image Finder & Generator Skill

## Purpose

This skill helps the user find suitable images based on a short description.  
The first priority is to search the web for existing images and provide clear source information.  
If no suitable image can be found, the skill may generate a new image and clearly tell the user that the image is AI-generated.

## User Input

The user may provide:

- A short image description
- Intended use, such as essay, presentation, poster, social media, website, or personal reference
- Preferred style, such as realistic, academic, infographic, cartoon, editorial, minimal, or poster-style
- Required format, such as landscape, portrait, square, transparent background, or high resolution
- Any restrictions, such as no watermark, free-to-use only, UK context, food security theme, climate theme, etc.

If key information is missing, ask only one or two necessary follow-up questions.  
If the request is clear enough, proceed without asking.

## Core Workflow

### Step 1: Understand the Image Need

Rewrite the user's request into a clear search brief.

Identify:

- Main subject
- Visual style
- Context or theme
- Intended use
- Required orientation or format
- Whether the image needs to be realistic, symbolic, academic, or decorative

Example:

User request:
> I need an image of a warehouse full of food but people cannot access it because of poverty and inequality.

Search brief:
> Symbolic image showing food abundance but restricted access, with themes of poverty, conflict, inequality, food security, hunger, and social justice.

---

### Step 2: Search Existing Images First

Always search for existing images before generating a new one.

Search across relevant sources, such as:

- Wikimedia Commons
- Unsplash
- Pexels
- Pixabay
- Flickr Creative Commons
- Government or NGO image libraries
- Academic or institutional sources
- News or report images, if appropriate

Use multiple search queries if needed.

Example search queries:

- "food security poverty inequality warehouse image"
- "food aid warehouse poverty access"
- "food abundance hunger inequality illustration"
- "empty wallet food access poverty image"
- "food security barriers poverty conflict inequality visual"

---

### Step 3: Evaluate Search Results

For each useful image, evaluate:

- Relevance to the user’s description
- Image quality
- Whether it has a clear source
- Whether the author or institution is identifiable
- Whether the licence allows reuse
- Whether attribution is required
- Whether the image contains watermarks
- Whether it is suitable for academic or public-facing use

Do not recommend images if:

- The source is unclear
- The licence is unclear and the user needs public/academic reuse
- The image is low quality
- The image is misleading
- The image contains copyrighted material without reuse permission
- The image is AI-generated but presented as a real photograph

---

### Step 4: Output Search Results Clearly

When suitable images are found, provide them in a table.

Use this format:

| Option | Image Description | Source | Licence / Usage | Best Use | Notes |
|---|---|---|---|---|---|
| 1 | Short description of the image | Website / author / organisation + link | Licence type or usage condition | Essay / poster / slides / social media | Any cautions |

For each image, include:

- Direct source link
- Author or organisation if available
- Licence information if available
- Attribution format if needed
- Whether the image is free to use, requires attribution, or needs permission

Never invent missing licence information.  
If the licence is unclear, say clearly:

> The source is visible, but the reuse licence is unclear. I would not recommend using this image in a submitted academic poster unless permission is confirmed.

---

### Step 5: Recommend the Best Option

After listing results, recommend the most suitable image.

Explain briefly:

- Why it matches the user’s description
- Whether it is safe to use
- Whether it fits the intended format
- Any citation or attribution needed

Example:

> I recommend Option 2 because it clearly shows food access inequality, has a reliable source, and is available under a Creative Commons licence. It would work well for an academic poster if you include the attribution below the image.

---

### Step 6: Generate an Image Only If Needed

If no suitable existing image is found, offer or create an AI-generated image.

Before generating, explain:

> I could not find a suitable existing image with a clear source and usable licence. The best option is to generate a new image based on your description. This image should be labelled as AI-generated if used in academic or public work.

When generating, produce:

- A clear image prompt
- Suggested style
- Suggested aspect ratio
- Short note for disclosure

Example disclosure:

> Image generated using AI based on the author’s prompt, 2026.

---

## AI Image Generation Prompt Format

When generating an image, use this structure:

```text
Create a [style] image of [main subject].
The scene should show [key visual details].
The mood should be [tone].
Use [composition, colour, lighting].
Avoid [unwanted elements].
Aspect ratio: [ratio].
The image should be suitable for [intended use].
