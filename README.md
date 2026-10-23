# NMA fireside chat

A 13-slide Slidev deck that carries every point of the supplied NMA outline, in its wording, with an approximately eight-minute speaking plan. Forest green, warm cream and the original NMA badge accompany photographs from the supplied trail-work collections.

## Run locally

```sh
cd ~/dev/trav/nma-fireside-chat
npm run dev
```

Open http://localhost:3030. Use the arrow keys to move through the deck. Presenter view is http://localhost:3030/presenter and includes the timing and speaker notes written in `slides.md`.

To reinstall dependencies on another computer, use Node 22.12+ (Node 24 LTS recommended) and `npm ci`.

## Edit

- `slides.md`: slide text, photographs, layout options and presenter notes.
- `styles/theme.css`: Pacific Northwest palette, typography and composition.
- `layouts/frame.vue`: the slide canvas and unchanged NMA logo.
- `public/photos/`: the 12 browser-ready photographs used on slides.
- `photo-library/` (gitignored, local only): the other 70 web copies, for swapping photos. Move one into `public/photos/` to use it. Original JPEG and HEIC files remain in Downloads.
- `drive-photos/` (gitignored, local only): full-size downloads from the WP #1 Orr Creek Drive folder.
- `sources/outline.txt`: a snapshot of the supplied Google Doc.
- `sources/photo-inventory.json`: the correspondence between original images and deck assets.
- `sources/trans-cascadia-downloads.json`: the verified Trans-Cascadia download inventory.

## Build

```sh
npm run build
```

This produces a static web deck in `dist/`. View it through a web server rather than opening its HTML directly. The build contains local fonts, photographs and the logo, so it does not depend on Google Drive or a font service.

Slidev's optional PDF export requires `playwright-chromium`. If needed:

```sh
npm install -D playwright-chromium
npm run export
```

## Sources

Content follows the Fireside Chat Outline: NMA document, read October 13, 2026. Numerical claims and trail completion statuses reflect that outline. Each slide includes its source and photo provenance in presenter notes.

Photos come from the three selected folders in the supplied photo collection:

- Kris & Robert Hand Crew 2026: 7 images.
- Sawtooth Area: 59 images, including its nested folders.
- Trans-Cascadia Work Parties 2026: 16 images. Original download sizes were checked against Drive metadata.

Logo source: `~/Downloads/NMA_badge_Logo_2022_White (1).png`. Its artwork and proportions are preserved. The outline's 1937 origin and the badge's 1973 date are presented as distinct parts of NMA's history.
