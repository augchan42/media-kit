# Media Kit

Claude Code skill for building speaker media kits from scratch.

Walks you through bio writing, photo prep (cropping, background removal, sizing), and page generation — so event organizers get everything they need in one place.

## Install

**Add the plugin from the marketplace:**

```shell
/plugin marketplace add augchan42/media-kit
```

**Install it:**

```shell
/plugin install media-kit@augchan42-media-kit
```

That's it. The `/media-kit` command is now available in Claude Code.

## Usage

Start from scratch — the skill interviews you and builds everything:

```
/media-kit
```

Or point it at an existing headshot to skip straight to photo prep:

```
/media-kit ~/photos/headshot.jpg
```

### What it builds

The skill interviews you in 2-3 question rounds, then produces everything an event organizer needs. Here's a real example built with this skill: [augustinchan.dev/media-kit](https://augustinchan.dev/media-kit)

**Bios** — four variants, shortest first, each building on the previous:

> **One-liner:** CTO & Founder, Digital Rain Technologies. Enterprise architecture background (Informatica, Dun & Bradstreet), now building systems that reason — across culture, operations, and enterprise governance.
>
> **Short (~50 words):** Augustin Chan is the CTO and founder of Digital Rain Technologies. Enterprise architecture background (Informatica, Dun & Bradstreet), now building systems that reason — across culture, operations, and enterprise governance. Co-host of the Hong Kong AI Podcast. B.S. Cognitive Science (Computation), UC San Diego.
>
> **Medium (~100 words):** Expands with company names, regions (APAC, MENA, Europe), current projects (ARA-Eval, Ridgeline, Six Lines), and the Hong Kong AI Podcast.
>
> **Long (~200 words):** Full press bio with a paragraph per project and concrete details.

Each bio has a copy button — organizers grab exactly the length they need.

**Photo assets** — crops, resizes, and removes backgrounds from a single source photo:

| Asset | Dimensions | Format | Use |
|-------|-----------|--------|-----|
| Headshot (square) | 800×800 | PNG | Avatars, thumbnails |
| Headshot (wide) | 1170×1170 | PNG | Speaker grids, social media |
| Portrait | ~1200×1800 | JPEG | Banners, press, print |
| + transparent variants | Same | PNG | Composite graphics, stage screens |

**Page + bundle** — generates a media kit page (Next.js, static HTML, or Markdown) with copy buttons, download links, and a zip of all assets.

## Requirements

- **Photo processing**: `sips` (built into macOS) for cropping, resizing, and rotation
- **Background removal**: `rembg` — runs U2-Net locally, no external uploads

Install rembg if you don't have it:

```shell
pip install rembg
```

## Bio principles baked in

- No year counts (they create update debt)
- Lead with current work, not background
- Spell out abbreviations (organizers copy verbatim)
- Name companies, not durations
- Write shortest variant first, then expand

## License

MIT
