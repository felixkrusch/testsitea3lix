# testsitea3lix

Juniper is a fictional restaurant website for testing a3lix. It is a static Astro site with six editable Markdown menu dishes, opening hours, and no external services or API keys.

## Run locally

Requires Node.js 22.23.4 or later and npm.

```sh
npm ci
npm run dev
```

Open http://127.0.0.1:4321. Validate with `npm run build`.

## Edit with a3lix

Import `restaurant.a3lix`, select an empty local destination, and connect your GitHub account. The a3lix GitHub App also needs access to this repository.

Each dish lives in `src/content/menu/*.md`. The body is its description; frontmatter sets `title`, `price` (EUR), `course`, and `order`. The homepage renders these files directly. In the Restaurant menu collection, use the source editor for prices and course/order fields. Keep the frontmatter when editing entries; use an existing dish as a template when adding one. New course names appear automatically.

Restaurant details and opening hours live in `src/content/restaurant.json`.

Example assistant requests:

- Change whipped feta from 8 to 10 euros.
- Replace the market fish with a mushroom risotto for 19 euros.
- Add a 7-euro soup to Small plates, with the required frontmatter.
- Change Sunday closing time to 21:00.

Changes are local until committed and pushed. This repository does not configure hosting or automated deployment; pushing alone does not make a website live.

The restaurant, address, menu, and illustration are demo content. The dish descriptions are not a verified allergen guide.
