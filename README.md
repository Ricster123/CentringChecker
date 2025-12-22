# Card Centering Tool (Pokémon TCG)

A browser based tool for **measuring Pokémon card centring** from photos or scans, with optional **rotation and perspective correction** before measurement.

Built to be fast, visual, and accurate without needing external software.

---

## Features

- Measure **Left / Right** and **Top / Bottom** centring
- Pixel level measurements with percentage split output
- Supports **Front and Back** of the card
- Optional **Rotate only** correction to straighten skewed images
- Optional **Perspective correction** locked to Pokémon card aspect ratio (63 × 88 mm)
- Visual guides with locked axes for consistent measurements
- Pan and zoom with mouse or touch
- Export a **print ready PDF** with annotated images and results
- Runs fully client side, no uploads, no tracking

---

## How it works

1. Upload a photo or scan of the card
2. Optional: apply Geometry correction  
   - **Rotate only**: draw a short line along any straight border  
   - **Perspective**: draw four short lines along the card edges
3. Measure centring  
   - **Left / Right**: outer left, inner left, inner right, outer right  
   - **Top / Bottom**: outer top, inner top, inner bottom, outer bottom
4. Repeat for the back of the card
5. Export the results as a PDF

---

## Geometry correction

### Rotate only
- Automatically snaps to **horizontal or vertical**
- Drawing a vertical edge will straighten the card without rotating it sideways
- Best for slightly tilted but otherwise flat images

### Perspective correction
- Corrects keystone distortion from angled photos
- Normalises the card to the official Pokémon TCG aspect ratio (63 × 88 mm)
- Should be used before measuring if the photo was not taken square on

---

## Controls

- Mouse wheel or pinch to zoom
- Middle mouse button or two finger drag to pan
- Click to place measurement points
- `U` to undo last point
- `R` to clear the active measurement axis

---

## Accuracy & limitations

This tool measures **pixel based centring** from an image.  
Results are only as accurate as the image and the points placed by the user.

### Accuracy

- Measurements are calculated from **exact pixel distances**
- Axis locking ensures consistent horizontal and vertical measurements
- Rotation and perspective correction are applied **before** any centring calculations
- Perspective correction enforces the Pokémon card aspect ratio (63 × 88 mm)

With a high resolution, well lit image taken square to the card, results are **highly consistent and repeatable**.

### Image quality matters

Accuracy is affected by:
- Low resolution images
- Motion blur or heavy JPEG compression
- Strong shadows along card edges
- Rounded corners blending into the background
- Cropped or partially obscured borders

For best results:
- Take photos slightly zoomed in from further away
- Use even lighting and a plain background
- Avoid wide angle distortion from very close shots

### User input

All measurements rely on **manual point placement**.

Common mistakes include:
- Clicking artwork instead of the true card edge
- Mixing up inner and outer border clicks
- Measuring a skewed image without applying perspective correction first

Follow the on screen prompts and labels carefully.

### What this tool does not do

- It does **not** automatically detect borders
- It does **not** predict grading outcomes
- It does **not** account for print tolerance or factory variance
- It does **not** guarantee PSA, CGC, or Beckett centring results

Different grading companies may interpret centring differently, even with identical measurements.

---

## Requirements

- A modern browser (Chrome, Edge, Firefox, Safari)
- No installation
- No backend
- No dependencies

---

## Disclaimer

This tool is for **personal reference and comparison only**.

It is **not affiliated with or endorsed by PSA, CGC, Beckett, or The Pokémon Company**.  
Grading decisions are subjective and influenced by factors beyond centring, including corners, edges, surface condition, and print quality.
