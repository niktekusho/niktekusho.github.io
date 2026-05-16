# Astro as the site framework with multi-framework islands

The site needs to host a growing portfolio of browser-based tools and games alongside static content (CV, photo gallery). We chose Astro over Next.js static export, SvelteKit, or plain Vite+React because it ships zero JS by default for static pages, supports React and Svelte islands on the same page without conflict, and splits bundles per route automatically. The owner is proficient in React and wants to learn Svelte — Astro lets both coexist without a forced migration: start tools in React, write new games in Svelte as familiarity grows.

## Considered Options

- **Next.js static export** — rejected: React-only, heavier baseline bundle, no built-in multi-framework support
- **SvelteKit + adapter-static** — rejected: would require rewriting any existing React work
- **Vite + React** — rejected: hand-roll routing, code splitting, and image optimisation
