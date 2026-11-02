# United Way Greater Toronto Brand Assets

Scraped from https://www.unitedwaygt.org/ for use as inputs to a website generation tool. Every asset uses a placeholder style name, so a prompt can say "use `primary` font" or "use `united_way_logo.svg`" and the file exists here under that exact name.

## What was done

Two subagents scraped the site in parallel with curl:

1. **Colors and fonts.** They read the homepage, `/our-work/` and the theme stylesheet `frontend.css`.
2. **Images.** They read the homepage and 13 inner pages (about, mission, get involved, volunteer, workplace giving, CN Tower Climb, our work, investments, news, 70 years, contact, careers, donate). They extracted `img` tags, `srcset`, `og:image` tags, CSS backgrounds, favicons and inline SVGs.

Every file was renamed to a descriptive snake_case name. Nothing keeps a hashed or original filename.

## Folder layout

```
colors/
  color_palette.md      table: placeholder name, hex, rgb, role, tier (primary/secondary/neutral)
  colors.css            CSS variables using the same names, e.g. --color-primary
fonts/
  fonts.css             @font-face rules using the placeholder family names
  fonts_manifest.md     placeholder -> real font, weights, files, usage, license
  *.woff / *.woff2      font files
images/
  images_manifest.md    every image: description, dimensions, usage, source URL
  logos/                united_way_logo.svg, _white, _white_header, _icon, partner/campaign logos
  favicon/              favicon_* and apple_touch_icon_* by pixel size
  icons/                icon_*.svg (search, menu, close, chevrons, social)
  hero/                 hero_* wide banner images, named by page or topic
  photos/               photo_* people and community photography
  backgrounds/          background_* textures and illustration_* / graphic_* art
  other/                card_*, map_*, mockup_* and report graphics
```

## How things are annotated

- **Colors.** Placeholder names are the identifiers, e.g. `primary`, `secondary`, `text`, `background`, `border`, `button`, `link`. Variants add a suffix: `_hover`, `_light`. Accents are `accent_green`, `accent_orange` and `accent_purple`. Each color has a tier (primary, secondary or neutral) and a note on where the site uses it. The same names are CSS variables in `colors/colors.css`.
- **Fonts.** The CSS family names are the placeholders, as in `font-family: "primary"`. Their real families are:

  | Placeholder | Real font | Used for |
  |---|---|---|
  | `primary` | Avenir Heavy | h1 and h2 headings |
  | `secondary` | Avenir (55 Roman) | body text and links |
  | `accent` | Oswald (300, 400, 700) | campaign hero and header navigation |
  | `serif` | Georgia | h4 and blockquotes |
  | `display` | Obviously Black Italic | occasional campaign headings |
  | `fallback_sans` | Nunito Sans | free substitute for Avenir |

- **Images.** The filename prefix tells the tool what the file is for: `hero_`, `photo_`, `icon_`, `background_`, `card_`, `map_`, `mockup_`. Logos are named by variant, e.g. `united_way_logo.svg` (full colour), `united_way_logo_white.svg` (for dark or red backgrounds) and `united_way_logo_icon.png`. `images/images_manifest.md` lists a description, dimensions, suggested usage and source URL for each.

## Caveats

- **Licensing.** Avenir, Georgia and Obviously are proprietary. The files were pulled from the site's own server, so check licensing before reuse. Oswald and Nunito Sans are free (SIL OFL).
- **Missing font weight.** The site has only one Avenir bold file, so `secondary` bold reuses `primary_bold.woff`.
- **Logos and icons.** The site has no logo or icon image files for most uses. The white logos and the UI and social icons were extracted from inline SVGs in the page HTML.
- **Favicons.** There is no ICO file. The favicons are the WordPress PNGs from 32 to 270 px.
- **Pages.** `/get-help/` returned 404 and was skipped. `/donate/` has no distinct hero, so `hero_donate.jpg` is that page's `og:image`.
- **Image labels.** The agent viewed only about six images. The other labels, and the hero versus photos split, come from alt text and page context. A few names are best guesses, such as `photo_rat_race.jpg`.
- **Colors.** They come from the theme's WordPress editor palette. Red, black and white dominate the real look.
- **Copyright.** The images are United Way's, so check usage rights before publishing.
