# niktekusho.github.com

Personal GitHub profile site. Serves three audiences: hiring (CV + work history), hobbyist (photo gallery), and developer (browser-based tools and games).

## Language

**CV Data**:
A [JSON Resume](https://jsonresume.org/schema/) document that is the canonical source of truth for CV content. Rendered as a custom-designed HTML page.
_Avoid_: resume, curriculum

**CV PDF**:
Downloadable Europass-format PDF artifact generated from the EU Europass portal. Not the source of truth — derived from CV Data for recruiters who require the official format.
_Avoid_: resume PDF, CV file

**Tool**:
A browser-based interactive utility exposed at its own route (`/tools/{slug}`), built as a native Astro island.
_Avoid_: app, widget, mini-app

**Game**:
A browser-based game (e.g. sudoku, nonogram) exposed at its own route, built as a native Astro island.
_Avoid_: toy, puzzle app

**Island**:
An Astro client-side component that hydrates interactivity on an otherwise static page. May be written in React or Svelte.
_Avoid_: component (too generic), widget

**Photo**:
An entry in the **Gallery** consisting of an image file plus optional EXIF metadata (camera, lens, date) and an optional caption. Both metadata fields may be absent and the UI must render gracefully when they are.
_Avoid_: image, picture

**Gallery**:
The collection of **Photos**, rendered initially as a single flat grid at `/gallery`. Albums and tags are not in scope yet but the flat data model permits them later.
_Avoid_: photos page, portfolio (collides with the tools/games portfolio section)

## Relationships

- **CV Data** is rendered into one HTML CV page and also exported as **CV PDF** for download
- Each **Tool** and **Game** is one **Island** mounted inside a shared Astro layout
- **Tools** and **Games** are siblings — both live under the portfolio section, each at its own route
- The **Gallery** is a flat list of **Photos**; each **Photo** may carry EXIF and/or a caption, both optional

## Flagged ambiguities

- "tools" was used loosely to include games — resolved: **Tool** = utility, **Game** = game; both are Islands, both get own routes, but they are distinct terms
