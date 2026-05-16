# i18n: English at root, no prefix; locale prefixes reserved for future languages

The site ships English-only at launch, served from the root (`/cv`, `/tools/sudoku`) with no locale prefix. URL structure is set up via `@astrojs/i18n` with English as the default locale (no prefix) so additional languages can be added later under prefixed paths (`/it/cv`, `/de/cv`) without breaking existing English URLs.

This avoids both extremes: not committing to translating everything up front (no `/en/` clutter), but not locking out future locales either. Italian is the likeliest second locale given the Europass context but is deferred until there is real content to publish.
