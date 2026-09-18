# Base44 Dev Environment

## Project

Astro static blog located in `Blog_rhumanas/`. No backend, no database, no external services or secrets required.

## Running

```sh
docker compose -f docker-compose.base44.yml up -d
```

The app runs on host port 3000 (mapped to Astro's dev port 4321). Dependencies install automatically on container start via `npm install`.

## Important Notes

- The Astro config sets `base` for GitHub Pages deployment (`/Blog_comunicacion_relaciones`), but it's now overridable via the `ASTRO_BASE` env var. The compose file sets `ASTRO_BASE=/` so the preview serves at `/`. GitHub Pages deployment is unaffected (no env var = default base path).
- Node >= 22.12.0 required (per `package.json` engines).
- Astro v7 with MDX, RSS, and sitemap integrations.
- Live reload is active; file changes in `Blog_rhumanas/src/` appear in the preview automatically.
