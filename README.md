# aixmath.org

Main portal site for AI x Math and OmegaCombinator.

The site is intentionally static and has no user system. It points visitors to
the organization's blog, projects, seminars, and research notes.

## Development

```sh
pnpm install
pnpm dev
```

## Production

```sh
pnpm build
```

The build writes static files to `dist/`. The live site is published by a
self-hosted release pipeline: a push to `main` notifies a small deploy API
(see `.github/workflows/notify-deploy.yml`), which pulls this repository, runs
the build with pnpm, and swaps the published release atomically.
`www.aixmath.org` redirects to the canonical `https://aixmath.org/`.

`news.aixmath.org` is reserved for a future, separate site; the portal links to
it from the navigation and the community-node grid.

To preview the built site locally:

```sh
PORT=8120 pnpm start
```
