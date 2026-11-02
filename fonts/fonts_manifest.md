# Fonts - United Way Greater Toronto (unitedwaygt.org)

Source: https://www.unitedwaygt.org/wp-content/themes/uwgt/dist/css/frontend.css (@font-face rules; files at /wp-content/themes/uwgt/dist/fonts/). Base font size is `html { font-size: 10px }`, so 1rem = 10px.

| placeholder | real family | weights | files | used for | sizes | license / source |
|---|---|---|---|---|---|---|
| primary | Avenir Heavy (Avenir 85 Heavy) | 700 | primary_bold.woff | h1, h2, footer menu titles, buttons | h1/h2 36px, uppercase, letter-spacing 2px on h1 | Proprietary (Linotype / Monotype). Self-hosted by the site: https://www.unitedwaygt.org/wp-content/themes/uwgt/dist/fonts/Avenir-85-Heavy.woff |
| secondary | Avenir (Avenir 55 Roman) | 400 (700 reuses Heavy file) | secondary_regular.woff | body text, links, h3 (22px uppercase), nav, inputs | body/links 16px, line-height 22px; h3 22px | Proprietary (Linotype / Monotype). https://www.unitedwaygt.org/wp-content/themes/uwgt/dist/fonts/Avenir-55-Roman.woff |
| accent | Oswald | 300, 400, 700 (site file is demibold) | accent_light.woff2, accent_regular.woff2, accent_bold.woff2, accent_bold.woff | campaign hero h1 (60px uppercase), hero subtitle (28px), campaign header nav (18px) | 18px to 60px | SIL OFL 1.1, free. https://fonts.google.com/specimen/Oswald |
| serif | Georgia | 400 | serif_regular.woff2, serif_regular.woff | h4 (18px), blockquotes (23px, large 33px) | 18px to 33px | Proprietary (Monotype/Microsoft). https://www.unitedwaygt.org/wp-content/themes/uwgt/dist/fonts/georgia-webfont.woff |
| display | Obviously Black Italic | 900 italic | display_black_italic.woff | occasional campaign headings (inline style, !important) | varies | Proprietary (Hannes von Doehren, Fonts In Use / commercial). https://www.unitedwaygt.org/wp-content/themes/uwgt/dist/fonts/Obviously-Black_Italic.woff |
| fallback_sans | Nunito Sans (substitute for Avenir) | 400-800 variable (latin subset) | substitute_nunito_sans_latin.woff2 | fallback when Avenir is not licensed | n/a | SIL OFL 1.1, free. https://fonts.google.com/specimen/Nunito+Sans |

## Notes
- Avenir, Georgia and Obviously are proprietary commercial fonts. The woff files above were downloaded from the live site's own server; check licensing before reuse on other domains. If unlicensed, use `fallback_sans` (Nunito Sans), the closest free Google Font to Avenir. Oswald is free.
- The site's CSS declares `Oswald` weight 300 as Owswald-Light.woff2 (typo, 404 on server); the correct file Oswald-Light.woff2 exists and was downloaded.
- The site has no Google Fonts / Adobe Fonts requests; everything is self-hosted.
- Fallback stacks: primary/secondary `Helvetica, Arial, sans-serif`; accent `Impact, "Arial Narrow", sans-serif`; serif `Georgia, serif`.
- Heading styles on site: h1 36px/50px Avenir Heavy uppercase; h2 36px/50px Avenir Heavy uppercase; h3 22px/28px Avenir uppercase; h4 18px/28px Georgia; h5 12px; h6 10px.
