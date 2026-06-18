# Tao Birthday Gift Website Brief

## Goal

Create a mobile-first 9:16 birthday gift website for a handmade seal gift.

Recipient:

- Name: 曾宪涛
- Short display name: 涛

Sender/signature:

- 谢海

The site should feel like a refined personal birthday gift reveal, not a template slideshow or PPT.

Core feeling:

- Minimal, restrained, tasteful.
- Realistic and cinematic, based on the actual seal photos.
- Mobile Safari / WeChat browser first.
- No stretched images or videos. Keep aspect ratio locked.

## Assets

### Opening video

Primary:

- `assets/opening_video/primary_opening_2K30_30fps.mp4`
- Use this as the main opening video.
- Black background, white text, about 9 seconds.

Optional:

- `assets/opening_video/optional_opening_4K_60fps.mp4`
- Higher spec option. Use only if performance is still good on mobile.

### Original images

Use these original images and process them yourself:

- `assets/original_images/01.jpeg`
- `assets/original_images/02.jpeg`
- `assets/original_images/03.jpeg`
- `assets/original_images/04.jpeg`
- `assets/original_images/05.jpeg`

Do not reuse another AI's already processed web images. You may resize/compress/sharpen lightly for web delivery, but do not make the images gray, overexposed, plastic-looking, or stretched.

## Required Sequence

Visual sequence after the opening video:

1. Image 01
2. Image 02
3. Image 05
4. Image 04
5. Image 03 as the final still

Note: image 03 and image 05 were intentionally swapped. The final image should be 03.

## Interaction Requirements

### Initial state

- The page opens on a pure black screen.
- A button is shown around the lower-middle area.
- While loading, the button shows `加载中...` with a small loading icon/spinner.
- The button is disabled until the opening video and all five images are fully ready.
- Once all assets are ready, the button changes to `轻触开始`.
- Before the user starts, nothing else should flash or show: no first photo, no video poster, no progress bar, no final text.

### Playback

- Tap `轻触开始` to play the opening video.
- After the video ends, automatically show the five images.
- Each image stays for 2.16 seconds.
- Transitions should be subtle and clean. Do not use noisy effects.
- If swipe navigation is supported, it must not break the automatic sequence.

### Replay

- The final page stops on the last image.
- Show a small `再看一次` button.
- Tapping `再看一次` must return to the same pure black start screen with `轻触开始`.
- The replay reset must not show the final photo, video poster, progress bar, or any other content.

## Final Text

Content:

```text
涛，生日快乐
谢海
```

Design requirement:

- This is the most important visual typography part.
- The typography must look good, not just "clean" by default.
- It must be designed against the final image composition.
- Do not casually add decorative lines, boxes, fake-premium symbols, glow, or random ornaments.
- Use a restrained system-style or editorial-style type treatment.
- The main blessing may be stronger than the signature.
- The signature should be lower-key and should not compete with the main line.
- Avoid putting text near the seal, the red paste, reflections, or visually busy areas.
- If typography on the photo cannot be made tasteful, consider letting the final photo breathe first and then transition into a proper minimal closing card. Do not do cheap black-background text as a shortcut.

## Hard Constraints

- No image/video stretching.
- Use `object-fit: cover` or equivalent if the full screen needs to be filled.
- Preserve the dark cinematic mood of the photos.
- Avoid gray, washed-out image processing.
- Avoid long explanatory text.
- No frequent production deploys for small edits. Work locally first, deploy only after a meaningful version is approved.

## Current Site Behavior To Match

- Title: `涛，生日快乐`
- Initial button: loading gate, then `轻触开始`
- Opening video first
- Image order: `01 -> 02 -> 05 -> 04 -> 03`
- Image duration: `2.16s`
- Final button: `再看一次`
- Replay returns to the pure black start gate

