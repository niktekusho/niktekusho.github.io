# CV pipeline: JSON Resume as source, custom HTML render, Europass PDF as artifact

The CV lives as a [JSON Resume](https://jsonresume.org/schema/) document committed to the repo. The site renders it through a custom-designed HTML page (not a stock JSON Resume theme). The Europass PDF, manually exported from the EU Europass portal, is kept in the repo as a downloadable artifact for recruiters who require the official format. The JSON Resume document and the Europass PDF must be kept in sync manually — when CV content changes, both the JSON file and the Europass portal entry must be updated and re-exported.

## Considered Options

- **Custom JSON/YAML schema** — rejected: more design work, no ecosystem
- **Hybrid (JSON Resume + custom extensions)** — rejected for now: Europass-only fields (detailed CEFR language matrix, driving license) can be handled with optional top-level fields if needed later, without forking the schema
- **Stock JSON Resume theme** — rejected: design ownership matters for a personal site
