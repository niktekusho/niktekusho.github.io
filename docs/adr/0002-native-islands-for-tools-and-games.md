# Embed tools and games as native Astro islands, not iframes

All browser-based tools and games are built as native Astro island components rather than embedded iframes. Native islands share the site's design tokens, theme, and layout shell, eliminating the resize/theme-mismatch problems iframes produce. The cost is that any existing tool code must be ported into the Astro component model, but the UX and maintainability gain justifies it for a portfolio site where polish matters.
