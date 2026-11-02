## Design Reference: United Way Greater Toronto

Match the look and feel of unitedwaygt.org: clean, white, high contrast, with bold red calls to action and plenty of whitespace. Use the exact tokens below. Do not invent other brand colors.

### Colors (define as CSS variables)

| Variable | Hex | Use |
|---|---|---|
| --color-primary | #DA291C | United Way red: primary buttons (Donate), accents, campaign header |
| --color-primary-hover | #E74E42 | hover state for red buttons |
| --color-text | #040503 | headings, links, near-black text |
| --color-text-body | #444444 | paragraph text |
| --color-text-muted | #757575 | secondary text |
| --color-background | #FFFFFF | page and header background |
| --color-background-alt | #FAFAFA | alternate section background |
| --color-background-dark | #040503 | footer (white text) |
| --color-border | #E8E8E8 | dividers and card borders |
| --color-secondary | #41B6E6 | sky blue accent, used sparingly |
| --color-accent-green | #4D8406 | occasional accent |
| --color-accent-orange | #D64A04 | occasional accent |

Red, black and white should dominate. Blue, green and orange are small accents only.

### Fonts (define as CSS variables)

| Variable | Font | Use |
|---|---|---|
| --font-primary | Nunito Sans, weight 800 | h1 and h2 headings (stands in for Avenir Heavy) |
| --font-secondary | Nunito Sans, weights 400 and 700 | body text, links, forms (stands in for Avenir) |
| --font-accent | Oswald, weights 300, 400 and 700 | navigation, campaign hero text, section labels |

Load both from Google Fonts. Reference fonts only through the variables so they can be swapped later.

### Image slots

Do not use real photos. Use neutral placeholder boxes with the slot name as a label, so each can be swapped for a real file later.

| Slot name | Where | Description |
|---|---|---|
| united_way_logo.svg | header | full-colour United Way logo, red on white |
| united_way_logo_white.svg | footer | white version of the logo on dark background |
| hero_home.jpg | home hero | wide banner of a community photo, text overlaid on the left |
| hero_donate.jpg | donate page hero | wide banner, warm community photo |
| hero_volunteer.jpg | volunteer page hero | wide banner of volunteers in action |
| photo_community_01.jpg to photo_community_05.jpg | cards and story sections | square or 4:3 photos of people in the community |
| photo_person_01.jpg | testimonials | portrait headshot of a person |
| icon_facebook.svg, icon_instagram.svg, icon_linkedin.svg, icon_twitter.svg | footer | social icons in white |
| icon_search.svg, icon_menu.svg, icon_close.svg | header | UI icons in near-black |
| icon_chevron_down.svg, icon_chevron_right.svg | menus, accordions, links | small directional icons |

### Style notes

- Buttons: solid red with white text, square or slightly rounded corners, darker-to-lighter red on hover.
- Links: near-black, no underline, short color transition on hover.
- Layout: white header with logo on the left and navigation on the right, a red Donate button in the header, and a black footer.
- Cards: white with a thin light-gray border, no heavy shadows.
