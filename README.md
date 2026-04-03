# media-kit

Claude Code skill for building speaker media kits from scratch.

Walks you through bio writing, photo prep (cropping, background removal, sizing), and page generation — so event organizers get everything they need in one place.

## Install

```bash
claude install-skill /path/to/media-kit
# or
claude install-skill github:augchan42/media-kit
```

## Usage

```
/media-kit
/media-kit ~/photos/headshot.jpg
```

## What it produces

1. **Bio variants** — one-liner, short (~50 words), medium (~100 words), long (~200 words)
2. **Photo assets** — headshot square, headshot wide, portrait, each with transparent background
3. **Media kit page** — Next.js or static HTML with copy buttons and download links
4. **Markdown kit** — plain text version for email and docs
5. **Downloadable zip** — all assets bundled for organizers

## Photo specs

| Asset | Dimensions | Format | Use |
|-------|-----------|--------|-----|
| Headshot (square) | 800x800 | PNG | Avatars, thumbnails |
| Headshot (wide) | 1170x1170 | PNG | Speaker grids, social media |
| Portrait | ~1200x1800 | JPEG | Banners, press, print |
| + transparent variants | Same | PNG | Composite graphics, stage screens |

## Requirements

- **Photo processing**: `sips` (built into macOS) for cropping, resizing, and rotation
- **Background removal**: `rembg` (`pip install rembg`) — runs U2-Net locally, no external uploads

## Bio principles baked in

- No year counts (they create update debt)
- Lead with current work, not background
- Spell out abbreviations (organizers copy verbatim)
- Name companies, not durations
- Write shortest variant first, then expand

## License

MIT
